# API REST de Gestión de Envíos

Proyecto desarrollado como parte del Taller de Integración de Sistemas. Esta API implementa un servicio REST para gestionar envíos utilizando Apache Camel y documentado con OpenAPI 3.0.

## Descripción

La API permite realizar operaciones básicas para la gestión de envíos:

- Consultar todos los envíos.
- Consultar un envío por su ID.
- Registrar un nuevo envío.

## Endpoints

| Método | Ruta | Descripción |
|--------|------|-------------|
| GET | `/api/envios` | Listar todos los envíos |
| GET | `/api/envios/{id}` | Consultar un envío por ID |
| POST | `/api/envios` | Registrar un nuevo envío |
| GET | `/api/api-doc` | Documentación OpenAPI/Swagger |

## Tecnologías Utilizadas

- Java 17+
- Apache Maven 3.9+
- Apache Camel 4.x
- Netty HTTP Server
- OpenAPI 3.0
- Postman para pruebas

## Instalación y Ejecución

### Clonar el repositorio

```bash
git clone https://github.com/USUARIO/api-rest-lab.git
cd api-rest-lab
```

### Compilar el proyecto

```bash
mvn clean package
```

### Ejecutar la aplicación

```bash
mvn exec:java -Dexec.mainClass="edu.udla.isw.App"
```

La API estará disponible en:

```
http://localhost:8080/api
```

## Documentación de la API

Documentación OpenAPI disponible en:

```
http://localhost:8080/api/api-doc
```

Archivo OpenAPI:

```
src/main/resources/openapi.yaml
```

## Pruebas con Postman

Ejemplos de pruebas:

### GET /envios

Devuelve la lista de envíos registrados.

### GET /envios/{id}

```bash
GET http://localhost:8080/api/envios/001
```

### POST /envios

Body en formato JSON:

```json
{
  "id": "002",
  "destinatario": "Maria Lopez",
  "direccion": "Av. Central 123",
  "estado": "Registrado"
}
```

## Evidencias

- Capturas de ejecución de terminal
- Capturas de pruebas en Postman

## Autor

Institución: UDLA  
Curso: Integración de Sistemas  
Año: 2025

## Reflexión

Una API REST bien diseñada proporciona un medio estándar, escalable y desacoplado para integrar sistemas, facilitando la comunicación mediante protocolos abiertos como HTTP y formatos estructurados como JSON. Esto permite construir arquitecturas modulares y mantener la interoperabilidad entre aplicaciones desarrolladas en diferentes tecnologías.
