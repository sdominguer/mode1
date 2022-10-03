# TOMAR MEDIDAS DE:
- ## Centro

### Importamos paquetes
```R
install.packages(statip)
library(statip) 
```

#### Media
```R
media<-mean(CPSSW9204$earnings)
media
```
#### Salida:
[1] 14.26301


#### Mediana
```R
mediana<-median(CPSSW9204$earnings)
mediana
```
#### Salida:
[1] 12.5


#### Moda
```R
moda<-mfv(CPSSW9204$earnings)
moda
```
#### Salida:
[1] 9.615385


- ## Variabilidad
#### Rango
```R
rango<-range(CPSSW9204$earnings)
rango
```
#### Salida:
[1]  1.50000 61.05769


#### Varianza
```R
varianza<-var(CPSSW9204$earnings)
varianza
```
#### Salida:
[1] 60.97475


#### Desviación estándar
```R
desvest<-sd(CPSSW9204$earnings)
desvest
```
#### Salida:
[1] 7.808633


#### Coeficiente de variación
```R
coefvar<-(desvest/media)
coefvar
```
#### Salida:
[1] 0.5474744


- ## Orden
#### Cuantiles
```R
cuantiles<-quantile(CPSSW9204$earnings)
cuantiles
```
#### Salida:
|       0%  |     25%    |   50%  |     75% |     100% |
|-----------|-----------|--------|--------|------------|
| 1.500000 | 8.974359 |12.500000| 17.576495| 61.057690|


- ## Investigación coeficiente de asimetría de Fisher
  - #### Definición: 
  Las medidas de asimetría son indicadores que permiten establecer el grado de simetría que presenta una distribución de probabilidad de una variable aleatoria sin   tener que hacer su representación gráfica. 
  
  - #### Interpretación:
  Mide el grado de asimetría de la distribución con respecto a la media. Un valor positivo de este indicador significa que la distribución se encuentra sesgada       hacia la izquierda (orientación positiva). Un resultado negativo significa que la distribución se sesga a la derecha. Las dimensiones de la caja está determinada por la distancia del rango intercuartílico, que es la diferencia entre el primer y tercer cuartil.
  
  - #### Implementación en R:
  Primero debemos instalar la libreria "e1071" la cual contiene la función skewness que nos da el coeficiente de asimétrica de fisher.
  ```R
  install.packages("e1071")
  ```
  Ahora, utilicemos la función skewness con la variable de salario.
  ```R
  asimetria <- skewness(CPSSW9204$earnings, na.rm = TRUE, type = 3)
  asimetria
  ```
  #### Salida:
  [1] 1.595585
  
  - #### ¿Qué información da el boxplot con relación a la asimetría de los datos?
        - Si la mediana se sitúa en el centro de la caja entonces la distribución es simétrica y tanto la media, mediana y moda coinciden.
        - Si la mediana corta la caja en dos lados desiguales se tiene:
              - Asimetría positiva o segada a la derecha si la parte más larga de la caja es la parte superior a la mediana. Los datos se concentran en la parte                     inferior de la distribución. La media suele ser mayor que la mediana.
              - Asimetría negativa o sesgada a la izquierda si la parte más larga es la inferior a la mediana. Los datos se concentran en la parte superior de la                    distribución. La media suele ser menor que la mediana.
  
  
  


