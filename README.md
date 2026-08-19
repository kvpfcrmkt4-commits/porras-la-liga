# Porra La Liga 2026/27

Aplicación compartida para pronosticar los partidos de LaLiga.

## Arquitectura
- GitHub Pages: frontend (`index.html`).
- Supabase: partidos y predicciones.
- Supabase Edge Function `sync-sofascore-v2`: sincroniza SofaScore.
- SofaScore: calendario, estados y resultados.

## Publicación
Sube `index.html` a la raíz del repositorio `porras-la-liga` y activa GitHub Pages desde Settings → Pages → Deploy from branch → main → root.

La página ya contiene la URL y publishable key del proyecto Supabase preparado para esta porra.

## Puntuación
- 3 puntos: marcador exacto.
- 1 punto: acierta 1X2 aunque falle el marcador.
- 0 puntos: cualquier otro resultado.

Las predicciones se bloquean por fecha/hora de inicio y también cuando SofaScore marca el partido como en juego/finalizado.

## Actualización
Al abrir la web se sincroniza el calendario. Después se actualizan las jornadas relevantes aproximadamente cada minuto mientras la página está abierta.
