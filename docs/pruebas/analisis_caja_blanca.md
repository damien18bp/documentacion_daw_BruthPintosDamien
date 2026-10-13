---
sidebar_position: 1
---

# Análisis de caja blanca

## Objetivo

Las pruebas de caja blanca permiten comprobar el comportamiento interno de los métodos del programa. En este proyecto se analizará el método encargado de añadir videojuegos a la colección.

## Método analizado

El siguiente pseudocódigo representa la lógica del método `agregarVideojuego`:

```java
public boolean agregarVideojuego(Videojuego videojuego) {
    if (videojuego == null) {
        return false;
    }

    if (videojuego.getTitulo() == null || videojuego.getTitulo().isBlank()) {
        return false;
    }

    if (videojuego.getValoracion() < 0 || videojuego.getValoracion() > 10) {
        return false;
    }

    videojuegos.add(videojuego);
    return true;
}
```

## Decisiones del método

El método contiene tres decisiones:

| Decisión | Condición | Resultado si es verdadera |
|---|---|---|
| D1 | El videojuego es nulo | Devuelve `false` |
| D2 | El título es nulo o está vacío | Devuelve `false` |
| D3 | La valoración es menor que 0 o mayor que 10 | Devuelve `false` |

Si ninguna condición se cumple, el videojuego se añade a la lista y el método devuelve `true`.

## Casos de prueba

| Prueba | Videojuego | Título | Valoración | Resultado esperado |
|---|---|---|---:|---|
| CP01 | `null` | No aplica | No aplica | `false` |
| CP02 | Objeto válido | Vacío | 8 | `false` |
| CP03 | Objeto válido | Hollow Knight | -1 | `false` |
| CP04 | Objeto válido | Hollow Knight | 11 | `false` |
| CP05 | Objeto válido | Hollow Knight | 9 | `true` |

## Caminos independientes

Los caminos principales que se deben probar son los siguientes:

1. El objeto recibido es `null`.
2. El objeto existe, pero el título no es válido.
3. El objeto y el título son válidos, pero la valoración es menor que 0.
4. El objeto y el título son válidos, pero la valoración es mayor que 10.
5. Todos los datos son válidos y el videojuego se añade correctamente.

Con estos casos se recorren todas las condiciones y todas las salidas posibles del método.