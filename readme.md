Hola!!
Soy Mario, estudiante de ingeniería electrónica industrial, de la Universidad de Málaga.

Aquí iré subiendo tanto mis proyectos personales, como los que realice en la Universidad.

# 🔋 Construcción de batería LiFePo4
![IMG_20241003_191400](https://github.com/user-attachments/assets/d06b3e95-aa53-49b8-b809-0659b0052233)
## Introducción

En este capítulo se detalla el desarrollo seguido para la construcción de una batería tipo 12S LiFePo4 para Horu. Esta batería permitirá alimentar todo el robot, incluyendo motores de orugas, ordenador, gráfica, etc. Debido a las características mecánicas del robot, esta batería ha debido ser completamente a medida.

Además, se explica la importancia de utilizar baterías LiFePo4 en aplicaciones robóticas, debido a su durabilidad y eficiencia. 

## 🛠️ Materiales usados

Para la construcción de la batería del robot, se ha usado una distribución de celdas 12S. En este caso, se utilizan tres celdas en paralelo, y luego una sucesión de doce de estas en serie. La batería será regulada mediante un BMS de la marca DALY, que se profundizará más adelante.

### 🔋 Celdas LiFePo4

Las celdas LiFePO4 (litio hierro fosfato) son reconocidas por ser más seguras en comparación con otras químicas de baterías de litio (como las de Li-ion o LiPo). Tienen menor riesgo de sobrecalentamiento, explosión o incendio. En total, se utilizarán 36 celdas.

Este tipo de baterías permite una gran cantidad de ciclos de carga y descarga, gracias a la construcción interna de la pila y la estabilidad química del material activo en los electrodos. Esto significa que las celdas son menos propensas a degradarse con el tiempo.

### 🧲 Tira de níquel puro

Para la unión de las celdas en grupos de 3 celdas en paralelo, se ha usado níquel puro, el cual es un gran conductor. El espesor de este material es de 0.25 mm, lo que es idóneo para el método de soldadura utilizado.

## 📐 Cálculos justificativos

### **Capacidad**

Al conectar 3 celdas en paralelo (3P), la capacidad se suma, lo que proporciona:


Capacidad 6000 mAh x 3 = 18000 mAh


### **Voltaje**

La configuración de 12S significa que se tienen 12 celdas conectadas en serie, elevando el voltaje total:


Voltaje = 3.2 x 12 = 38.4V

## ⚙️ Construcción de la batería

### 1. 🔗 Unión de los terminales en paquetes de 3 celdas

![IMG_20240924_161026](https://github.com/user-attachments/assets/c2218f44-aa1c-4f04-bcb6-9e7ad50a2dde)

El método elegido para hacer esta unión entre celdas ha sido la **soldadura por puntos**. Este proceso implica hacer pasar una corriente eléctrica a través de las piezas de metal, calentando el material y aplicando presión para unirlos. 

Asegúrate de que los electrodos del soldador estén posicionados correctamente, de modo que la corriente fluya y genere el calor necesario para unir los terminales.
![IMG_20240924_181653](https://github.com/user-attachments/assets/91cbd631-8891-43cd-8be7-f47ab8e8c39a)

### 2. 🔗 Unión de grupos

Una vez que las tres celdas en paralelo que constituyen un paquete han sido soldadas, se procede a soldar en serie todo el conjunto. Para la soldadura entre dos grupos, se utiliza una tira de níquel como puente entre los terminales de las celdas.
![IMG_20240924_174147](https://github.com/user-attachments/assets/0af7f86b-943a-42a7-b7a9-0f0612fd854e)

Además, se monta una tira de níquel que sobresale de la unión de dos grupos, donde se soldarán los cables del BMS. Esto permitirá medir el voltaje de cada grupo independientemente y detectar errores a tiempo. El BMS también permite monitorear la temperatura de la batería, lo cual es crucial para evitar problemas de sobrecalentamiento.

### 3. 🔌 Conexión de la batería con el BMS

![IMG_20240925_194659_1](https://github.com/user-attachments/assets/71dcdd56-ed69-4583-a4ab-12d479a7ce0f)

El conexionado del BMS con los conjuntos de 3 celdas se realiza utilizando los cables proporcionados por DALY. Se coloca un sensor de temperatura en un punto intermedio de la batería para medir la temperatura de manera uniforme


### 4. 🛡️ Recubrimiento de la batería con termoretráctil

Para un correcto aislamiento de la batería, se utiliza plástico termoretráctil, que proporciona uniformidad al conjunto y un grado de aislamiento extra frente a la humedad y el polvo. Esto es esencial, ya que el robot enfrentará diversos terrenos y condiciones.

Se utiliza una pistola de aire caliente para reducir el material termoretráctil.

![IMG_20241003_182221](https://github.com/user-attachments/assets/67ede893-4768-4b64-b706-bfddaedd06ea)

![IMG_20241003_190142](https://github.com/user-attachments/assets/c3dbee81-1599-4cc1-8781-206d4d54f18a)

---

## 🎯 Batería ensamblada

Finalmente, se puede ver un primer planteamiento de cómo quedará la batería ensamblada:

![IMG_20241003_191405](https://github.com/user-attachments/assets/321576d5-b8dd-4a21-b2c3-e7f22088386c)

## Medidas de DALY BMS

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/user-attachments/assets/b8d19963-4fa1-4343-8888-4651103ccf38" alt="Screenshot_2024-10-01-18-37-35" width="45%">
    <img src="https://github.com/user-attachments/assets/9eb45c25-0096-42f9-aa9e-2db966ad9a6e" alt="Screenshot_2024-10-01-18-39-32" width="45%">
</div>



---
