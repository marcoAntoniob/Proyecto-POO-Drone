UTEC - Ciencias de la Computaci´on
Programaci´on Orientada a Objetos I
2018-2 Fecha Elaboraci´on: 19/09/2018
PROYECTO 1
Profesor: Te´ofilo Chambilla A.
1. DESCRIPCION DEL PROYECTO ´
El Departamento de Ciencia de la Computaci´on (DCC) de UTEC en convenio con la
Fuerza A´erea de Per´u ha implementado su laboratorio de f´abrica de Drones de tipo
“DRONE UTEC” que tiene suficiente autonom´ıa.
Las principales caracter´ısticas con que cuenta “DRONE UTEC” son los siguientes:
• Sistema de Comunicaci´on: Para transmitir los datos a una terminal y conectada
a un sat´elite.
• Sistema de Visi´on: C´amara de video para navegaci´on por visi´on computacional.
• Sistema de Sonar: Detector de Obst´aculos (Para evitar choques).
• Plan de navegaci´on: Almacenamiento del plan de navegaci´on formado por coordenadas
(Latitud, longitud) en el plano.
Estos Drones “DRONE UTEC” est´an destinados a la
Programaci´on Orientada a Objetos I
Estas im´agenes ”permitir´an a las autoridades establecer los niveles de afectaci´on al
medio ambiente y la biodiversidad”.
El DCC ya tiene casi listo la primera versi´on de “DRONE UTEC” y realiz´o sus primeras
pruebas en campo habi´endose entrenado para seguir un plan de navegaci´on formado
por coordenadas (Latitud, longitud) en el plano. “DRONE UTEC” es un drone muy
curioso, y no quiere obedecer respecto a su plan de navegaci´on hasta que alguien le
diga cu´antas veces en su camino debe girar a la izquierda y cu´antas veces debe girar a
la derecha, como se muestra en la figura 1.
Por ejemplo, en la figura 2 se muestra la secuencia de los desplazamientos de “DRONE
UTEC” que tiene un plan de navegaci´on compuesto por los siguientes puntos: (0,0),
(0,5), (5,6), y (6,1). De acuerdo a esto, empieza en el punto (0,0) y mirando hacia el
punto (0,5).
Figure 2: Ejemplo de plan de navegaci´on
Programaci´on Orientada a Objetos I
En la secuencia, de la figura 2, se puede observar que realiza dos giros a la derecha
y ninguno a la izquierda. N´otese que en cada ocasi´on que debe girar, se escoge el
´angulo de giro m´as peque˜no posible. En el ´ultimo punto de su recorrido no necesita
girar, simplemente procede a detenerse y descender a tierra. N´otese adem´as que no
necesariamente gira en cada punto. Por ejemplo, si en su trayecto debe ir del punto
(0,0) al (0,1) y luego al (0,2), dado que estos puntos son colineales, por lo tanto no
necesita hacer un giro en el punto (0,1). Se puede suponer que el plan de navegaci´on
no contiene puntos repetidos, y es tal que el “DRONE UTEC” no debe efectuar giros
en 180 grados.
La Fuerza A´erea de Per´u ha financiado el proyecto “DRONE UTEC” y est´a presionando
al DCC para realizar el lanzamiento del primer Drone quien le pide ayuda a su equipo de
desarrollo (programadores) para desarrollar algoritmos que permita generar los planes
de navegaci´on para ambientes desconocidos, desde un punto inicial a uno final. Estos
planes deben ser una lista de puntos en el plano representado mediante matrices
que describen el plan de navegaci´on, considerando que el Drone comienza en el primer
punto de su plan y mirando hacia el segundo punto. Desde ah´ı en adelante, siempre
va de cada punto al siguiente en l´ınea recta. Antes de cada desplazamiento, El Drone
debe girar de manera de estar mirando siempre en la direcci´on en que debe avanzar.
Para este comportamiento, usted debe determinar cu´antas veces El Drone tendr´a que
girar a la izquierda y cu´antas veces tendr´a que girar a la derecha.
2. ENTREGA DEL PROYECTO
El proyecto se entregar´a y se presentar´a el viernes 12 de octubre al buz´on: tchambilla@utec.edu.pe
3. GRUPOS
El trabajo se realizar´a en grupos de 3 integrantes.
4. CRITERIOS DE CALIFICACION
Criterio Puntaje(puntos)
Algoritmo contempla distintas
casu´ısticas que pueden aparecer
durante su programa.
6
Complejidad. Se eval´ua por la
presencia de funciones. 6
Cada estudiante conoce todo el
proyecto y lo sustenta
adecuadamente.
4
Ejecuci´on del Programa. (El programa
se ejecuta adecuadamente y entrega los
resultados esperados)
4
Programaci´on Orientada a Objetos I
5. ALGUNOS EJEMPLOS DE NAVEGACION´
En las figuras 3, 4, 5, 6, 7 se presenta ejemplos de planes de navegaci´on, notese que
estos planes debe ser elaborados mediante matrices y usando el plano carteciano.
Figure 3: Ejemplo de plan de navegaci´on 1
Figure 4: Ejemplo de plan de navegaci´on 2
Figure 5: Ejemplo de plan de navegaci´on 3
6. Recursos
Aplicaciones para planificar el vuelo de tu drone: http://www.aerial-insights.co/blog/6-
aplicaciones-para-planificar-el-vuelo-de-tu-dron/
Programaci´on Orientada a Objetos I
Figure 6: Ejemplo de plan de navegaci´on 4
Figure 7: Ejemplo de plan de navegaci´on 5
