# Guía Básica de PHP


Ingresa el comando ` php -a ` en una terminal:

```bash
Interactive shell

php >
```
## Input / Output

```php
  $stdin = fopen('php://stdin','r');
  echo "Ingrese nombre";
  $nombre = fgets($stdin);
  echo "Hola $nombre";
```

### echo
```php
echo "Hola mundo";
# Hola Mundo
```
### print
```php
print "Hola mundo";
# Hola mundo
```
### print_r
```php
print_r("Hola mundo");
# Hola mundo
```
### var_dump
```php
var_dump("Hola Mundo");
# string(10) "Hola Mundo"
```
## Comillas simples y dobles

Comillas dobles evalua el contenido
```
$a = "Juanito";
echo "Hola $a : \nBienvenido";
# Hola Juanito :
# Bienvenido
```
Comillas simples muestra tal cual
```
$a = "Juanito";
echo 'Hola $a : \nBienvenido';
# Hola $a : \nBienvenido
```

## Constantes y Variables

### Variable

```php
$mi_variable=10;
var_dump($mi_constante);
# string(21) "Esta es una constante"
```

### Constante
```php
define("mi_constante","Esta es una constante");
var_dump(mi_constante);
# string(21) "Esta es una constante"
```

## Tipo de datos

### Entero
```php
$n=1;
var_dump($n);
# int(1)
```
### Flotante
```php
$a = 1.4;
var_dump($a);
# float(1.4)
```
### Booleano
```php
$a=true;
var_dump($a);
# bool(true)
```
### Cadena
```php 
$a = "Una cadena";
var_dump($a);
# string(10) "Una cadena"
```

### Cadena
```php 
$a = null;
var_dump($a);
# NULL
```


### Vectores Enumerativas
```php
$arreglo=array("uno",2,3.0);
// otra forma : $arreglo = ["uno",2,3.0];
var_dump($arreglo);
echo arreglo[0];
# uno
```

### Vectores Asociativas
```php
$arreglo = array("uno"=>1,"dos"=>2,"tres"=>3);
// otra forma : $arreglo = ["uno"=>1,"dos"=>2,"tres"=>3];
var_dump($arreglo);
echo arreglo["uno"];
# 1
```

## Operadores


### Operadores Arimeticos

```php
//Suma
echo $10 + 4;
# 14

//Resta
echo 10 - 4;
# 6

//Multiplicacion
echo 10 * 4;
# 40

//Division
echo 10 / 4;
# 2.5;

//Potencia
echo 10 ** 4;
# 10000;


//Modulo
echo 10%4;
# 2 
```

### Operadores de cadena
```php
//Concatenación
$nombre="Juanito";
$edad=20;
$saludo="Hola ".$nombre." tu edad es ".$edad;
echo $saludo;
# Hola Juanito tu edad es 20
```

### Operadores logicos
```php
//Igualdad
echo 1 == 1;
# true;
echo 1 == 1.0;
# true

//Identico
echo 1 === 1;
# true;
echo 1 === 1.0;
# false

//Diferente ( != , <> ) 
echo 1 != 1;
# false
echo 1 != 1.0;
# false

//No identico
echo 1 !== 1;
# true
echo 1 !== 1.0;
# false

//Menor que
echo 1 < 2;
# true

//Mayor que
echo 1 > 2;
# false

//Menor igual que
echo 1 <= 2;
# true

//Mayor igual que
echo 1 >= 2;
# false

//Mayor menor o igual
echo 1<=>1;
# 0
echo 1<=>2;
# -1
echo 2<=>1;
# 1
```
### Operador Null
```
echo $a ?? 'default';
# default
```


### Operadores de incremento y decremento

