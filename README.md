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
|:-------:|
|A|

```sql
--dice que numero tiene ese caracter
select ascii('A') from dual;
```
|ASCII('A')|
|:-------:|
|65|
___

> Funcion concat: sirve para unir cadenas de carácteres
```sql
select concat('buenas','tardes') from dual;
```
|CONCAT('BUENAS','TARDES')|
|:-------:|
|buenas tardes|

___

> Funcion initcap: coloca primera letra en mayúscula de cada palabra que se coloque dentro de una sentencia

```SQL
select initcap('buenas tardes') from dual;
```
|INITCAP('BUENASTARDES')|
|:-------:|
|Buenas Tardes|

___

> funcion lower: coloca todas las letras en minúscula
```sql
select lower('BUENAS TARDES') from dual;
```
|LOWER('BUENASTARDES')|
|:-------:|
|buenas tardes|

___

> funcion upper: coloca todas las letras en mayúscula
```sql
select upper('buenas tardes') from dual;
```
|UPPER('BUENASTARDES')|
|:-------:|
|BUENAS TARDES|

___

> funcion lpad: agrega caracteres al lado izquierdo de los caracteres colocado entre parentesis dentro de la ejecucion


```sql
select lpad('oracle',11,'abc') from dual;
```
|LPAD('ORACLE',11,'ABC')|
|:-------:|
|abcaboracle|
#####el sistema agrega el abc pero como no llega a los 11 caracteres agrega el ab

___

>--funcion rpad: completa los carácteres del lado derecho con la cantidad que le indiquen

```sql
select rpad('oracle',12,'abc') from dual;
```
|RPAD('ORACLE',11,'ABC')|
|:-------:|
|oracleabcab|
##### el sistema utiliza el abc para completar los caracteres.

___
> funcion ltrim: corta del lado izquiero los carácteres que le indiquen
``` sql
select ltrim('curso de oracle','cur')from dual;
```
|LTRIM('CURSODEORACLE'CUR')|
|:-------:|
|so de oracle|
##### el sistema corta del lado izquierdo de los caracteres lo que diga 'cur', esto solo funcion solo si los caracteres coinciden, y si colocamos 'curso de oracle' nos borrara todo y mostrara null.

___

> funcion rtrim: corta del lado derecho los carácteres que le indiquen
``` sql
select rtrim('curso de oracle','cle')from dual;
```
|RTRIM('CURSODEORACLE'CUR')|
|:-------:|
|curso de ora|

___

>funcion trim : sirve para eliminar espacios en blanco dentro de una linea de caracteres.
``` sql
select trim('  oracle  ') from dual;
```
|TRIM('CURSODEORACLE'CUR')|
|:-------:|
|oracle|

##### tambien funciona con rtrim y ltrim nos cortaria todo los espacios en blanco

___

>funcion replace: reemplaza la letra indicada con la que se requiera

```sql
select replace('www.oracle.com','o','a') from dual;
```
|REPLACE('CURSODEORACLE'CUR')|
|:-------:|
|www.aracle.cam|

___

>--funcion subsstr : devuelve una parte de una cadena especifica q se le coloque como argumento dentro de una ejecucion, empezando desde la posicion que se le indique del argumento con tantos caracteres de longitud como querramos saberlo

```sql
select substr ('www.oracle.com', 1,10) from dual; --de izquierda a dercha
```
|SUBSTR('CURSODEORACLE.COM',1,10)|
|:-------:|
|www.oracle|

```sql
select substr ('www.oracle.com', -14) from dual; -- de derecha a izquierda
```
|SUBSTR('CURSODEORACLE.COM',-3)|
|:-------:|
|com|

___

> funcion length: nos retorna la cantidad total de caracteres q contenga un string

```sql
select length('www.oracle.com') as cantidad from dual;
```
|CANTIDAD|
|:-------:|
|14|

___

> funcion instr: Nos dice donde se encuentra o seccion de caracteres especifica dentro de una palabra o frase que le pasemos en una ejecucion

```sql
select instr('curso de oracle sql','curso') from dual;
```
|INSTR('CURSODEORACLESQL','CURSO')|
|:-------:|
|1|
##### Lo que el sistema hace es buscar la palabra desde donde concuerda y nos mostrara desde q posicion  concuerda

> funcion translate : nos ayuda a sustituir letras o caracteres dentro de una cadena de caracteres que le pasemos en una ejecucion con otras letras especificadas como tercer parametro dentro de la misma ejecucion
```sql
select translate('CURSO DE ORACLE','AOE', 'XYZ') from dual;
```
|TRANSLATE('CURSODEORACLESQL','OAE','XYZ')|
|:-------:|
|CURSY DZ YRXCLZ|

##### la 'o' sera remplazada por la 'x', 'a' por la 'y' , la 'e' por la 'z'













