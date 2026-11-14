# cuba-eventos-pages — cuba-eventos.giwa-ia.com

Front estático (GitHub Pages, repo **público**, sin datos sensibles) del formulario del brindis
de dirigentes. Toda la lógica y los datos (evento, precio, áreas, registro, Mercado Pago) viven
en `../cuba-brindis-dirigentes-gs`, que se usa como **API JSON** (deployment fijo `AKfycbxuCmwE…`).

- Deploy: `git push` (Pages desde `main`). DNS en Squarespace:
  `CNAME cuba-eventos → sechavarria-star.github.io`.
- API: `GET ?api=config`, `GET ?api=retorno&<params de MP>`, `POST {accion:'registrar'|'linkPago'}`
  con `Content-Type: text/plain` (sin preflight de CORS).
- Mercado Pago vuelve a este dominio (`?mp=retorno&payment_id=…`) y el front verifica el pago por la API.
- El diseño es copia de `Index.html` / `Resultado.html` del script: si se toca uno, tocar el otro.
- **No usar iframe ni redirección al `/exec`**: el iframe falla con visitantes logueados en Google
  (en iPhone: "Sorry, unable to open the file at this time") y la redirección muestra `script.google.com`.
