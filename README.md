# Documentación del Código de Carrusel

## Descripción

Este código implementa un carrusel simple que permite desplazarse hacia la derecha o hacia la izquierda mediante los botones de navegación "Siguiente" y "Anterior". Cada clic en los botones desplaza el carrusel hacia la derecha o hacia la izquierda, mostrando un conjunto específico de elementos HTML.

## Funcionamiento

### Variables

- `click`: Variable que lleva un seguimiento del número de clics en los botones de navegación.

### Función `ScrolTo(viewElm, margin, moveTo)`

Esta función se encarga de desplazar el carrusel y actualizar la posición actual basándose en los parámetros proporcionados.

- `viewElm`: Número de elementos visibles en el carrusel.
- `margin`: Margen entre elementos.
- `moveTo`: Dirección del movimiento, puede ser "right" (derecha) o "left" (izquierda).

### Acciones

- Se obtienen todos los elementos HTML con la clase "item".
- Se determina el elemento actual basándose en el número de clics.
- Cuando se hace clic en el botón "Siguiente" (`btnNext`), se desplaza el carrusel hacia la derecha, y se actualiza la posición actual. Si alcanza el final, vuelve al principio.
- Cuando se hace clic en el botón "Anterior" (`btnPrev`), se desplaza el carrusel hacia la izquierda, y se actualiza la posición actual. Si alcanza el inicio, vuelve al final.

## Uso

```javascript
// Ejemplo de uso
let click = 0;
let isScrolling = false;

btnNext.addEventListener("click", () => {
  ScrolTo(3, 15, "right");
});

btnPrev.addEventListener("click", () => {
  ScrolTo(3, 15, "left");
});
```

```html
<!-- Estructura HTML-->
<div class="container">
  <button class="next"></button>
  <div class="carrousel">
    <div class="item">Tú contenido</div>
    <div class="item">Tú contenido</div>
    <div class="item">Tú contenido</div>
    <div class="item">Tú contenido</div>
  </div>
  <button class="prev"></button>
</div>
```