```php
$a = 10;

//suma y asigna
echo ++$a:

//asigna y suma
echo $a++;

//resta y asigna
echo --$a;

//asigna y resta
echo $a--;

//suma y asigna
echo $a+=2;

//resta y asigna
echo $a-=2;

//multiplica y asigna
echo $a*=2;

//divide y asigna
echo $a/=2;

//concatena y asigna
echo $c = "Hola ";
echo $c .= "mundo";

```

### Operadores Logicos

Y
```php
// and, & , &&
echo true and true and false;
#

echo true & true & false;
#

echo true && true && false;
#
```

O
```php
// or, | , ||
echo true or true or false;
#

echo true ! true ! false;
#

echo true !! true !! false;
#

// xor
echo true xor false;
```

NO
```php
// !
echo !true;
# false
```

### Operador ternario
```php
// condicion ? valor1 : valor2;
echo true ? 1 : 2;
# 1
```

### Operador de control de errores
```php
define(); // muestra mensaje de error ya que espera 2 parametros
# PHP Warning:  define() expects at least 2 parameters, 0 given in php shell code on line 1

@ define(); //No muestra mensaje de error

```

## Sentencias de control
### Condicionales
#### If Else

Condicional simple 
```php
if( condicion )
{
    //Lineas de codigo
}
```

Condicional Else
```php
if( condicion )
{
    //Lineas de codigo
}
else
{
    //Lineas de codigo
}
```

Condicional anidada
```php
if( condicion )
{
    //Lineas de codigo
}
elseif(condicion)
{
    //Lineas de codigo
}
else
{
    //Lineas de codigo
}
```

### Bucle

#### While
```php
while(condicion)
{
    //Lineas de codigo
}
```
#### Do While
```php
do{
    //Lineas de codigo
}while(condicion);
```
#### For
```php
for( inicializacion; condicion; operacion)
{
    //Lineas de codigo
}
```
#### ForEach

Foreach arreglo enumerativo
```php
foreach($arreglo as $elemento)
{
    //Lineas de codigo
}
```
Foreach arreglo asociativo
```php
foreach($arreglo as $key => $item)
{
    //Lineas de codigo
}
```

### Seleccion
#### Switch
```php
switch(valor)
{
  case valor1:
    //Lineas de codigo;
    break;
  case valor2:
    //Lineas de codigo;
    break;
  case valor_n:
    //Lineas de codigo;
    break;
  default:
   //Lineas de codigo;
}
```

## Funciones

Simple
```php
function saludar()
{
  //Lineas de codigo
}
```
Con parametros
```php
function saludar($parametro)
{
  //LInesa de codigo
}
```
En variable
```php
$saludar = function($nombre){
  echo "Hola".$nombre;
};
$saludar("Juanito");
# Hola Juanito
```

Anonima
```php
echo function() {
  return "Hola mundo";
};
# Hola mundo
```

Usando Variables externas a la funcion

```php

$nombre = "Juanito";

function saludar () use($nombre) {
  echo "Hola ".$nombre;
};

saludar();
# Hola Juanito

$nombre = "Pepito";

saludar();
# Hola Juanito 

/* use() Importa la variable al momento de crearla y no captura los cambios posteriores*/

```


## Inclusion de Archivos

### include
Si el archivo importado contiene error, muestra el mensaje y continua con al ejecucion. El archivo es importado por cada llamada realizada.

```php
include 'include.php'
```


### include_once
Si el archivo importado contiene error, muestra el mensaje y continua con al ejecucion. El archivo solo es importado en su primera llamada realizada.

```php
include_once 'include.php'
```


### require
Si el archivo importado contiene error, muestra el mensaje y para la ejecucion. El archivo es importado por cada llamada realizada.

```php
include 'include.php'
```


### require_once
Si el archivo importado contiene error, muestra el mensaje y para la ejecucion. El archivo solo es importado en su primera llamada realizada.

```php
include_once 'include.php'
```
## Sesiones


Cuando inicias una session, prepara la variable $_SESSION;

Iniciar Sesion
```php
session_start();
```

