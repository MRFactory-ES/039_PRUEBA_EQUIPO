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
- Cada persona toca solo su bloque de `equipo.js`. Los bloques van separados por
  líneas de comentario para que dos cambios en bloques distintos no choquen.
- Remoto con el usuario dentro: `https://cokemomoMR@github.com/MRFactory-ES/039_PRUEBA_EQUIPO.git`.
