# Implementación de la clase Queue en el juego de la serpiente

## Descripción
En el código se implementó una clase `Queue` con sus métodos básicos. Los métodos incluidos son:

- **enqueue**: Agrega un elemento a la cola.
- **dequeue**: Remueve el primer elemento de la cola.
- **toArray**: Convierte la cola en un array, facilitando el dibujo de la serpiente dentro del juego.
- **size**: Devuelve la longitud de la serpiente.
- **peek**: Permite ver la cabeza sin modificar la cola de la serpiente.

## Cambios realizados

- Se modificó el array que inicializaba la serpiente, ahora usamos:
  ```java
  snake = new Queue();
  ```
  Además, agregamos la cabeza inicial con:
  ```java
  snake.enqueue();
  ```

## Movimiento de la serpiente

Para el movimiento de la serpiente:
- Usamos `snake.peek()` para obtener la posición de la cabeza.
- En lugar de `snake.pop()` para remover la cola, usamos `snake.dequeue()`.

## Dibujo y colisiones

Para manejar el dibujo y las colisiones de la serpiente:
- Se usa `snake.toArray()` para convertir la cola en un array temporal y así poder dibujar todos los segmentos correctamente.

## Puntuación y tamaño de la serpiente

- Para obtener el tamaño de la serpiente, usamos `snake.size()` en lugar de `snake.length`.