Ver variables de session
```php
var_dump($_SESSION);
```


Crer y asignar valor a variable session
```php
$_SESSION["mi_session"]=1;
$_SESSION["mi_session"]=2;
```

Eliminar session
```php
session_destroy();
```


## Cookies

Ver variables cookie
```php
var_dump($_COOKIE);
```

Crear variable cookie
```php
// nombre cookie, valor, fecha de expiracion
setcookie('nombre','valor',time()+36000);
```

Asignar valor a variable cookie
```php
setcookie('nombre','nuevo_valor');
```

Destruir cookie
```php
setcookie('nombre','',time()-1);
```
## Programacion Orientada a Objetos

### Clases

Estructura de clase
```php
class MiClase
{
 //Linea de codigo
}

$instanciaClase1 = new MiClase();
$instanciaClase2 = new MiClase();

```


### Consutructores y Destructores

```php

public class MiClase
{

  public function __construct()
  {
      echo "Constructor sin parametro";
  }

  public function __construct($parametro)
  {
    echo "Constructor con parametro : " . $parametro;
  }
  
  public function __destruct()
  {
    echo "Destruido";
  }
}


$miObjeto1 = new MiClase();
# Constructor sin parametro

$miObjeto2 = new MiClase("ABC");
# Constructor con parametro : ABC

# Destruido
```

## Herencia

```php
class Padre
{
    $pripiedad_padre;
    
    function metodo_padre()
    {
        //Lineas de codigo
    }
    
    function __construct()
    {
        //Constructor padre
    }
}

class Hijo extends Padre
{
    $propiedad_hijo;
    
    function metodo_hijo()
    {
        parent::pripiedad_padre="Valor inicial";
        $this->propiedad_hijo = "Valor inicial";
    }
    
    function __construct()
    {
        parent::__construct();
    }
}

```

### Propiedades y metodos

```php
class MiClase
{
   public $mi_propiedad;
   
   public function mi_metodo()
   {
      //Lineas de codigo
   }
}

$instanciaClase = new MiClase();
$instanciaClase->mi_propiedad = "Valor";
$instanciaClase->mi_metodo();

```

### Niveles de acceso

```php

class Padre
{
    public     $propiedad_publica_padre;
    protected  $propiedad_protegida_padre;
    private    $propiedad_privada_padre;
}


class MiClase
{
   public $mi_propiedad_publica;
   private $mi_propiedad_privada;
   
   public function mi_metodo_publico()
   {
      parent::propiedad_publica_padre ="VALOR"; #Acceso , es publica
      parent::propiedad_protegida_padre ="VALOR"; #Acceso , es protegida   
      parent::propiedad_privada_padre ="VALOR"; #No es privada   
      
      //Lineas de codigo
   }
   
   private function mi_metodo_privado()
   {
      //Lineas de codigo
   }
}

$instanciaClase = new MiClase();

$instanciaClase->mi_propiedad_publica = "Valor";
$instanciaClase->mi_propiedad_privada = "Valor"; #Genera error 

$instanciaClase->mi_metodo_publica();
$instanciaClase->mi_metodo_privada(); #Genera error 

$instanciaPadre = new Padre();
$instanciaPadre->propiedad_publica_padre ="VALOR"; #Acceso , es publica
$instanciaPadre->propiedad_protegida_padre ="VALOR"; #No , es protegida   
$instanciaPadre->propiedad_privada_padre ="VALOR"; #No es privada   
      

```

### Encapsulamiento, Getters y Setters

```php
class Persona
{
   private $nombre;
   
   public function getNombre()
   {
      return $this->nombre;
   }
   
   public function setNombre($_nombre)
   {
      $this->nombre = $_nombre;
   }
}

$cliente = new Persona();
$cliente->setNombre("Juanito");

echo "Bienvenido ". $cliente->getNombre();

# Bienvenido Juanito

```

## Namespaces

