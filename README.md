# Recomendadores clásicos vs. generativos (GR-LLMs)

Notebook que compara recomendadores vistos en clase (contenido, colaborativo user-user, híbrido) contra modelos secuenciales inspirados en el paper:

> Yang, Lin, Xue y Zhang (AMAP, Alibaba). *GR-LLMs: Recent Advances in Generative Recommendation Based on Large Language Models*. arXiv 2507.06507 (2025).

El paper es un survey. Acá se implementan versiones chicas de SASRec, HSTU-lite y KuaiFormer-style, y se evalúan sobre MovieLens con partición temporal.

## Contenido

- `comparacion_gr_llms_topicos.ipynb`: notebook completo (datos, evaluación, métodos, comparación, matrices de confusión).

## Datos

El dataset no se incluye en el repo. Descargá **MovieLens (ml-latest-small)** desde https://grouplens.org/datasets/movielens/ y copiá estos archivos en una carpeta `data/`:

```
data/
├── ratings.csv
└── movies.csv
```

Si los guardás en otro lugar, cambiá `DATA_DIR` en la celda de configuración del notebook.

## Cómo correrlo

**En Google Colab (recomendado, usa GPU):**
1. Abrí https://colab.research.google.com → Archivo → Abrir notebook → pestaña GitHub.
2. Pegá la URL de este repo y elegí el notebook.
3. Entorno de ejecución → Cambiar tipo de entorno → GPU T4.
4. Subí `ratings.csv` y `movies.csv` a `data/` en el entorno de Colab.

**Local:**
```bash
git clone <URL_DEL_REPO>
cd <carpeta>
pip install numpy pandas scikit-learn torch jupyter matplotlib
jupyter notebook comparacion_gr_llms_topicos.ipynb
```

## Trabajo en equipo

- Hacer `git pull` antes de empezar.
- Trabajar en una rama propia (`git checkout -b mi-rama`) y abrir un Pull Request.
- Evitar que dos personas editen el notebook a la vez: los `.ipynb` se mezclan mal.
