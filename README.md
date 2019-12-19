<img src="https://github.com/luisferlc/IMECA-CDMX-Prediction/blob/master/images/ironhack.png">

# Predicción de IMECA para PM10 y PM2.5

**Luis Fernando López Corrales**

**Facebook Prophet**

## Alcance del análisis
Crear un modelo de predicción para las mediciones de PM10 y PM2.5 máximas diarias, en la zona centro de la Ciudad de México. Posteriormente, se calculará el IMECA máximo diario y se hará la comparación de los resultados con los IMECA's del 2019.
### Alcaldía: Cuahtemoc
Esto se traduce a las estaciones de medicion:
- Cuahtémoc: HGM (Hospital General de México). Zona Centro de CDMX.
#### Contaminantes
* PM10
* PM2.5

## Resúmen
El análisis se puede dividir en dos etapas:

#### 1.-Predicción de partículas por cada hora del día (análisis hecho solo para PM10):
- Rellenando NaN's con el promedio de cada año y eliminando otros.

#### 2.-Predicción de partículas por máxima concentración del día individual (PM10 y PM2.5):
- Eliminando outliers y dejando NaN's
 
 
## Modo de cálculo
1. Las mediciones de PM10 y PM2.5 derivan de las concentraciones obtenidas como promedio móvil de 24 horas (NOM-025-SSA1-2014).
2. Con base a las mediciones por hora, se obtendra el valor máximo o promedio de cada día y se hará la predicción bajo estos valores.
3. Se comparará con el IMECA máximo o promedio de cada día del 2019.

## Resultados

### Predicción de partículas por cada hora del día:

#### Datos para entrenar y testear la predicción:
<img src="https://github.com/luisferlc/IMECA-CDMX-Prediction/blob/master/images/train.test.PNG">

#### Predicción de partículas PM10:
<img src="https://github.com/luisferlc/IMECA-CDMX-Prediction/blob/master/images/enfoque%201.2.PNG">

- MAPE alrededor de 40%

#### Predicción de IMECA:
<img src="https://github.com/luisferlc/IMECA-CDMX-Prediction/blob/master/images/imeca%201.PNG">

- 50-70% de similitud con IMECA real.

### Predicción de partículas por día

#### Datos para entrenar y testear la predicción:
<img src="https://github.com/luisferlc/IMECA-CDMX-Prediction/blob/master/images/train.test2.PNG">

#### Predicción de partículas PM10 y PM2.5

<img src="https://github.com/luisferlc/IMECA-CDMX-Prediction/blob/master/images/enfoque%202%20pm10.png">
<img src="https://github.com/luisferlc/IMECA-CDMX-Prediction/blob/master/images/enfoque%202%20pm2.5.PNG">

- MAPE alrededor de 26%-28%

#### Predicción de IMECA:

<img src="https://github.com/luisferlc/IMECA-CDMX-Prediction/blob/master/images/imeca%202%20pm10.png">
<img src="https://github.com/luisferlc/IMECA-CDMX-Prediction/blob/master/images/imeca%202%20pm2.5.PNG">

- 81%-83% de similitud con IMECA real.
