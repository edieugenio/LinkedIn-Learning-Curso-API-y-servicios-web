## JSON vs XML

### XML

```
<pacientes>
  <paciente>
    <nombre>Juan</nombre> <apellido>Quenovi</apellido>
  </paciente>
  <paciente>
    <nombre>Mark</nombre> <apellido>Weider</apellido>
  </paciente>
  <paciente>
    <nombre>Artu</nombre> <apellido>Rito</apellido>
  </paciente>
</pacientes>
```


### JSON

```
{"pacientes": [
	{ "nombre": "Juan", "apellido": "Quenovi"},
	{ "nombre": "Mark", "apellido": "Weider"},
	{ "nombre": "Artu", "apellido": "Rito"}
]}
```

Como puedes ver, JSON y XML tienen varias similitudes y diferencias. 

Ambos son "auto-descriptivos", lo que quiere decir es que son fácilmente legibles para humanos. 

Asimismo, ambos son jerárquicos, es decir, hay valores contenidos dentro de otros en una jerarquía concreta. 

Por otro lado, tanto JSON como XML pueden ser parseados por muchos lenguajes de programación, y ambos pueden ser obtenidos con un XMLHttpRequest. 

Los objetos JSON tienen tipo de datos mientras que en XML los datos no tienen tipo porque todos deben ser Strings o cadenas de caracteres. 

Normalmente JSON se puede utilizar en la mayoría de navegadores mientras que el parsing de XML para ser soportado en varios navegadores puede ser complicado. 

Sin embargo, así como JSON no tiene capacidad para presentar sus datos, XML ofrece no sólo la posibilidad, sino también el soporte CSS para formatear los datos para su mejor presentación. 

Por otro lado, en JSON es más fácil que en XML obtener datos, tiene soporte en la mayoría de herramientas AJAX y soporte nativo de objetos. En XML los objetos deben ser convertidos a elementos con atributos. 

Al margen de esto, los archivos JSON son mucho más fáciles de leer que los XML aunque, a cambio, es menos seguro que XML.