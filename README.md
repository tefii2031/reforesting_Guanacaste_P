# 🌍 Análisis Geoespacial de Reforestación en Guanacaste con IA

[![Estado del Proyecto](https://img.shields.io/badge/estado-en%20desarrollo-blue)]()
[![Python](https://img.shields.io/badge/python-3.8%2B-blue)]()
[![Asistido por IA](https://img.shields.io/badge/asistido%20por-IA-purple)]()

Proyecto de análisis de datos geoespacial asistido por inteligencia artificial para monitoreo y evaluación de iniciativas de reforestación en la región de Guanacaste, Costa Rica.

## 📋 Tabla de Contenidos

- [Descripción General](#descripción-general)
- [Características](#características)
- [Requisitos Previos](#requisitos-previos)
- [Instalación](#instalación)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Datos](#datos)
- [Uso](#uso)
- [Metodología](#metodología)
- [Resultados](#resultados)
- [Tecnologías](#tecnologías)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)
- [Contacto](#contacto)

## 📖 Descripción General

Este proyecto integra técnicas avanzadas de análisis geoespacial y modelos de inteligencia artificial para:

- **Monitoreo de cobertura forestal** mediante análisis de imágenes satelitales
- **Predicción de cambios** en uso de suelo utilizando modelos de aprendizaje automático
- **Evaluación de impacto**  de diferentes esenarios de reforestación
- **Generación de reportes** automatizados para stakeholders
- **Visualización interactiva** de resultados geoespaciales

## ✨ Características

- ✅ API REST para consultas programáticas
- ✅ Procesamiento automático de imágenes satelitales (Sentinel-2, Landsat, potencialmente Planet)
- ✅ Clasificación de cobertura forestal con algoritmos de ML/DL
- ✅ Análisis de series temporales geoespaciales
- ✅ Detección de cambios automática
- ✅ Dashboard interactivo con visualización de resultados
- ✅ Exportación de reportes en múltiples formatos


## 🔧 Requisitos Previos

- Python 3.8 o superior
- GDAL/OGR 3.0+
- PostGIS (opcional, para análisis avanzados)
- Git
- Conda o pip para gestión de dependencias
- QGIS 4.2.2-Belém do Pará


## 📦 Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/[usuario]/reforesting_Guanacaste_P.git
cd reforesting_Guanacaste_P
```

### 2. Crear entorno virtual

```bash
# Con Conda (recomendado para dependencias geoespaciales)
conda create -n guanacaste-geo python=3.10
conda activate guanacaste-geo

# O con venv
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 4. Descargar datos iniciales (opcional)

```bash
python scripts/download_data.py
```

## 📁 Estructura del Proyecto sugerida

```
reforesting_Guanacaste_P/
├── data/                          # Datos de entrada y procesados
│   ├── raw/                       # Datos sin procesar
│   ├── processed/                 # Datos procesados
│   └── reference/                 # Datos de referencia (shapefiles, etc.)
├── notebooks/                     # Notebooks Jupyter
│   ├── 01_exploratory_analysis.ipynb
│   ├── 02_data_preprocessing.ipynb
│   └── 03_model_training.ipynb
├── src/                           # Código fuente
│   ├── __init__.py
│   ├── data_processing.py         # Procesamiento de datos
│   ├── ml_models.py               # Modelos de aprendizaje automático
│   ├── geospatial_analysis.py     # Análisis geoespacial
│   └── visualization.py           # Visualización de resultados
├── models/                        # Modelos entrenados
│   └── best_model.pkl
├── results/                       # Resultados y reportes
│   ├── figures/
│   ├── maps/
│   └── reports/
├── scripts/                       # Scripts de utilidad
│   ├── download_data.py
│   ├── train_model.py
│   └── generate_report.py
├── tests/                         # Pruebas unitarias
├── requirements.txt               # Dependencias del proyecto
├── setup.py                       # Configuración del paquete
├── .gitignore
└── README.md
```

## 📊 Datos

### Fuentes de Datos

- **Imágenes Satelitales**: por definir
- **Datos de Referencia**:  por definir
- **Datos de Campo**: por definir

### Acceso a los Datos

Los datos pueden descargarse desde:
- [Copernicus Open Access Hub](https://scihub.copernicus.eu/)
- [USGS EarthExplorer](https://earthexplorer.usgs.gov/)
- [Google Earth Engine](https://earthengine.google.com/)

## 🚀 Uso

### Procesamiento Básico

# Inicializar procesador
# Descargar y procesar imágenes
# Entrenar modelo

### Dashboard Interactivo

```bash
streamlit run src/dashboard.py
```

Acceder en: `http://localhost:8501`

## 🔬 Metodología

### 1. Preprocesamiento de Datos

- Descarga de imágenes satelitales
- Corrección atmosférica (sen2cor)
- Remuestreo y alineación de capas
- Enmascaramiento de nubes

### 2. Ingeniería de Características

- Cálculo de índices espectrales (NDVI, NDBI, NDWI)
- Análisis textural
- Características temporales

### 3. Modelo de IA

- **Algoritmo**: por definir
- **Clases**: por definir
- **Validación**: por definir


### Hallazgos Principales

- Ver reportes completos en `results/reports/`

### Mapas y Visualizaciones

- [Mapa interactivo de cambios](results/maps/)
- [Serie temporales](results/figures/)

## 🛠️ Tecnologías

### Geoespacial
- **GDAL/OGR** - Procesamiento de datos raster y vector
- **Rasterio** - I/O de datos raster
- **Fiona** - I/O de datos vector (shapefiles)
- **Geopandas** - Análisis geoespacial
- **Folium/Leaflet** - Mapas interactivos

### Machine Learning
- **Scikit-learn** - Algoritmos ML clásicos
- **TensorFlow/Keras** - Redes neuronales
- **XGBoost** - Gradient boosting

### Visualización
- **Matplotlib/Seaborn** - Gráficos estáticos
- **Plotly** - Gráficos interactivos
- **Streamlit** - Dashboard web

### Utilidades
- **Jupyter** - Notebooks interactivos
- **Pandas** - Manipulación de datos
- **NumPy** - Computación numérica

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Para cambios mayores:

1. Fork del repositorio
2. Crear rama de feature (`git checkout -b feature/AmazingFeature`)
3. Commit de cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abrir Pull Request

## Formatos de las contribuciones

Formato general

`<tipo>(<alcance>): <descripción>`
`<cuerpo>`
`<pie de página>`

Tipos principales:
`feat:` Nueva característica
`fix:` Corrección de bug
`docs:` Cambios en documentación
`style:` Cambios de formato (espacios, comillas, etc.)
`refactor:` Cambios que no añaden features ni fixes
`perf:` Mejoras de rendimiento
`test:` Añadir o actualizar tests
`chore:` Cambios en build, dependencies, config
`ci:` Cambios en CI/CD

### Resumen
📋 Cheat Sheet Rápido

| Acción | Comando |
|--------|---------|
| Nueva feature | `git commit -m "feat(módulo): descripción"` |
| Corrección | `git commit -m "fix(módulo): descripción"` |
| Documentación | `git commit -m "docs: descripción"` |
| Tests | `git commit -m "test(módulo): descripción"` |
| Refactor | `git commit -m "refactor(módulo): descripción"` |
| Configuración | `git commit -m "chore: descripción"` |

### Directrices

- Seguir PEP 8 para estilos de código
- Incluir tests unitarios
- Actualizar documentación
- Añadir docstrings en inglés y español

---

**Última actualización**: 2024
**Estado**: En desarrollo activo
**Versión**: 1.0.0

> 🤖 **Nota**: Este proyecto fue desarrollado con asistencia de herramientas de IA generativa (GitHub Copilot y Claude) para optimizar el workflow de desarrollo y análisis de datos.