Declaracion de namespace  y sus clases

```php
namespace vehicles;

class Car
{

}
```

Importando clases de un namespace

```php
use vehicles\Car;
$obj = nes Car();
```

Importando varias clases


```php
use vehicles\Car;
use vehicles\Truck;

#Resumido
use vehicles\{Car,Truck};
```

Clases homonimas de diferentes namespaces

```php
$objUser1 = administrativo\User();
$objUser2 = ejecutivo\User();
```
## Propiedade y metodos estaticos

```php
class Padre
{
  public static $propiedad_static;
 
 
  public static function metodo_static()
  {
      //Lineas de codigo 
  }
}
```

Acceso desde fuera

```php
  Padre::propiedad_static ="VALOR";
  Padre::metodo_static();
```

Acceso desde hijos

```php
  class Hijo extends
  {
      function metodo_hijo()
      {
          self::propiedad_static;
          self::metodo_static;
      }
  }
```
## Variables de entorno web

### $_GET

Captura las variables enviadas por el metodo GET.
```php
    $nombre = $_GET["nombre"];  
```

### $_POST

Captura las variables enviadas por el metodo POST.
```php
    $nombre = $_POST["nombre"];  
```

### $_REQUEST

Captura las variables enviadas por el metodo GET o POST.
```php
    $nombre = $_REQUEST["nombre"];  
```

### $_FILES

Captura un archivo subidos al sistema.


```php
    $nombre = $_REQUEST["nombre"];  
```



### $_SESSION

Captura las variables guardadas en session.
```php
    $nombre = $_SESSION["nombre"];  
```

## Funciones PHP

### isset

Retorna true si la variable existe:
```php
  isset($variable)
```
### empty

Retorna true si la variable es null
```php
  empty($variable)
```

### unset

Destruye el objeto
```php
  unset($objeto)
```

### mail
Envia un correo
```php
   # destinatario , asunto, cuerpo , remitente
   mail($to,$subject,$body,$from);
```

## Manejo de archivos

### Crear y escribir archivo

```php
    $file = fopen("archivo.txt","a")
            or die("Error al crear el archivo");
    
    fwrite($file, "Hola mundo");
    fwrite($file, " .. Fin");
    fclose($file);
```


### Leer archivos

```php 
    $file = fopen("archivo.txt","r");
   
    $linea = 0;
    
    while(!feof($file))
    {
        $contenido = fgets($file);
        $contenido = nl2br($file); #Cambia nl a <br>
        
        echo "$linea -> $contenido";
        $linea++;       
    }
```

### Eliminar archivo

```php
     unlink($filename);
```
  
## Conexion a BD
 
### Select

```php
   $cn = mysqli_connect($server, $userDB, $passBD)
         or die("Error al conectarse a la BD");
         
   mysqli_select_db($cn, "BaseDatos") 
   or die("Error al seleccionar BD");
   
   $rs = mysqli_query($cn , "Select ...") 
   or die("Error al realizar la consulta");
   
   while( $row = mysqli_fetch_array($rs) )
   {
       echo $row["column_name"];
   }
```

#### Ejecucion de comandos
 
```php
<!Doctype html>
<html>

<head>
</head>

<body>

    <?php
    if(isset($_REQUEST['upload'])){
        
        echo "Se subira el archivo";
        
        foreach($_FILES['foto'] as $item => $valor)
        {
            echo "$item => $valor <br>";
        }
        
        $tmp_name=$_FILES['foto']['tmp_name'];
        $name = $_FILES['foto']['name'];
        
        copy($tmp_name,$name);
        
        echo "Archivo subido exitosamente";
        
        echo "<img src='$name'>";
        
        
    }else
    {
        echo "No subira el archivo";
    }
    ?>
        <form enctype="multipart/form-data" method="post">
            <input type="file" name="foto">
            <input type="submit" name='upload' value="upload">
        </form>
</body>

</html>
```
