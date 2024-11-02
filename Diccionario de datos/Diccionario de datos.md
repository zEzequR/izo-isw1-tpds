## Diccionario de Datos

### Cámara
- **Estructura**: `1{@id + desc + ubi + dirIP + modelo}x`

### Ubi
- **Estructura**: `coordenadax + coordenaday`

### Registro
- **Estructura**: `fecha + @id + patente + velocidad`

| Nombre        | Descripción                                           | Tipo    | Longitud | Dominio   |
|---------------|-------------------------------------------------------|---------|----------|-----------|
| Patente       | Detalla la patente del auto                            | String  | 7        | Continuo  |
| Velocidad     | Detalla la velocidad del auto                          | Float   | 10       | Continuo  |
| Coordenadax   | Coordenadas X de la ubicación del paso del auto       | String  | 100      | Continuo  |
| Coordenaday   | Coordenadas Y de la ubicación del paso del auto       | String  | 100      | Continuo  |
| Desc          | Detalla alguna cosa en particular al registrar el paso el vehículo | String  | 900      | Continuo  |
| ID            | Identificador único de la cámara                       | Integer | 20       | 0-9       |
| DirIP         | Dirección IP de la cámara                             | String  | 16       | 0-9       |
| Modelo        | Modelo de la cámara                                   | String  | 800      | Continuo  |
| Fecha         | Detalla la fecha al registrar el paso del vehículo.   | Date    | -        | -         |


