# 039_PRUEBA_EQUIPO

Web de práctica para aprender Pull Requests con los compañeros. Repo público en la
organización `MRFactory-ES`, publicada en `https://mrfactory-es.github.io/039_PRUEBA_EQUIPO/`.
Un tablón con una tarjeta por persona; cada tarjeta abre la página de esa persona en
`paginas/`.

## Si ayudas a un compañero del equipo (léelo antes de nada)

Quien te habla está aprendiendo a trabajar con GitHub y no es programador. Tú haces
todo lo de git por él. Respóndele en castellano, corto, y al terminar cada cosa dile
en una línea qué has hecho y qué tiene que mirar.

**Quién es.** Su página es `paginas/<su-nombre>.html` (`juan-luis`, `coke`, `vero`,
`justo`, `ines`, `teresa`, `agus`). Si no te ha dicho quién es, pregúntaselo antes de
tocar nada.

**Qué puede tocar: solo su página.** Si te pide cambiar otro fichero (`index.html`,
`equipo.js`, la página de otro), no lo hagas: dile que en esta práctica cada uno
cambia solo la suya.

**Nunca trabajes en `main`.** `main` está protegida y GitHub rechaza cualquier subida
directa. Todo cambio va en una rama suya, con nombre `<su-nombre>-<algo>` en minúsculas,
sin espacios ni tildes (por ejemplo `vero-titulo`).

Lo que te va a pedir, y qué hacer:

- **«Bájate lo último»** → `git switch main` y `git pull`. Si tiene cambios sin subir,
  avísale antes y no los pierdas.
- **«Crea mi rama …»** → desde `main` recién actualizada: `git switch -c <rama>`.
  Si te pide un cambio y está en `main`, crea antes la rama tú.
- **«Cambia en mi página …»** → edita solo `paginas/<su-nombre>.html`. Lo que se
  cambia está entre las marcas ✏️; el color, en `--color`.
- **«Ábreme el tablón»** → abre `index.html` en su navegador: `open index.html` en
  Mac, `start index.html` en Windows. Dile que pulse su tarjeta.
- **«Sube mi cambio»** → `git add` de su página, commit con un mensaje corto en
  castellano, `git push -u origin <rama>` y, si la rama aún no tiene Pull Request,
  `gh pr create --base main` con un título claro. Dale el enlace y dile que Coke lo
  revisará. Si ya tenía Pull Request, basta con el push: se actualiza solo.
- **«Lee lo que dice Coke»** → `gh pr view --comments`. Explícaselo y, si te lo pide,
  arréglalo en la misma rama y súbelo.
- **«Coke ya lo ha aprobado»** → `git switch main`, `git pull` y borra la rama local.
- **Conflicto** («This branch has conflicts» o un `pull` que choca) → no lo
  resuelvas por tu cuenta: explícale qué ha pasado y que avise a Coke.

Nunca: `--force`, aprobar o fusionar Pull Requests, ni cambiar la configuración del
repo en GitHub.

**Si falta algo en su ordenador.** Hace falta `git` y GitHub CLI (`gh`) con su sesión
iniciada (`gh auth status`). Si falta, instálalo. Para iniciar sesión,
`gh auth login --hostname github.com --git-protocol https --web`: si te pide
respuestas que no puedes dar, dile que lo ejecute él en una terminal y que acepte en
el navegador con el código que le salga. Si git no tiene nombre y correo, pídeselos
y configúralos.

## Para quien mantiene el repo (Coke)

- **`main` está protegida, también para los admins** (`enforce_admins` activado el
  03/11/2026). Todo entra por Pull Request con una aprobación. Un `git push` directo a
  `main` lo rechaza GitHub con `GH006`: comprobado el 03/11/2026.
- **Nadie aprueba su propio Pull Request.** Los cambios de Coke los tiene que aprobar
  otro: hoy Joe (`JoeCode5050`). Si Coke está solo y necesita entrar algo, la salida
  es desactivar un momento `enforce_admins`, fusionar y volver a activarlo.
- **Los propietarios de la organización son admins de todos sus repos** sin que nadie
  se lo dé: `JoeCode5050` y `MRFactoryAI`. Por eso `enforce_admins` tiene que estar
  activado; si no, pueden subir a `main` sin pasar por revisión.
- Un fichero por persona en `paginas/`, para que dos cambios de personas distintas
  nunca choquen. Las páginas no comparten CSS a propósito, por el mismo motivo.
  `equipo.js` solo lista quién sale en el tablón y no es parte de las prácticas.
- Las 7 personas de la prueba (03/11/2026): Juan Luis, Coke, Vero, Justo, Inés,
  Teresa y Agus. Joe no tiene tarjeta: es el que aprueba lo de Coke.
- **Instrucciones del equipo en `docs/INSTRUCCIONES_EQUIPO.html` → `.pdf`**: frases
  exactas para decirle a Claude Code. Funcionan porque la sección de arriba de este
  fichero le dice a su Claude qué hacer con cada una; si se cambia una, se cambian las
  dos.
- **Trampa del PDF: medir el desborde en pantalla no sirve.** Con `scrollHeight` en
  Chrome salía todo a 0 y aun así la página 3 se salía al imprimir y su pie caía sobre
  la 4. Se comprueba leyendo el texto de cada página del PDF (`pypdfium2`): cada una
  tiene que empezar por su título y llevar su «N / total».
- Remoto con el usuario dentro: `https://cokemomoMR@github.com/MRFactory-ES/039_PRUEBA_EQUIPO.git`.
