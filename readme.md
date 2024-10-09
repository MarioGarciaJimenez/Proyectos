Hola!!
Soy Mario, estudiante de ingeniería electrónica industrial, de la Universidad de Málaga.

Aquí iré subiendo tanto mis proyectos personales, como los que realice en la Universidad.


# Construcción de batería LiFePo4

![Batería](IMG_20241003_191400.jpg)

## Introducción

En este capítulo se detalla el desarrollo seguido para la construcción de una batería tipo 12S LiFePo4 para Horu. Esta batería permitirá alimentar todo el robot, incluyendo motores de orugas, ordenador, gráfica, etc. Debido a las características mecánicas del robot, esta batería ha debido ser completamente a medida.

Además, se explica la importancia de utilizar baterías LiFePo4 en aplicaciones robóticas, debido a su durabilidad y eficiencia.

## Materiales usados

Para la construcción de la batería del robot, se ha usado una distribución de celdas 12S. En este caso, se utilizan tres celdas en paralelo, y luego una sucesión de doce de estas en serie. La batería será regulada mediante un BMS de la marca DALY, que se profundizará más adelante.

### Celdas LiFePo4

![Celda 3.2V 6000mAh](image.png)

Las celdas LiFePO4 (litio hierro fosfato) son reconocidas por ser más seguras en comparación con otras químicas de baterías de litio (como las de Li-ion o LiPo). Tienen menor riesgo de sobrecalentamiento, explosión o incendio. En total, se utilizarán 36 celdas.

Este tipo de baterías permite una gran cantidad de ciclos de carga y descarga, gracias a la construcción interna de la pila y la estabilidad química del material activo en los electrodos. Esto significa que las celdas son menos propensas a degradarse con el tiempo.

### Tira de níquel puro

![Tira de Níquel](niquel.png)

Para la unión de las celdas, en grupos de 3 celdas en paralelo, se ha usado níquel puro, el cual es un gran conductor. El espesor de este material es de 0.25 mm, lo que es idóneo para el método de soldadura utilizado.

## Esquemático de la batería

El esquemático de la batería se ha realizado en la plataforma de Fritzing. *[Incluir captura de pantalla o descripción del diseño aquí]*

## Cálculos justificativos

Al conectar 3 celdas en paralelo (3P), la capacidad se suma, lo que proporciona:

\[ 
\text{Capacidad} = 6000 \, \text{mAh} \times 3 = 18000 \, \text{mAh} 
\]

La configuración de 12S significa que se tienen 12 celdas conectadas en serie, elevando el voltaje total:

\[ 
\text{Voltaje} = 3,2 \, \text{V} \times 12 = 38,4 \, \text{V} 
\]

Estos cálculos son fundamentales para entender la duración de la batería y su rendimiento en el robot.

## Construcción de la batería

En esta sección se presentan los pasos seguidos para la construcción de esta batería en las instalaciones de RoboRescue, en la escuela de ingenierías industriales.

### 1. Unión de los terminales en paquetes de 3 celdas

![Unión de celdas](celdas_fila.jpg)

El método elegido para hacer esta unión entre celdas ha sido la soldadura por puntos. Este proceso implica hacer pasar una corriente eléctrica a través de las piezas de metal, calentando el material y aplicando presión para unirlos. 

Asegúrate de que los electrodos del soldador estén posicionados correctamente, de modo que la corriente fluya y genere el calor necesario para unir los terminales.

![Soldador y unión entre celdas](soldador_puntos.png)

### 2. Unión de grupos

Una vez que las tres celdas en paralelo que constituyen un paquete han sido soldadas, se procede a soldar en serie todo el conjunto. Para la soldadura entre dos grupos, se utiliza una tira de níquel como puente entre los terminales de las celdas.

![Conjunto de celdas](Conjunto de celdas.jpg)

Además, se monta una tira de níquel que sobresale de la unión de dos grupos, donde se soldarán los cables del BMS. Esto permitirá medir el voltaje de cada grupo independientemente y detectar errores a tiempo. El BMS también permite monitorear la temperatura de la batería, lo cual es crucial para evitar problemas de sobrecalentamiento.

### 3. Conexión de la batería con el BMS

![Conexión BMS](Conexion interna batería.jpg)

El conexionado del BMS con los conjuntos de 3 celdas se realiza utilizando los cables proporcionados por DALY. Se coloca un sensor de temperatura en un punto intermedio de la batería para medir la temperatura de manera uniforme.

### 4. Recubrimiento de la batería con termoretráctil

Para un correcto aislamiento de la batería, se utiliza plástico termoretráctil, que proporciona uniformidad al conjunto y un grado de aislamiento extra frente a la humedad y el polvo. Esto es esencial, ya que el robot enfrentará diversos terrenos y condiciones.

Se utiliza una pistola de aire caliente para reducir el material termoretráctil.

![Termoretráctil](Termoretráctil_calor.jpg)

### Batería

Finalmente, se puede ver un primer planteamiento de cómo quedará la batería ensamblada:

![Batería en chasis](Batería en chasis.jpg)

---

**Nota:** Asegúrate de que todas las imágenes y figuras están disponibles en el repositorio y que sus nombres coinciden con los utilizados en el texto.
