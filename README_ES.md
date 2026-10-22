# Análisis del Mercado de Videojuegos

[English](README.md)

## Descripción del proyecto

Este proyecto analiza datos históricos de ventas de videojuegos para identificar patrones asociados con el éxito comercial y apoyar decisiones de producto y publicidad para una tienda internacional de videojuegos.

El análisis fue desarrollado como un proyecto integral de análisis de datos utilizando Python e incluye preparación de datos, análisis exploratorio, diferencias entre mercados regionales, análisis de correlación y pruebas estadísticas de hipótesis.

El escenario de negocio supone que se dispone de información histórica hasta 2016 y que la empresa está preparando su estrategia comercial para 2017.

## Objetivo de negocio

El objetivo principal es identificar qué características están asociadas con mayores ventas de videojuegos y determinar cómo estos patrones varían entre mercados.

El análisis busca responder preguntas como:

- ¿Qué plataformas han tenido mejor desempeño en los últimos años?
- ¿Qué géneros generan mayores ventas?
- ¿Cómo cambian las preferencias entre Norteamérica, Europa y Japón?
- ¿Existe relación entre las calificaciones de críticos y usuarios y las ventas?
- ¿Las calificaciones promedio de los usuarios de Xbox One y PC son diferentes?
- ¿Las calificaciones de los juegos de Acción y Deportes presentan diferencias estadísticamente significativas?

## Dataset

El conjunto de datos contiene **16.715 registros de videojuegos** e incluye:

- Nombre del videojuego
- Plataforma
- Año de lanzamiento
- Género
- Ventas en Norteamérica
- Ventas en Europa
- Ventas en Japón
- Ventas en otras regiones
- Calificación de críticos
- Calificación de usuarios
- Clasificación ESRB

Las ventas están expresadas en millones de unidades.

## Herramientas y tecnologías

- Python
- Pandas
- NumPy
- Matplotlib
- SciPy
- Jupyter Notebook

## Proceso de análisis

### 1. Exploración inicial

Se revisó la estructura y calidad del dataset utilizando métodos como:

- `head()`
- `sample()`
- `info()`
- `isna()`
- `duplicated()`

Esto permitió identificar tipos de datos, valores ausentes y posibles problemas de calidad.

### 2. Limpieza y preparación de datos

El proceso incluyó:

- Estandarización de nombres de columnas.
- Conversión de las calificaciones de usuarios a valores numéricos.
- Tratamiento de los valores `tbd` como datos ausentes.
- Revisión de valores faltantes.
- Eliminación de registros sin información esencial.
- Creación de una variable de ventas totales mediante la suma de las ventas regionales.

### 3. Análisis histórico y período relevante

Los datos históricos fueron utilizados para estudiar el ciclo de vida de las plataformas.

Para las decisiones relacionadas con 2017, el análisis se concentró principalmente en el período **2012–2016**, compuesto por **2.886 videojuegos**, ya que representa mejor el comportamiento reciente del mercado.

## Principales hallazgos

### Desempeño de plataformas

Durante 2012–2016, las plataformas con mayores ventas totales fueron:

1. PS4 — 314,14 millones
2. PS3 — 288,79 millones
3. Xbox 360 — 236,54 millones
4. Nintendo 3DS — 194,61 millones
5. Xbox One — 159,32 millones

El análisis histórico muestra que las plataformas tienen ciclos claros de crecimiento y descenso.

Por esta razón, el desempeño reciente resulta más útil para la planificación comercial de corto plazo que las ventas históricas acumuladas.

### Desempeño por género

Action registró las mayores ventas durante el período reciente, seguido por Shooter, Role-Playing y Sports.

Sin embargo, las preferencias por género cambian considerablemente entre regiones.

## Análisis regional

### Norteamérica

Xbox 360 fue la plataforma con mayores ventas durante el período analizado, seguida por PS4, PS3, Xbox One y Nintendo 3DS.

Los géneros Action y Shooter presentaron el mayor volumen de ventas.

### Europa

PS4 fue la plataforma con mayores ventas, seguida por PS3 y Xbox 360.

