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

## Cómo cambiar tu página (con Claude Code)

Todo el equipo trabaja con **Claude Code**: le dices lo que quieres y él hace el git.
Los pasos, con las frases exactas que hay que decirle, están en
[`docs/INSTRUCCIONES_EQUIPO.pdf`](docs/INSTRUCCIONES_EQUIPO.pdf).

La versión corta, con Claude Code abierto en la carpeta del proyecto:

1. «Soy Vero. Bájate lo último de main y crea una rama nueva llamada vero-titulo.»
2. «En mi página cambia …»
3. «Ábreme el tablón en el navegador.»
4. «Sube mi cambio y crea un Pull Request para Coke.»

Las reglas que tiene que seguir Claude están en `CLAUDE.md`, que lee solo al abrirse
en esta carpeta.

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
