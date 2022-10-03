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
  - Definición: 
  Se le define como el tercer momento en torno a la media y es la desviación estándar, si la distribución es asimétrica positiva o a la derecha; si la distribución   es asimétrica negativa o a la izquierda.
  
  - Interpretación:
  
  - Implementación en R 
  
  - ¿Qué información da el boxplot con relación a la asimetría de los datos?
  
  
  
  
  


