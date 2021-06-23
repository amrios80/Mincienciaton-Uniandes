# Título de la Solución: Proyecto Descriptivo Covid-Uniandes
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
Repositorio de la solución que calcula el **Análisis Descriptivo** de los datos fuente para los 6 eventos/enfermedades seleccionadas.

Se calcularon las estadísticas descriptivas para los siguientes eventos:
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
import os
import json
import yaml
import logging
import pandas as pd
import numpy as np
import scipy.stats as ss
import util_lib as ul
from datetime import datetime
from math import sqrt, log
from scipy import stats
from sklearn.metrics import mean_squared_error
```

### Requerimientos Hardware
Es una solución ligera que no tiene mayores requisitos de hardware. Al ser ejecutada en un equipo con una CPU Intel Core i7 (o mejor) y 8 GB de RAM, generará los resultados en 1 o 2 minutos como máximo.

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
      "enabled": true,
      "frequency": "weekly",
      "name": "TUBERCULOSIS",
      "rate_enable": true,
      "skip_years": []
    },
    {
      ...
    }
  ],
  "entity_filter": []
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
- Creado el 15 de noviembre, 2020
- Última actualización el 16 de diciembre, 2020
