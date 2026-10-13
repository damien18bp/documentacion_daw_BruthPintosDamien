---
sidebar_position: 1
---

# Estructura del proyecto

## Organización lógica

El proyecto GameShelf puede organizarse siguiendo una estructura sencilla basada en el patrón MVC.

```text
gameshelf/
├── src/
│   ├── model/
│   │   └── Videojuego.java
│   ├── controller/
│   │   └── ColeccionVideojuegos.java
│   ├── view/
│   │   └── MenuConsola.java
│   └── app/
│       └── Main.java
├── docs/
├── README.md
└── pom.xml
```

## Descripción de las carpetas

| Carpeta o archivo | Descripción |
|---|---|
| `model/` | Contiene las clases que representan los datos del programa |
| `controller/` | Contiene la lógica de negocio y la gestión de la colección |
| `view/` | Contiene la interacción con el usuario, por ejemplo un menú de consola |
| `app/` | Contiene la clase principal que inicia la aplicación |
| `docs/` | Contiene la documentación técnica creada con Docusaurus |
| `README.md` | Explica de forma breve el objetivo del repositorio |
| `pom.xml` | Archivo de configuración de dependencias si se utiliza Maven |

## Flujo de la aplicación

1. La clase `Main` inicia el programa.
2. Se crea una instancia de `ColeccionVideojuegos`.
3. El usuario utiliza un menú para seleccionar una operación.
4. La vista recoge los datos introducidos.
5. El controlador valida y procesa la operación.
6. Los objetos `Videojuego` se añaden, modifican, buscan o eliminan.
7. La aplicación muestra el resultado al usuario.

## Ejemplo de uso

Un usuario añade el videojuego *The Binding of Isaac* con los siguientes datos:

```text
Título: The Binding of Isaac
Plataforma: PC
Género: Roguelike
Año: 2011
Estado: Completado
Valoración: 9
```

La aplicación crea un objeto `Videojuego` y lo guarda en la lista gestionada por `ColeccionVideojuegos`.