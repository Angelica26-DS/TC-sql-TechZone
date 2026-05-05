### Team Challenge SQL
 Parte 1: SQL Murder Mystery

 Resolución del caso mediante consultas SQL.

### Parte 2: BigQuery - TechZone

Diseño de un modelo de datos para un e-commerce, generación de datos simulados, carga en BigQuery y análisis con SQL.

Estructura del proyecto
TC-SQL-TECHZONE/
├── credentials/
│   └── key.json
├── data/
├── docs/
│   ├── data_model.md
│   └── er_model.png
├── notebooks/
│   ├── 01_sql_murder_mystery.ipynb
│   ├── 02_setup_bigquery.ipynb
│   ├── 03_generate_data.ipynb
│   └── 04_queries_verification.ipynb
├── .env
├── .env.example
├── .gitignore
├── README.md
└── requirements.txt

## Setup

### 1. Clonar el repositorio
git clone https://github.com/[usuario]/tc-sql-techzone.git
cd TC-SQL-TECHZONE

### 2. Crear entorno virtual
python -m venv venv
venv\Scripts\activate

### 3. Instalar dependencias
pip install -r requirements.txt

### 4. Configurar variables de entorno
Crear archivo .env basado en .env.example y añadir:

GCP_PROJECT_ID=techzone-494713
BQ_DATASET_ID=TechZone
GOOGLE_APPLICATION_CREDENTIALS=credentials/key.json

El archivo .env no se sube al repositorio.

### Ejecución

### Orden recomendado de notebooks:
notebooks/02_setup_bigquery.ipynb → conexión a BigQuery
notebooks/03_generate_data.ipynb → generación de datos
notebooks/04_queries_verification.ipynb → análisis

### Flujo del proyecto
Diseño del modelo de datos (3NF)
Generación de datos con Faker
Carga en BigQuery
Validación de datos
Análisis con SQL

### Análisis realizado
Ventas totales del negocio
Productos más vendidos
Productos con mayor generación de ingresos
Ventas por categoría
Valoración media de productos

### Insights principales
Las laptops generan más ingresos
Los productos más vendidos no son los más rentables
Existe diferencia entre volumen de ventas y valor económico
Las valoraciones deben analizarse junto al número de reviews

### Consideraciones
Datos simulados
Posibles inconsistencias entre ciudad y país
Comentarios generados automáticamente

### Equipo
| Nombre     | Rol               | Rama                    |
|------------|------------------|-------------------------|
| Angélica   | Scrum Master     | feature/setup-angie     |
| Carlos     | QA / Docs        | feature/docs-carlos     |
| Hugo       | Data Engineer    | feature/data-hugo       |

Cada integrante trabajó en su propia rama siguiendo un flujo de Pull Requests (PR), 
permitiendo revisiones antes de integrar los cambios en la rama principal (main).

### Presentación 
Duración total: 10 minutos
Incluye:
Modelo de datos (ER + 3NF)
Demo en BigQuery
Queries analíticas
Revisión del repositorio
Retrospectiva del equipo
