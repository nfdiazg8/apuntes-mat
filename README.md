# apuntes-mat

Apuntes de clase de Matemáticas con énfasis en Estadística (Universidad del Tolima).
Sitio Quarto publicado en <https://nfdiazg8.github.io/apuntes-mat>.

## Estructura

```
_quarto.yml                 configuración del sitio, navbar y sidebar
index.qmd                   home (HTML puro con las clases .am-*)
styles/base.scss            todas las reglas del diseño (compartidas)
styles/claro.scss           paleta modo claro
styles/oscuro.scss          paleta modo oscuro
_includes/fuentes.html      Google Fonts
materias/<materia>/         index.qmd (listado automático) + un .qmd por apunte
herramientas/ formulas/
docs/                       salida renderizada (lo que sirve GitHub Pages)
```

## Trabajar en el sitio

```bash
quarto preview            # servidor local con recarga
quarto render             # genera docs/
```

## Publicar

En GitHub: Settings → Pages → Source: `Deploy from a branch`, rama `main`,
carpeta `/docs`. Después basta con `quarto render` y `git push`.

## Añadir un apunte

1. Crear `materias/<materia>/<slug>.qmd` con `title`, `subtitle` y `date`.
2. Añadirlo al `sidebar` en `_quarto.yml`.
3. El índice de la materia lo recoge solo (listing).

## Clases propias del diseño

- `.kicker` — antetítulo azul en versalitas ("TEMA 3 · 12 SEP 2026")
- `.definicion` / `.teorema` / `.ejemplo` — bloque con barra de acento; la
  etiqueta va como `[Definición 3.1]{.etiqueta}` en la primera línea
- `.salida-pendiente` — marcador rayado para una figura que todavía no existe
- `.am-*` — solo para el home
