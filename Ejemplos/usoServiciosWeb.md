##  Usos de los servicios web 



Los servicios web pueden ser utilizados para facilitar la obtención y usos de ciertos servicios por internet  como inicios de sesión,  solicitudes de datos, obtención de tickets, etc. 

En este ejemplo veremos cómo funciona un webservice que convierte medidas de temperatura Farenheit a Celsius. El primer bloque es la petición desde el cliente de la conversión de los datos y el segundo, la respuesta del servidor. 



```
POST /xml/tempconvert.asmx HTTP/1.1
Host: www.w3schools.com
Content-Type: application/soap+xml; charset=utf-8
Content-Length: length

<?xml version="1.0" encoding="utf-8"?>
<soap12:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap12="http://www.w3.org/2003/05/soap-envelope">
  <soap12:Body>
    <CelsiusToFahrenheit xmlns="https://www.w3schools.com/xml/">
      <Celsius>string</Celsius>
    </CelsiusToFahrenheit>
  </soap12:Body>
</soap12:Envelope>
```



Como ves, utilizamos una petición HTTP al servidor de la web de w3schools, que nos proporcionará el servicio de conversión. 

En el apartado content-type especificamos que  queremos recibir una aplicación en XML utilizando SOAP y que se deben codificar los datos en utf-8

En el siguiente paso tenemos un bloque XML donde presentamos los placeholders a utilizar para introducir los valores que irán en cada petición al servicio web. 

En el siguiente bloque de código se ve una respuesta típica del servidor: 



```
HTTP/1.1 200 OK
Content-Type: application/soap+xml; charset=utf-8
Content-Length: length

<?xml version="1.0" encoding="utf-8"?>
<soap12:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:soap12="http://www.w3.org/2003/05/soap-envelope">
  <soap12:Body>
    <CelsiusToFahrenheitResponse xmlns="https://www.w3schools.com/xml/">
      <CelsiusToFahrenheitResult>string</CelsiusToFahrenheitResult>
    </CelsiusToFahrenheitResponse>
  </soap12:Body>
</soap12:Envelope>
```