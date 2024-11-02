## Actores

### Actores Primarios:
- Vehículo
- Cámaras

### Actores Secundarios:
- API
- Base de datos
- Impresora
- Correo electrónico

## Precondiciones:
Tanto las cámaras, base de datos, API y impresoras deben estar funcionando previamente.

## Camino básico:
1. La cámara detecta el paso del vehículo y registra los datos correspondientes.
2. La cámara envía los datos registrados al sistema.
3. El sistema evalúa los datos recibidos por la cámara y realiza diferentes acciones de acuerdo a esos datos.

## Caminos Alternativos:
- Si la velocidad enviada por la cámara es >70km/h y <100km/h:
  - Envía los datos a una API para luego guardarlos en una base de datos.
  - Envía un correo con los datos a la cuenta de correo electrónico específica.
  
- Si la velocidad recibida de la cámara es >100km/h:
  - Envía los datos a una API para luego guardarlos en una base de datos.
  - Envía un correo con los datos a la cuenta de correo electrónico específica.
  - Envía 3 veces los datos a una impresora para ser impresos.

## Escenario de éxito:
- El sistema concreta eficientemente la multa del vehículo y, dependiendo de la condición de la multa, el sistema va a imprimir esos datos registrados en una impresora o no.

## Escenario de fracaso:
- El sistema no puede finalizar o realizar la multa correctamente debido a algún error inesperado al cargar los datos a una API.
- La impresora falla al recibir o intentar imprimir los datos recibidos desde el sistema debido a problemas técnicos.
- El sistema no puede conectar o enviar los datos desde la API a la base de datos debido a algún error inesperado o desconocido.