Action y Shooter también fueron los géneros con mayor participación.

### Japón

El mercado japonés presentó un comportamiento diferente al de Norteamérica y Europa.

Nintendo 3DS fue la plataforma más importante y **Role-Playing** fue el género con mayores ventas.

Estos resultados indican que una estrategia comercial global debería adaptarse a las preferencias particulares de cada región.

## Relación entre calificaciones y ventas

Para los videojuegos de PS4 se encontró:

- Correlación entre calificación de críticos y ventas: **0,407**
- Correlación entre calificación de usuarios y ventas: **-0,032**

Las calificaciones de críticos presentan una asociación positiva moderada con las ventas.

En contraste, las calificaciones de los usuarios muestran prácticamente ninguna relación lineal con las ventas.

Estas correlaciones representan asociaciones entre variables y no deben interpretarse como evidencia de causalidad.

## Pruebas de hipótesis

### Xbox One vs PC

**Hipótesis nula (H₀):** las calificaciones promedio de usuarios para Xbox One y PC son iguales.

**Hipótesis alternativa (H₁):** las calificaciones promedio son diferentes.

Se utilizó un nivel de significancia de:

**α = 0,05**

Resultado:

**p-value = 0,549**

Como el p-value es mayor que el nivel de significancia, no se puede rechazar la hipótesis nula.

Los datos disponibles no proporcionan evidencia estadística suficiente para afirmar que las calificaciones promedio de los usuarios de Xbox One y PC sean diferentes.

### Action vs Sports

**Hipótesis nula (H₀):** las calificaciones promedio de los juegos Action y Sports son iguales.

**Hipótesis alternativa (H₁):** las calificaciones promedio son diferentes.

Resultado:

**p-value ≈ 4,24 × 10⁻²⁰**

Como el p-value es considerablemente menor que 0,05, se rechaza la hipótesis nula.

Los datos proporcionan evidencia estadística de una diferencia entre las calificaciones promedio de los juegos Action y Sports.

## Conclusiones de negocio

A partir del análisis realizado, para una estrategia comercial orientada a 2017:

- PS4 representa una plataforma relevante por su desempeño reciente.
- Los géneros Action y Shooter presentan un alto potencial para campañas dirigidas a mercados amplios.
- Las diferencias regionales deben tenerse en cuenta al seleccionar productos y diseñar campañas.
- Japón requiere una estrategia diferenciada, especialmente orientada a Nintendo 3DS y juegos Role-Playing.
- Las calificaciones de críticos pueden aportar información adicional sobre el desempeño comercial, aunque no deben utilizarse como único criterio.
- El potencial de un videojuego debe evaluarse considerando conjuntamente plataforma, género, región, calificaciones y clasificación ESRB.

## Estructura del repositorio

```text
video-game-market-analysis/
│
├── data/
│   └── games.csv
│
├── notebooks/
│   └── video_game_market_analysis.ipynb
│
├── images/
│
├── .gitignore
├── README.md
├── README_ES.md
└── requirements.txt
```

## Cómo ejecutar el proyecto

Clone el repositorio:

```bash
git clone https://github.com/sebas-arl/video-game-market-analysis.git
```

Ingrese a la carpeta:

```bash
cd video-game-market-analysis
```

Cree un entorno virtual:

```bash
python -m venv .venv
```

Instale las dependencias:

```bash
python -m pip install -r requirements.txt
```

Abra el notebook:

```text
notebooks/video_game_market_analysis.ipynb
```

## Competencias demostradas

- Limpieza y preparación de datos
- Análisis Exploratorio de Datos
- Agrupación y agregación
- Visualización de datos
- Análisis de mercados
- Segmentación regional
- Análisis de correlación
- Estadística descriptiva
- Pruebas de hipótesis
- Interpretación de resultados
- Python
- Pandas
- Comunicación de hallazgos orientados al negocio

## Autor

**Sebastián Arcos Alvear**

Data Analyst / Data Scientist Jr

GitHub: [sebas-arl](https://github.com/sebas-arl)
