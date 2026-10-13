---
sidebar_position: 1
---

# Análisis de requisitos

## Descripción del sistema

GameShelf es una aplicación de gestión de videojuegos. El usuario podrá mantener una colección personal de juegos y consultar su información de forma organizada.

Cada videojuego tendrá los siguientes datos:

- Identificador único.
- Título.
- Plataforma.
- Género.
- Año de lanzamiento.
- Estado.
- Valoración personal.

Los estados posibles de un videojuego serán:

- Pendiente.
- Jugando.
- Completado.
- Abandonado.

## Requisitos funcionales

| Código | Requisito |
|---|---|
| RF01 | El sistema debe permitir añadir un videojuego a la colección |
| RF02 | El sistema debe mostrar todos los videojuegos registrados |
| RF03 | El sistema debe buscar videojuegos por título |
| RF04 | El sistema debe modificar los datos de un videojuego existente |
| RF05 | El sistema debe eliminar un videojuego de la colección |
| RF06 | El sistema debe permitir cambiar el estado de un videojuego |
| RF07 | El sistema debe mostrar la valoración de cada videojuego |

## Requisitos no funcionales

| Código | Requisito |
|---|---|
| RNF01 | La aplicación debe tener una interfaz clara y sencilla |
| RNF02 | Los datos introducidos deben validarse antes de guardarse |
| RNF03 | El título de un videojuego no puede estar vacío |
| RNF04 | La valoración debe estar comprendida entre 0 y 10 |
| RNF05 | La aplicación debe permitir consultar la colección de forma rápida |
| RNF06 | El código debe estar organizado en clases y métodos reutilizables |

## Caso de uso: añadir videojuego

**Actor principal:** Usuario.

**Descripción:** El usuario registra un videojuego nuevo en su colección.

**Flujo principal:**

1. El usuario selecciona la opción para añadir un videojuego.
2. El sistema solicita los datos del juego.
3. El usuario introduce el título, plataforma, género, año, estado y valoración.
4. El sistema valida los datos introducidos.
5. El sistema guarda el videojuego en la colección.
6. El sistema muestra un mensaje de confirmación.

## Reglas de negocio

- No se puede añadir un videojuego sin título.
- El año de lanzamiento debe ser un número válido.
- La valoración debe estar entre 0 y 10.
- Cada videojuego debe tener un identificador único.
- Solo se puede modificar o eliminar un videojuego que exista en la colección.