<div align="center">

<img src="icons/icon-192.png" alt="Icono de Rincón Rosa" width="96" height="96">

# Rincón Rosa

**Tu ruleta y tus números de la suerte, en una app cozy de color rosa pastel.**

[![Demo en vivo](https://img.shields.io/badge/demo-GitHub%20Pages-F29DB5?style=for-the-badge)](https://francisykza.github.io/rincon-rosa/)
![PWA](https://img.shields.io/badge/PWA-instalable-D2668A?style=for-the-badge)
![Sin dependencias](https://img.shields.io/badge/dependencias-0-E6CBEA?style=for-the-badge)
[![Licencia MIT](https://img.shields.io/badge/licencia-MIT-FDD5C2?style=for-the-badge)](LICENSE)

<img src="docs/ruleta.jpg" alt="Pantalla de la ruleta" width="760">

</div>

## ¿Qué es?

Rincón Rosa es una pequeña aplicación web para decidir cosas al azar sin complicarse: qué leer, qué cenar, qué plan hacer el domingo… o sacar números aleatorios para un dado, un sorteo o la lotería.

Se instala en el móvil como una app más (con su icono y a pantalla completa) y funciona **sin conexión**.

## Funciones

### Ruleta
- Varias ruletas guardadas, cada una con su nombre.
- Añade, edita o quita opciones; pega varias a la vez separándolas con comas.
- Giro con animación, sonido de clic y lluvia de corazones al terminar.
- Panel de resultado con *¡Genial!*, *Quitar de la ruleta*, *Mezclar* y *Otra vez*.
- Opción para que la opción ganadora salga de la ruleta (ideal para sorteos sin repetir).
- Historial de los últimos resultados.

### Números
- Elige el rango (desde / hasta), cuántos números quieres, sin repetir y ordenados.
- Atajos: dado, dos dados, 1 al 10, 1 al 100, lotería (6 de 49) y PIN de 4 cifras.
- Bolitas animadas, suma automática y botón para copiar el resultado.
- Historial de las últimas tiradas.
- Números generados con `crypto.getRandomValues` y muestreo por rechazo, para que todos los valores tengan la misma probabilidad.

### General
- Modo claro y modo oscuro automáticos.
- Diseño adaptado a móvil, tablet y ordenador.
- Respeta la preferencia de *movimiento reducido* del sistema.
- Atajo de teclado: barra espaciadora para girar o generar.

<div align="center">
<img src="docs/numeros.jpg" alt="Generador de números" width="560">
<img src="docs/movil.jpg" alt="Vista en el móvil" width="200">
</div>

## Instalarla en el móvil

1. Abre la [demo](https://francisykza.github.io/rincon-rosa/) en el navegador del móvil.
2. **Android (Chrome):** pulsa *Instalar app* o *⋮ → Añadir a pantalla de inicio*.
3. **iPhone (Safari):** botón de compartir → *Añadir a pantalla de inicio*.

## Tecnología

- HTML, CSS y JavaScript sin frameworks ni dependencias ni paso de compilación.
- Ruleta dibujada con `<canvas>`; sonidos generados con la Web Audio API.
- PWA: `manifest.webmanifest` + *service worker* (`sw.js`) para instalarla y usarla sin conexión.
- Datos guardados en `localStorage` del propio dispositivo: no hay servidor ni cuentas, y nada sale de tu navegador.
- Tipografías: [Fredoka](https://fonts.google.com/specimen/Fredoka) y [Nunito](https://fonts.google.com/specimen/Nunito) (Google Fonts).

## Estructura

```
rincon-rosa/
├── index.html            # La app completa (HTML + CSS + JS)
├── manifest.webmanifest  # Nombre, colores e iconos para instalarla
├── sw.js                 # Service worker: funcionamiento sin conexión
├── icons/                # Iconos de la app
└── docs/                 # Capturas para este README
```

## Privacidad

Rincón Rosa no recoge ni envía ningún dato. Tus ruletas e historial se quedan en el almacenamiento local de tu navegador; si borras los datos del sitio, se borran también.

## Licencia

Publicado bajo la [licencia MIT](LICENSE) © 2026 Francisco Muñoz Dorado.
