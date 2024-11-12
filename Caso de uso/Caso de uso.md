**Actores Primarios:**

* Cámaras

**Actores Secundarios:**

* API

**Precondiciones:** 

* Tanto las cámaras como la API deben estar funcionando 24/7

**Camino básico:**

* La cámara detecta el paso del vehículo y registra los datos del vehículo (fecha y hora, id de la cámara, patente y velocidad)  
* La cámara envía los datos registrados al sistema  
* El sistema evalúa los datos recibidos por la cámara y realiza diferentes acciones de acuerdo a esos datos.

**Caminos Alternativos:**

1. Si la velocidad envíada por la cámara es \>=70km/h y \<= 100km/h:  
   1. Envía los datos a una API para luego guardarlos en una base de datos  
   2. Envía un correo con los datos a la cuenta de correo electrónico específico  
2. Si la velocidad recibida de la cámara es \> 100km/h:  
   1. Envía los datos a una API para luego guardarlos en una base de datos  
   2. Envía un correo con los datos a la cuenta de correo electrónico específico  
   3. Envía 3 veces los datos a una impresora para ser impresos

**Escenario de éxito:**

* El sistema concreta eficientemente la multa del vehículo y dependiendo de la condición de la multa, el sistema va a imprimir esos datos registrados en una impresora o no.

	  
**Escenario de fracaso:**

* El sistema no puede finalizar o realizar la multa correctamente debido a algún error inesperado al cargar los datos a una API  
* La impresora falla al recibir o intentar imprimir los datos recibidos desde el sistema debido a problemas técnicos.  
* El sistema no puede conectar o envíar los datos desde la API a la base de datos debido algún error inesperado o desconocido  
* La cámara/s dejan de funcionar, evitando que se registren los vehículos.

	