# Galería Python + NumPy + Pyodide

## Estructura
- `index.html`: catálogo principal.
- `dibujos/flower/index.html`: página que ejecuta la animación Flower.
- `dibujos/flower/flower.py`: código Python de Flower.

## Cómo funciona Flower
La página carga `./flower.py` desde su misma carpeta mediante Pyodide 0.27.7, carga NumPy y ejecuta el código. El archivo define `frame(t)`, que devuelve un buffer RGBA de 720 × 1280 para dibujarlo en Canvas.

## Publicación
Sube el contenido de esta carpeta al repositorio de GitHub Pages respetando los nombres y las rutas.

## Agregar otro dibujo
1. Crea `dibujos/nombre/`.
2. Copia el `index.html` de `dibujos/flower/` y cambia el nombre del archivo que carga.
3. Coloca el Python adaptado en esa carpeta.
4. Agrega una tarjeta con el enlace correspondiente en el `index.html` principal.

Cada archivo Python debe exponer `frame(t)` y devolver píxeles RGBA compatibles con el tamaño de su Canvas.
