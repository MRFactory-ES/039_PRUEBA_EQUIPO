# 039_PRUEBA_EQUIPO

Web de práctica para aprender Pull Requests con los compañeros. Repo público en la
organización `MRFactory-ES`, publicada en `https://mrfactory-es.github.io/039_PRUEBA_EQUIPO/`.

## Reglas

- **`main` está protegida, también para los admins** (`enforce_admins` activado el
  03/11/2026). Todo entra por Pull Request con una aprobación. Un `git push` directo a
  `main` lo rechaza GitHub con `GH006`: comprobado el 03/11/2026.
- **Nadie aprueba su propio Pull Request.** Los cambios de Coke los tiene que aprobar
  otro: hoy Joe (`JoeCode5050`). Si Coke está solo y necesita entrar algo, la salida
  es desactivar un momento la protección en Settings → Branches, no saltársela a
  escondidas.
- **Los propietarios de la organización son admins de todos sus repos** sin que nadie
  se lo dé: `JoeCode5050` y `MRFactoryAI`. Por eso `enforce_admins` tiene que estar
  activado; si no, pueden subir a `main` sin pasar por revisión.
- Cada persona toca solo su página, `paginas/<nombre>.html`: un fichero por persona
  para que dos cambios de personas distintas nunca choquen. Las páginas no comparten
  CSS a propósito, por el mismo motivo. `equipo.js` solo lista quién sale en el
  tablón y no es parte de las prácticas.
- Las 7 personas de la prueba (03/11/2026): Juan Luis, Coke, Vero, Justo, Inés,
  Teresa y Agus. Joe no tiene tarjeta: es el que aprueba lo de Coke.
- **Instrucciones del equipo en `docs/INSTRUCCIONES_EQUIPO.html` → `.pdf`**, con
  GitHub Desktop + Visual Studio Code. Los textos de los botones (`Clone Repository…`,
  `New Branch…`, `Fetch origin`, `Pull origin`, `Publish branch`, `Push origin`,
  `Preview Pull Request`, `Show in Finder`/`Show in Explorer`) están sacados del código
  de desktop/desktop el 03/11/2026, no de la app abierta.
- **Trampa del PDF: medir el desborde en pantalla no sirve.** Con `scrollHeight` en
  Chrome salía todo a 0 y aun así la página 3 se salía al imprimir y su pie caía sobre
  la 4. Se comprueba leyendo el texto de cada página del PDF (`pypdfium2`): cada una
  tiene que empezar por su título y llevar su «N / 4».
- Remoto con el usuario dentro: `https://cokemomoMR@github.com/MRFactory-ES/039_PRUEBA_EQUIPO.git`.
