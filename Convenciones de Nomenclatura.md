# Convenciones de nomenclatura

## Convenciones del uso de Mayúsculas y minúsculas
Muchas convenciones de nomenclatura hacen uso de las mayúsculas y minúsculas en sus identificadores.

Entre ellas tenemos:

### 1. Estilo Pascal (PascalCase)
La primera letra del identificador y la primera letra de las siguientes palabras concatenadas están en mayúsculas. El estilo de mayúsculas y minúsculas Pascal se puede utilizar en identificadores de tres o más caracteres, por ejemplo:
```
ImageSprite
```

### 2. Estilo camelCase
La primera letra del identificador está en minúscula y la primera letra de las siguientes palabras concatenadas en mayúscula, por ejemplo:
```
imageSprite
```

### 3. Estilo Mayúsculas (ALL_CAPS)
Todas las letras del identificador se encuentran en mayúsculas ejemplo
```
IO
MI_CONSTANTE
```

### 4. Estilo minúsculas (small_caps)
Todas las letras del identificador se encuentran en minúsculas ejemplo
```
system
mi_variable
```

Esta designación de la convención se utiliza muy poco

Cada lenguaje de programación hace uso de estos estilos según el identificador que use y de acuerdo a su convención.

En la siguiente tabla tenemos, las convenciones usadas por cada lenguaje de programación

|Tipo                |PHP        |C#         |Java       |
|--------------------|-----------|-----------|-----------|
|Clase               |PascalCase |PascalCase |PascalCase |
|Constante           |ALL_CAPS   |PascalCase |ALL_CAPS   |
|Método              |camelCase  |PascalCase |camelCase  |
|Namespace / Package |small_caps |PascalCase |small_caps |
|Propiedades         |camelCase  |PascalCase |camelCase  |
|Parámetro           |camelCase  |camelCase  |camelCase  |
|Variable local      |camelCase  |camelCase  |camelCase  |
|Interface           |PascalCase |PascalCase |PascalCase |

## Convención de Nombres
La convención de nombres es un conjunto de normas y reglas para la escritura de nombres, código fuente, identificadores y comentarios dentro de la programación, que facilitan y hacen más comprensible su lectura.

### 1. Clases
 
Las clases representan “cosas” y no “acciones”, por tal motivo evitar verbos como nombre de clase.

El nombre de la clase debe estar en singular, salvo que la clase represente multiplicidad de cosas.

Las Nombres de las clases deberían ser Sustantivos: ejemplo *carro, hombre, tienda, pais, empleado, proveedor*
Cada clase debe tener un bloque de documentación según la norma del lenguaje.

En PHP
```php
/**
*  Bloque de Documentación
*/
class SampleClass
{
//contenido de la clase
}
```


En C#
```csharp
///
/// Bloque de Documentación
///
public class SampleClass
{
//contenido de clase
}
```

En Java
```java
/**
*  Bloque de Documentación
*/
public class SampleClass
{
//contenido de la clase
}
```

### 2. Métodos

Los nombres de los métodos deberían ser un verbo, dado que describe una acción ; ejemplo **remover(), enviar(), cargar()**

Los Métodos dentro de las clases siempre debe declarar su visibilidad tales como **privadas, protegidas, públicas, etc**

### 3. Variables

Evitar variables que sean de un solo carácter, Los nombres comunes para las variables temporales son **i, j, k, m, y n** para los números enteros; **c, d, y e** para los caracteres.
Nombres de variables sólo pueden contener caracteres alfanuméricos
Nombres de variables deben ser camelCase

### 4. Constantes 
Según el tipo de lenguaje tenemos algunos ejemplos

|PHP            |C#            |Java           |
|---------------|--------------|---------------|
|MIN_WIDTH      |LocalConstant |MIN_WIDTH      |
|LOCAL_CONSTANT |MinWidth      |LOCAL_CONSTANT |
|COLUMNS        |Colums        |COLUMNS        |