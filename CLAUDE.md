# cuba-eventos-pages — cuba-eventos.giwa-ia.com

Wrapper de GitHub Pages (repo **público**, sin datos sensibles) que abre a pantalla completa
la web app de `../cuba-brindis-dirigentes-gs` (deployment fijo `AKfycbxuCmwE…`).

- Deploy: `git push` (Pages desde `main`). DNS en Squarespace:
  `CNAME cuba-eventos → sechavarria-star.github.io`.
- El botón "Pagar con Mercado Pago" navega la ventana entera a MP (target `_top`), y MP
  vuelve directo al `/exec`, no al subdominio: es esperable.
