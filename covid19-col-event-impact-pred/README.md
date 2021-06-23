# Título de la Solución: Proyecto Predictivo Covid-Uniandes
Desarrollo y evaluación de modelos matemáticos y epidemiológicos que apoyen la toma de decisiones en respuesta a la emergencia Covid-19 en Colombia. El proyecto se abordó desde la perspectiva de la ciencia de datos, utilizando técnicas de Data Analytics y Machine Learning.

El proyecto fue separado en 2 grandes módulos, el de Análisis Descriptivo y el de Análisis Predictivo o de Pronósticos.

## Tabla de Contenidos
* [Descripción de la solución](#descripción-de-la-solución)
* [Screenshots](#screenshots)
* [Requerimientos](#requerimientos)
* [Instalación](#instalación)
* [Ejemplos de Código](#ejemplos-de-codigo)
* [Pruebas Automatizadas](#pruebas-automatizadas)
* [Autores](#autores)

## Descripción de la solución
Repositorio de la solución que calcula el **Análisis Predictivo o de Pronósticos** de los datos fuente para los 6 eventos/enfermedades seleccionadas.

Se calcularon los pronósticos con y sin COVID-19 para los siguientes eventos:
- Tuberculosis (TB)
- Mortalidad Infantil (IM)
- Intento de Suicidio (SA)
- Diabetes Mellitus (DM)
- Enfermedades Diarreicas Agudas (EDA)
- Exceso de Mortalidad (EM)

### Screenshots
![screenshot](https://www.eclipsemediasolutions.com/sites/default/files/Audience-web-traffic-fluctuations1.jpg)

## Requerimientos
La solución puede ser ejecutada tanto en un sistema operativo Linux como en uno Windows. Es necesario contar con Python 3.7.x o una versión posterior para ejecutar la solución. También puede ser ejecutada sobre la última versión de Anaconda.

### Librerias Empleadas 
Las librerías de Python necesarias para ejecutar la solución son:

```python
import concurrent.futures
import json
import logging
import numpy as np
import os
import pandas as pd
import pred_engine as pe
import scipy.stats as ss
import statsmodels.api as sm
import timeit
import util_lib as ul
import yaml
from datetime import datetime
from joblib import Parallel
from joblib import delayed
from math import ceil
from math import sqrt, log
from multiprocessing import cpu_count
from scipy import stats
from sklearn.metrics import mean_squared_error
from warnings import filterwarnings
```

### Requerimientos Hardware
Es una solución pesada que tiene altos requerimientos de hardware para poder generar los resultados en un tiempo aceptable.

Las pruebas se realizaron en un equipo EC2 c6g.2xlarge de AWS, y generaba los resultados para cada evento en aproximadamente 150 minutos (2.5 horas).

### Requerimientos Software
El proyecto fue realizado en Windows con la versión de <a href="https://www.anaconda.com/products/individual" target="_blank" >Anaconda</a>.

En Linux se probó también, sobre Python 3.8, con la posterior instalación de las siguientes librerías:

```python
sudo apt install
sudo add-apt-repository universe
sudo apt-get update
sudo apt install python3-pandas
sudo apt install python3-sklearn
sudo apt install python3-statsmodels
```

## Arquitectura de la solución
Para llenar

## Datos Fuente
Fuentes abiertas que se usaron para generar los datos de entrada a la solución:
- <a href="http://portalsivigila.ins.gov.co/Paginas/Vigilancia-Rutinaria.aspx" target="_blank">SIVIGILA</a>
- <a href="https://www.sispro.gov.co/Pages/Home.aspx" target="_blank">SISPRO</a>
- <a href="https://www.dane.gov.co/index.php/estadisticas-por-tema" target="_blank">DANE</a>
- <a href="https://www.datos.gov.co/Salud-y-Protecci-n-Social/Casos-positivos-de-COVID-19-en-Colombia/gt2j-8ykr" target="_blank">Datos Abiertos</a>

### Diagrama Entidad - Relación
Para llenar

## Instalación
Para llenar

## Configuración
Las tareas a ser realizadas por la solución son configuradas a partir de un archivo .JSON de configuración, con el siguiente formato:

```json
{
  "event_list": [
    {
      "analysis_list": [ "PARTIAL", "FULL" ],
      "ci_alpha": 0.9,
      "enabled": true,
      "full_init_date": "2017-01-01",
      "mape_threshold": 4.0,
      "n_forecast": 13,
      "name": "TUBERCULOSIS",
      "partial_end_date": "2019-12-27",
      "perc_test": 0.20,
      "ts_tolerance": 4.0
    },
    {
      ...
    }
  ],
  "entity_filter": ["COLOMBIA", "BOGOTA DC", "ANTIOQUIA"],
  "n_process": 1
}
```

## Ejemplos de Código
Para llenar

## Errores conocidos
Para llenar

## Pruebas Automatizadas
No aplica

## Imagenes
No aplica

## Autores
- Creado por <a href="https://github.com/ansegura7">Andrés Segura Tinoco</a>
- Creado el 25 de julio, 2020
- Última actualización el 10 de diciembre, 2020
