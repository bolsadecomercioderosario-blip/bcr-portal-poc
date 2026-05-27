# Instrucciones de deploy — Portal de búsqueda BCR

## Para la persona

Este es el material de una prueba de concepto que vas a mostrar a tus jefes.
Abrí la pestaña **Code** en Claude, arrastrá esta carpeta completa, y pegale
el bloque de texto que está más abajo (la sección "PEDIDO PARA CLAUDE CODE").

## Qué hay en esta carpeta

- `index.html` — la página: una home con un buscador inteligente para la BCR
- `assets/logo-bcr.png` — logo oficial BCR (versión blanca)
- `assets/hero-desktop.jpg` — foto del edificio, fondo para pantallas grandes
- `assets/hero-mobile.jpg` — foto del edificio, fondo para celular

Es un sitio estático puro: HTML + CSS + JS. No tiene backend, no necesita
build, no usa base de datos. Se sirve tal cual.

## Qué hace la página

Es una home alternativa para la Bolsa de Comercio de Rosario. Tiene un campo
de búsqueda donde el usuario escribe en lenguaje natural ("precio de la soja",
"turno para el puerto", "informe semanal") y lo redirige a la sección
correspondiente del sitio bcr.com.ar. También tiene un botón que lleva a la
página institucional de Shorthand. El buscador funciona por coincidencia de
palabras clave (no usa IA todavía — eso es una fase posterior).

---

## PEDIDO PARA CLAUDE CODE

Copiá y pegá esto en la pestaña Code:

> Tengo una carpeta con un sitio estático (un index.html y una carpeta assets
> con imágenes). Es una prueba de concepto que necesito desplegar en Render
> como Static Site para mostrarla. No tiene build ni backend, se sirve tal cual.
>
> Necesito que me ayudes a:
> 1. Inicializar un repositorio git en esta carpeta si no lo tiene.
> 2. Crear un repo en GitHub y subir estos archivos.
> 3. Guiarme para conectar ese repo a Render como Static Site
>    (publish directory = raíz, sin build command).
>
> Antes de hacer cada paso que cree recursos o suba algo, mostrame qué vas a
> hacer y esperá mi confirmación. No quiero que despliegues nada a producción
> sin que yo lo apruebe explícitamente.

---

## Notas importantes

- **Revisá la página antes de desplegar.** Abrí el `index.html` localmente
  y probá el buscador.
- **El sello "Prueba de concepto"** arriba a la derecha es a propósito, para
  la presentación. Cuando el proyecto se apruebe, se puede sacar (es un
  `<div class="demo">` en el HTML).
- **El buscador es por palabras clave, no IA.** Al presentarlo, conviene
  decir "ya funciona, y con IA entiende cualquier frase" — sin afirmar que
  ya es IA.
- **El mapa de destinos** (qué búsqueda lleva a qué URL) está al final del
  `index.html`, en la lista `DESTINOS`. Es texto plano, fácil de editar.
- Cuando GA empiece a registrar las búsquedas internas del sitio (la medición
  que se activó), esos términos reales sirven para afinar el buscador.
