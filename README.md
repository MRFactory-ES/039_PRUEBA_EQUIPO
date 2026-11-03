# 039_PRUEBA_EQUIPO

Web de práctica para aprender a trabajar en equipo con GitHub en **MRFactory-ES**.
No hace nada útil a propósito: es un tablón con una tarjeta por persona, y cada
tarjeta abre la página de esa persona. Todas las páginas empiezan iguales: son el sitio
donde cada uno hace sus pruebas.

Las páginas están en la carpeta `paginas/`, una por persona: `juan-luis.html`,
`coke.html`, `vero.html`, `justo.html`, `ines.html`, `teresa.html` y `agus.html`.

Para verla, abre `index.html` con doble clic. Funciona igual en Mac y en PC: no hay
que instalar nada.

## La regla

**Nadie sube cambios directamente a `main`.** Todo cambio entra por un *Pull Request*
(una propuesta de cambio) y Coke lo aprueba.

## Cómo cambiar tu página (desde la web de GitHub, sin instalar nada)

1. Entra en el repo en GitHub, abre la carpeta `paginas/` y luego **tu** fichero
   (por ejemplo `vero.html`).
2. Pulsa el lápiz ✏️ (*Edit this file*).
3. Cambia lo que quieras entre las dos marcas ✏️: el título, los textos, la lista.
   Más arriba hay otra marca ✏️ para cambiar tu color.
4. Pulsa **Commit changes…**. Elige *Create a new branch for this commit and start a
   pull request*, ponle un nombre (por ejemplo `vero-mi-pagina`) y confirma.
5. En la pantalla siguiente pulsa **Create pull request**.

Ya está. Coke recibe el aviso, lo revisa y lo acepta (o te pide un cambio en los
comentarios del Pull Request).

## Cómo aprobarlo (Coke)

1. Pestaña **Pull requests** del repo → abre el que haya llegado.
2. Pestaña **Files changed**: ahí se ve en rojo lo que se quita y en verde lo que entra.
3. Si está bien: **Review changes → Approve**, y luego **Merge pull request**.
4. Si no: deja un comentario en la línea y pulsa **Request changes**.

## Ejercicios para practicar

1. **El normal.** Cada uno cambia su página y Coke lo aprueba.
2. **El que se rechaza.** Alguien propone un cambio y Coke pide que lo corrija. El
   autor lo arregla en la misma rama y el Pull Request se actualiza solo.
3. **El choque.** Dos personas cambian a la vez la **misma línea de la misma** página.
   El primero que entra, entra; el segundo verá «This branch has conflicts» y tendrá
   que elegir con qué texto se queda.
4. **El atajo prohibido.** Alguien intenta subir directamente a `main`. Con `main`
   protegida, GitHub no le deja.
