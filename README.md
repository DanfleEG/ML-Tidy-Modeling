# ML-Tidy-Modeling

> Presentación académica de Machine Learning y modelado estadístico desarrollada con Quarto + RevealJS sobre el ecosistema R.

---

## Descripción general

**ML-Tidy-Modeling** es un proyecto académico que documenta y presenta los fundamentos del modelado estadístico y el aprendizaje automático mediante una serie de presentaciones interactivas construidas con [Quarto](https://quarto.org/) y [RevealJS](https://revealjs.com/).

El proyecto toma como referencia principal el libro *Tidy Modeling with R* (Kuhn & Silge, 2022) y organiza su contenido en capítulos progresivos, cada uno cubriendo un área temática del proceso de modelado moderno. El enfoque combina rigor académico con claridad visual, priorizando la reproducibilidad y la coherencia metodológica a través del ecosistema `tidymodels`.

El repositorio está diseñado para crecer de forma colaborativa y estructurada, sirviendo tanto como material de exposición como referencia técnica para el equipo.

---

## Objetivos

- Presentar los fundamentos conceptuales del modelado estadístico y el machine learning de forma clara y progresiva.
- Ilustrar el uso del ecosistema `tidymodels` como herramienta unificada para el modelado en R.
- Desarrollar competencias en comunicación técnica y científica mediante presentaciones reproducibles.
- Construir un repositorio colaborativo que pueda extenderse con nuevos capítulos y visualizaciones.

---

## Tecnologías utilizadas

| Tecnología | Rol en el proyecto |
|---|---|
| [Quarto](https://quarto.org/) | Sistema de publicación científica y técnica |
| [R](https://www.r-project.org/) | Lenguaje de análisis estadístico y modelado |
| [RevealJS](https://revealjs.com/) | Motor de presentaciones HTML interactivas |
| [tidyverse](https://www.tidyverse.org/) | Ecosistema de manipulación y visualización de datos |
| [tidymodels](https://www.tidymodels.org/) | Framework unificado de modelado en R |
| Git / GitHub | Control de versiones y colaboración distribuida |

---

## Estructura del proyecto

```txt
ML-Tidy-Modeling/
│
├── index.qmd          # Presentación principal (Capítulo 1)
├── _quarto.yml        # Configuración global del proyecto Quarto
├── images/            # Recursos gráficos e imágenes de soporte
├── data/              # Conjuntos de datos utilizados en los ejemplos
├── styles.css         # Estilos CSS adicionales (si aplica)
└── README.md          # Documentación del repositorio
```

**Descripción de cada elemento:**

- **`index.qmd`** — Archivo principal de la presentación. Contiene el contenido del Capítulo 1: *Software for Modeling*. Futuros capítulos se agregarán como archivos `.qmd` independientes.
- **`_quarto.yml`** — Configuración global del proyecto: tipo, título, opciones de ejecución. No debe modificarse sin coordinación del equipo.
- **`images/`** — Carpeta para logos, diagramas exportados y recursos visuales estáticos.
- **`data/`** — Datasets de ejemplo o referencia utilizados en las diapositivas.
- **`styles.css`** — Archivo de estilos opcionales complementarios al CSS embebido en las presentaciones.
- **`README.md`** — Este archivo. Documentación técnica y guía de colaboración.

---

## Cómo ejecutar el proyecto

### Requisitos previos

- [R](https://cran.r-project.org/) instalado (≥ 4.2)
- [Quarto CLI](https://quarto.org/docs/get-started/) instalado (≥ 1.4)
- Paquetes R necesarios:

```r
install.packages(c("tidyverse", "tidymodels"))
```

### Renderizar localmente

```bash
# Renderizar la presentación principal
quarto render index.qmd

# Renderizar todo el proyecto
quarto render
```

### Previsualizar en el navegador

```bash
quarto preview index.qmd
```

### Publicar en Quarto Pub

```bash
quarto publish quarto-pub
```

### Publicar en GitHub Pages

```bash
quarto publish gh-pages
```

---

## Flujo de trabajo recomendado

Para mantener la calidad y consistencia del proyecto, se recomienda seguir este flujo antes de cada contribución:

1. **Trabajar en una rama separada** — No hacer cambios directamente en `main`.
2. **Renderizar antes de subir** — Verificar que `quarto render` no genera errores.
3. **Commits descriptivos** — Usar mensajes claros que indiquen qué se modificó y en qué capítulo.
4. **Mantener consistencia visual** — Respetar la paleta de colores, tipografía y componentes CSS definidos en la presentación.
5. **No modificar `_quarto.yml`** sin acuerdo del equipo — Cambios en ese archivo afectan todo el proyecto.
6. **Usar rutas relativas** — Evitar rutas absolutas para garantizar compatibilidad entre sistemas.

```bash
# Ejemplo de flujo completo
git checkout -b capitulo-2/feature-ingenieria
# ... hacer cambios ...
quarto render
git add .
git commit -m "feat(cap2): agrega diapositivas de feature engineering"
git push origin capitulo-2/feature-ingenieria
```

---

## Reglas de colaboración

Para garantizar la integridad del proyecto, todos los colaboradores deben respetar las siguientes normas:

- **`_quarto.yml` es compartido** — Cualquier modificación debe ser consensuada. Un cambio incorrecto puede romper todo el proyecto.
- **Mantener rutas relativas** — Las referencias a imágenes, datos y estilos deben usar rutas relativas (`./images/logo.png`, no rutas absolutas del sistema).
- **No alterar el CSS global** — Los estilos visuales embebidos en `index.qmd` definen la identidad del proyecto. Cambios deben discutirse antes de aplicarse.
- **Probar la renderización** — Antes de hacer un Pull Request, confirmar que `quarto render` termina sin errores ni advertencias críticas.
- **No subir archivos generados** — Agregar `/_site`, `/.quarto` y archivos `*.html` al `.gitignore` para evitar conflictos.

Ejemplo de `.gitignore` recomendado:

```gitignore
/.quarto
/_site
*.html
*.pdf
.Rhistory
.RData
```

---

## Integrantes

| Nombre | Rol | Contacto |
|---|---|---|
| — | — | — |
| — | — | — |
| — | — | — |
| — | — | — |

> Completar con los nombres, roles y correos del equipo.

---

## Capítulos del proyecto

| # | Título | Estado | Archivo |
|---|---|---|---|
| 1 | Software for Modeling | ✅ Completo | `index.qmd` |
| 2 | *(próximo capítulo)* | 🔲 Pendiente | — |
| 3 | *(próximo capítulo)* | 🔲 Pendiente | — |

---

## Futuras mejoras

El proyecto está diseñado para escalar. Entre las extensiones planificadas se encuentran:

- **Nuevos capítulos** — Cubrir temas como preprocesamiento, validación cruzada, modelos de clasificación y regresión con `tidymodels`.
- **Visualizaciones interactivas** — Integrar gráficos dinámicos con `plotly` o `echarts4r` dentro de las diapositivas.
- **Dashboards complementarios** — Desarrollar tableros de análisis con `Quarto Dashboards` o `Shiny`.
- **Casos prácticos** — Incluir datasets reales y análisis end-to-end reproducibles.
- **Publicación web** — Despliegue continuo en Quarto Pub o GitHub Pages con cada actualización del repositorio.

---

## Referencias

- Kuhn, M. & Silge, J. (2022). *Tidy Modeling with R*. O'Reilly. [tmwr.org](https://www.tmwr.org/)
- James, G. et al. (2021). *An Introduction to Statistical Learning*. Springer.
- Quarto Documentation. [quarto.org/docs](https://quarto.org/docs/guide/)
- Tidymodels. [tidymodels.org](https://www.tidymodels.org/)

---

<p align="center">
  Proyecto académico · Quarto + R + RevealJS
</p>
