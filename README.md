# FUNCIONES  STRING Oracle
####Funciones Interna que nos permiten hacer el manejo de stringo cadena de caracteres al momento de manipular datos utilizando el lenguaje de sql
#### Las funciones de manejo de caracteres alfa numerico que nos facilita oracle aceptan argumento de tipo caracter y retornan caracteres o valores numericos.

>La tabla dual es una tabla especial q contiene una sola columana, esta presenta en toda las bd de oracle y se utiliza para seleccionar una especie de pseudo-columna de tipo varchar, con el nombre de DUMMY y contienen siempre un registro por defecto que es la letra 'x'

>Consultar numero de caracter dentro del codigo ASCII
```sql
select chr(65) from dual;
--dice el caracter que tiene ese numero
```
|CHR(65)|
|-------:|
|A|

```sql
--dice que numero tiene ese caracter
select ascii('A') from dual;
```
|ASCII('A')|
|-------:|
|65|
___

> Funcion concat: sirve para unir cadenas de carácteres
```sql
select concat('buenas','tardes') from dual;
```
|CONCAT('BUENAS','TARDES')|
|-------:|
|buenas tardes|

___

> Funcion initcap: coloca primera letra en mayúscula de cada palabra que se coloque dentro de una sentencia

```SQL
select initcap('buenas tardes') from dual;
```
|INITCAP('BUENASTARDES')|
|-------:|
|Buenas Tardes|

___

> funcion lower: coloca todas las letras en minúscula
```sql
select lower('BUENAS TARDES') from dual;
```
|LOWER('BUENASTARDES')|
|-------:|
|buenas tardes|

___
































