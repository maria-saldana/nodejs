<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1"/>
</head>
<style>body{
	padding-top:20px;
	max-width: 100%;
	margin: auto;
	font: bold 16px Arial;

}
table{
	text-align:left;
	border: 2px solid black;
	margin: auto;
	
	background-color:pink;
}
td
{
font: bold 16px Arial;
padding: 5px;
}
input[type=text],input[type=date],input[type=password],
input[type=email],select
{
	width:100%;
	font: 16px Arial;
	height:30px;
}
input[type=checkbox]
{
			width:  15px; 
            height: 15px; 
}

input[type=submit],input[type=reset]
{
	font: 16px Arial;
	height:30px;
}
</style>
<body>
<form name="Ejercicio6" method="post" action="Ejercicio6.php"> 
<table>
<tr><td colspan="2" align="center"><h2>Datos de usuario</h2></td></tr>
<tr><td>Nick de usuario: </td><td><input type="text" name="nick"></td></tr>
<tr><td>Correo: </td><td><input type="email" name="correo"></td></tr>
<tr><td>Contraseña: </td><td><input type="password" name="pass"></td></tr>
<tr><td>Pais: </td>
<td>
<select name="pais">
<option value="Perú">Perú</option>
<option value="Chile">Chile</option>
<option value="Argentina">Argentina</option>
<option value="Ecuador">Ecuador</option>
<option value="Italia">Italia</option>
<option value="Brasil">Brasil</option>
<option value="Grecia">Grecia</option>
<option value="Uruguay">Uruguay</option>
</select>
</td></tr>
<tr><td>Fecha de nacimiento: </td><td><input type="date" name="fecha"/></td></tr>
<tr><td colspan="2"><input type="checkbox" name="check1" >Recibir noticias </td></tr>
<tr><td colspan="2"><input type="checkbox" name="check2" >Recibir promociones </td></tr>
<tr><td colspan="2"><input type="checkbox" name="check3" >Aceptar las Condiciones y la política de cookies</td></tr>
<tr><td align="right"><input type="submit" value="Registrar" name="registrar"></td><td><input type="reset" name="cancelar" value="Cancelar"></td></tr>
<td><input type="edit" name="Editar" value="Editar"></td></tr>
</table>
</form>
</table>
</body>
</html>
<?php
$servername = "(https://ghcr.io/railwayapp-templates/postgres-ssl)";
$database = "(https://ghcr.io/railwayapp-templates/postgres-ssl)";
$username = "maria.saldana.udgvirtual.udg.mx";
$password = "22Carmen";
// Create connection
$conn = mysqli_connect($servername, $username, $password, $database);
// Check connection
if (!$conn) {
    die("Connection failed: " . postgres-ssl_connect_error());
}
echo "Connected successfully";
mysqli_close($conn);


public function index(){
    Utils::isAdmin();
    $categoria = new Categoria();
    $categorias = $categoria->getAll();

    require_once 'views/categoria/index.php';
}

public function crear(){
    Utils::isAdmin();
    require_once 'views/categoria/crear.php';
}

public function modificar(){
    Utils::isAdmin();
    require_once 'views/categoria/modificar.php';
}

public function save(){
    Utils::isAdmin();

    if(isset($_POST) && isset($_POST['nombre'])){
        //GUARDAR LA CATEGORIA EN BD
        $categoria = new Categoria();
        $categoria->setNombre($_POST['nombre']);
        $save = $categoria->save();
    }
    header('location:'mary-salda.database.windows.net'categoria/index');
}
?>
