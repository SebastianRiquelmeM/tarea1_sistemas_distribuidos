# Tarea 1 cache y gRPC

## Imágenes utilizadas

Base de datos: 
```bash
mariadb:10.3.9
```
Redis:
```bash
bitnami/redis:6.2.6
```

## Requisitos

- docker-compose

Opcional para la terminal interactiva:
- NodeJS

## Instalación

1- Lanzar docker-compose

Dejar cargar esto, pues cargará el archivo .sql en la db en el primer inicio, lo cual toma tiempo.

```bash
docker-compose up --build
```

Una vez termine de cargar los datos, volver a ejecutar docker compose, para que asi nodejs tenga los datos para funcionar. (La base de datos se guarda dentro del directorio ./docker)

```bash
docker-compose up --build
```

## Uso

### Terminal interactiva

Para ejecutar la terminal interactiva se necesita nodejs en el pc cliente. 

1- Instalar dependencias

En el directorio ./client usar:

```bash
npm i
```
Luego en el directorio ./client/src ejecutar:
```bash
node basic_example.js
```
### curl terminal

En una terminal linux, usar:

```bash
curl -X POST http://localhost:3000/keyword -H 'Content-Type: application/json' -d '{"keyword": "Palabra a buscar"}'
```