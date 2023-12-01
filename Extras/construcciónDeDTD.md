## DTD reglas de combinación: 

**<!ELEMENT person ( name ,email )>** 

Coma --> A,B: varios elementos, en el orden en que aparecen escritos

**<!ELEMENT person ( name ,email? )>**

Interrogante --> (A?): el elemento puede o no aparecer

**<!ELEMENT person ( name ,email+ )>**

Sumatorio --> (A+): el elemento debe aparecer al menos una vez

**<!ELEMENT person ( name ,email* )>**

Asterisco --> (A*): el elemento puede aparecer 0, 1 ó varias veces 

**<!ELEMENT person ( email | teléfono )>**

Barra --> (A | B): puedes aparecer uno u otro elemento

**<!ELEMENT person ( email | fax | teléfono)*>**

Paréntesis --> El paréntesis te permite aplicar reglas a un grupo de elementos completo

## DTD secciones extra para definir elementos: 

**<!ELEMENT title (#PCDATA)>**

#PCDATA ( Parsed Character Data ) - para elementos 

Implican que el elemento será tratado como una string o grupo
de caracteres y que no deben contener ni & ni <> ni otro tipo de elementos
semejantes. Para ellos usaremos las entidades. 

**<!ELEMENT person ANY>**

ANY permite usar subelementos sin especificarel tipo y datos de caracteres
en combinación. Se recomienda usarlo sólo en fases de desarrollo para 
mantener una buena consistencia en los datos a transmitir. 

**<!ELEMENT br EMPTY>**

Se utiliza para especificar que el elemento no tendrá contenido dentro. 


## DTD tipos de atributos: 

**<!ATTLIST person first_name CDATA #REQUIRED>**

CDATA - Character Data : el atributo sólo contendrá texto

'<!ENTITY % stamp '
   id ID #IMPLIED
   creation-day NMTOKEN #IMPLIED
   .......
   mod-by NMTOKEN #IMPLIED
   version NMTOKEN #IMPLIED
   status (draft|final|obsolete) #IMPLIED
   approval (ok|not-ok|so-so) #IMPLIED
   main-author CDATA #IMPLIED
   '>'

NMTOKEN - el atributo será una palabra sin espacios ni puntuaciones
ID - el atributo será un identificador único del elemento.

**<!ATTLIST Person Pin ID #REQUIRED>**
**<!ATTLIST Person Friend IDREF #IMPLIED>**
**<!ATTLIST Person Likes IDREFS #IMPLIED>**

IDREF -  el atributo referenciará a un identificador (ID)
IDREFS - el atributo referenciará a uno o más identificadores

**<!ATTLIST person gender (male|female) #IMPLIED>**

(A|B|C|...) - El atributo tendrá una lista de valores entre los que
el usuario debe elegir 

## DTD keywords sobre el valor de los atributos: 

'<!ATTLIST person id ID #REQUIRED>
<person id="N1004">'

#REQUIRED --> es obligatorio añadir un valor al atributo

'<!ATTLIST person gender (male|female) #IMPLIED>
<person gender="male">'

#IMPLIED --> el atributo es opcional

'<!ATTLIST form method CDATA #FIXED "POST">
<form method="POST">'

#FIXED --> el atributo tiene un valor previamente fijado

## DTD entidades: 

Las entidades son fragmentos reusables que pueden ser sustituidos en el DTD
o en el XML. 

XML por defecto tiene 5 entidades predefinidas: 

&lt; para < 
&gt; para >
&amp; para &
&quot; para "
&apos; para ' 

<!ENTITY copyright "&#xA9;">

 &#xA9; es el código para el símbolo de copyright