DATA WRANGLING Y EDA
1. INTRODUCCIÓN
El siguiente notebook se desarrollará una rutina de preprocesamiento sobre un conjunto de datos.

1) En primer lugar, se obtiene una breve descripción estadística y gráfica de cada una de las variables.

2) En segundo lugar, se aplicarán técnicas de limpieza, transformación y preparación de conjuntos de datos para su análisis.

3) En tercer lugar, se realizará un Análisis Exploratorio de Datos (EDA) luego de aplicar las técnicas de limpieza de datos.

2. PREPARACIÓN DE DATOS EN EL CONJUNTO DE DATOS

# Importamos librerias
import pandas as pd
import time
import numpy as np
from scipy import stats
import seaborn as sns
import matplotlib.pyplot as plt
import warnings
warnings.filterwarnings("ignore")
     
2.1. Carga de los datos
Cargaremos los datos sobre los que trabajaremos:


from google.colab import drive
drive.mount('/content/drive')
     
Mounted at /content/drive

from google.colab import files
     

# Importamos el archivo
df = pd.read_csv('/content/drive/MyDrive/automobile_raw.csv')
     

# Cantidad de filas y columnas
df.shape
     
(240, 26)
2.1.1. Breve descripción estadística

# Breve descripción del conjunto de datos
df.describe(include='all')
     
symboling	normalized-losses	make	fuel-type	aspiration	num-of-doors	body-style	drive-wheels	engine-location	wheel-base	...	engine-size	fuel-system	bore	stroke	compression-ratio	horsepower	peak-rpm	city-mpg	highway-mpg	price
count	240.000000	199.000000	240	240	240	238	240	240	240	240.000000	...	240.000000	240	236.000000	236.000000	240.000000	238.000000	238.000000	240.000000	240.000000	236.000000
unique	NaN	NaN	22	2	2	2	5	3	2	NaN	...	NaN	8	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN
top	NaN	NaN	toyota	gas	std	four	sedan	fwd	front	NaN	...	NaN	mpfi	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN
freq	NaN	NaN	36	210	196	132	105	144	237	NaN	...	NaN	115	NaN	NaN	NaN	NaN	NaN	NaN	NaN	NaN
mean	0.787500	120.507538	NaN	NaN	NaN	NaN	NaN	NaN	NaN	98.792083	...	124.229167	NaN	3.357119	3.238729	10.075917	102.357143	5166.033613	26.250000	30.525000	12314.292373
std	1.280956	35.264064	NaN	NaN	NaN	NaN	NaN	NaN	NaN	6.186493	...	41.118891	NaN	0.324350	0.337232	4.065526	38.767218	503.771153	7.277236	7.280354	7828.397336
min	-2.000000	65.000000	NaN	NaN	NaN	NaN	NaN	NaN	NaN	86.000000	...	61.000000	NaN	2.540000	2.000000	7.000000	47.000000	4089.000000	13.000000	13.000000	424.000000
25%	0.000000	94.000000	NaN	NaN	NaN	NaN	NaN	NaN	NaN	94.500000	...	97.000000	NaN	3.050000	3.030000	8.500000	70.000000	4800.000000	21.000000	25.000000	7295.000000
50%	1.000000	113.000000	NaN	NaN	NaN	NaN	NaN	NaN	NaN	97.000000	...	110.500000	NaN	3.310000	3.230000	9.000000	95.000000	5200.000000	25.500000	30.000000	9543.500000
75%	2.000000	149.000000	NaN	NaN	NaN	NaN	NaN	NaN	NaN	102.100000	...	141.000000	NaN	3.620000	3.402500	9.400000	116.000000	5500.000000	31.000000	34.000000	15656.250000
max	3.000000	256.000000	NaN	NaN	NaN	NaN	NaN	NaN	NaN	120.900000	...	326.000000	NaN	4.000000	4.170000	25.000000	288.000000	7067.000000	51.000000	57.000000	45400.000000
11 rows × 26 columns

2.1.2. Tipos de datos de las variables

# Tipos de datos de cada variable
df.dtypes
     
symboling              int64
normalized-losses    float64
make                  object
fuel-type             object
aspiration            object
num-of-doors          object
body-style            object
drive-wheels          object
engine-location       object
wheel-base           float64
length               float64
width                float64
height               float64
curb-weight            int64
engine-type           object
num-of-cylinders      object
engine-size            int64
fuel-system           object
bore                 float64
stroke               float64
compression-ratio    float64
horsepower           float64
peak-rpm             float64
city-mpg               int64
highway-mpg            int64
price                float64
dtype: object
