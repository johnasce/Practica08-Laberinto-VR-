# Practica08-Laberinto-VR-
Laberinto

 	PRÁCTICA DE LABORATORIO 
### PRACTICA DE LABORATORIO
### CARRERA: Computacion
### ASIGNATURA : Programación Hipermedial
### TÍTULO PRÁCTICA :  Desarrollo de una aplicación de realidad virtual usando la herramienta Unity y desplegada en un dispositivo móvil Android.
### ESTUDIANTE: JOHN HENRY CHIQUI C. ASCE

ACTIVIDADES DESARROLLADAS

 OBJETIVO 

• Experimenta con aplicaciones de realidad virtual. 
• Experimenta con aplicaciones de realidad aumentada. 
• Distingue la diferencia entre tecnologías de realidad virtual y realidad aumentada.

 
1.	Crear la GVR Camera Rig

2.	 Durante este paso, crearemos la cámara VR incluyendo el GvrEditorEmulator en la escena y configurando la cámara. 

1.	Agregue el objeto prefab GvrEditorEmulator a la escena. 

2.	Convierta el objeto Main Camera en un elemento hijo del objeto GvrEditorEmulator.

3.	Restablece el componente Transformar del objeto Main Camera 


4.	Mueva el objeto GvrEditorEmulator a una ubicación conveniente para el desarrollo, por ejemplo, Posición: 0, 3, 35 y Rotación: 0, 180, 0.


5.	Ingrese al modo de juego y use Alt + Mouse y Ctrl + Mouse para rotar e inclinar el ángulo de visión de la cámara.


La cámara esta agregada al GvrEditorEmulator: permitirá ver la escena del juego en un lugar donde incia, y en ves de tilizar la posición que se requeire lo moveré a un punto de incio perzonalizado
 
 
 ![image](https://user-images.githubusercontent.com/51840139/88140629-aff8e700-cbb7-11ea-8773-018997b6b2cb.png)

 

2.	Preparando la escena para la interacción

1. Agregue el objeto prefab GvrReticlePointer a la escena como elemento
secundario del objeto del Main Camera.

2. Aumente el valor de Distancia máxima de retícula para el GvrReticlePointer del
valor predeterminado de 10 a 20.

      3. Agregue el script GvrPointerPhysicsRaycaster como componente en el objeto Main Camera.
4. Agregue el objeto prefab GvrEventSystem a la escena.

5. Ingrese al modo de juego y navegue por la escena haciendo clic en los puntos de
referencia.



1.	El prefab  GvrReticlePointer: esta agregado  como elemento secundario de la MainCamera


 ![image](https://user-images.githubusercontent.com/51840139/88140653-bbe4a900-cbb7-11ea-9ebc-f0c9a2fe4142.png)



1.	Hacer que los objetos del juego sean interactivos
Durante este paso haremos que la Moneda, la Llave y la Puerta sean interactivas añadiéndoles componentes de disparadores y eventos.

2.	Localiza y selecciona el objeto Coin en la jerarquía.
3.	Verifique que tenga un componente Collider.
4.	Agregue el script Coin proporcionado como componente.
5.	Agregue un dispardor de evento (Event Trigger) como componente.
6.	Agregue el evento PointerClick al componente Event Trigger.
7.	Asigne el componente del script Coin al campo de objeto del evento Pointer Click.
8.	Asigne el método Coin.OnCoinClicked () como la función para el evento Pointer Click.
Configuracion de un collider para el prefab Coin.


 ![image](https://user-images.githubusercontent.com/51840139/88140716-da4aa480-cbb7-11ea-8241-9f4e038b19ca.png)

Al momento de hacer click en la moneda sale el mensaje en consola

![image](https://user-images.githubusercontent.com/51840139/88140734-e171b280-cbb7-11ea-8de6-cd13856dfdb5.png)

 
Configuracion para la Key.


 ![image](https://user-images.githubusercontent.com/51840139/88140748-eb93b100-cbb7-11ea-993b-d16986c690aa.png)


Configuracion para la Door

![image](https://user-images.githubusercontent.com/51840139/88140764-f2222880-cbb7-11ea-80d3-89e082c0149b.png)

 
4. Hacer la interfaz de usuario interactiva
Durante este paso, haremos que el objeto SignPost sea interactivo al agregarle componentes de disparadores y eventos. El proceso es casi idéntico al que hicimos con la moneda, la llave y la puerta en el paso anterior, pero no necesitamos un colisionador para interactuar con los objetos del juego de la interfaz de usuario. En su lugar, debemos verificar que el objeto del juego Canvas tenga un componente Graphic Raycaster, y debido a que estamos usando GVR, reemplazaremos el Graphic Raycaster de Unity con el GvrPointerGraphicRaycaster de Google VR.

1.	Localiza y selecciona el objeto del juego SignPost en la jerarquía.
2.	Elimine el componente Graphic Raycaster que se agrega automáticamente al crear un nuevo objeto.
3.	Agregue el script GvrPointerGraphicRaycaster como componente.
4.	Agregue el script SignPost proporcionado como componente.
5.	Agregue un Event Trigger como componente.
6.	Agregue el evento PointerClick al componente Event Trigger.
7.	Asigne el componente script SignPost al campo de objeto del evento Pointer Click.
8.	Asigne el método SignPost.ResetScene () como la función para el evento Pointer Click.

Se Agrego Gvr Pointer Graphic Raycaster y el Script Sign Post
 
 ![image](https://user-images.githubusercontent.com/51840139/88140780-fcdcbd80-cbb7-11ea-96ce-ef4beb30c680.png)


5.Programando el comportamiento de la moneda (coin)

Durante este paso, programaremos el comportamiento de la moneda para que, cuando se haga clic en una moneda (coin),se reproduzca un sonido, muestre un efecto de "poof" y desaparezca.

1.	Hay un mínimo de cinco monedas en el laberinto. Cuando se hace clic en una moneda, se reproduce un efecto de sonido en la ubicación de esa moneda.Cuando se hace clic en una moneda, esa moneda se elimina de la jerarquía de laescena.
2.	Abra el script de Coin y lea todo el script, incluidos todos los comentarios.
3.	Dedique un tiempo a comprender el comportamiento del objeto prefab CoinPoof proporcionado. Puede hacer esto, por ejemplo, ingresando al modo de juego y arrastrando un objeto prefab CoinPoof a la escena.
4.	Programe el comportamiento de la moneda completando todos los comentarios TODO en el script


				Configuracion del Coin para agregarle el Script
        
    ![image](https://user-images.githubusercontent.com/51840139/88140801-08c87f80-cbb8-11ea-8abb-ea61f2c94c62.png)

![image](https://user-images.githubusercontent.com/51840139/88140894-36152d80-cbb8-11ea-9c69-b7f71f5ed0f8.png)




6. Programando el comportamiento de la llave (key)
Durante este paso, programaremos el comportamiento de la llave (key) para que, cuando se haga clic en la llave, reproduzca un sonido, muestre un efecto de "poof" y desaparezca.

1.	Hay un mínimo de una llave en el laberinto. Cuando se hace clic en la llave, se reproduce un efecto de sonido en la ubicación de la llave. Cuando se hace clic en la llave, la llave se elimina de la jerarquía de la escena. Cuando se hace clic en la llave, la puerta se desbloquea.
2.	Abra el script key y lea completo, incluidos todos los comentarios.
3.	Dedique un tiempo a comprender el comportamiento del objeto prefab KeyPoof proporcionado. Puede haceresto, 	por ejemplo, ingresando al modo de juego y arrastrando un objeto prefab KeyPoof a la escena.
4.	Programe el comportamiento key completando todos los comentarios TODO enel script.



Configuracion para progrmar la llave(Key)

![image](https://user-images.githubusercontent.com/51840139/88140908-3b727800-cbb8-11ea-8528-243ce8d00a17.png)


![image](https://user-images.githubusercontent.com/51840139/88140943-46c5a380-cbb8-11ea-8ed3-26e5301f32d3.png)

7.	Programando el comportamiento del SignPost

![image](https://user-images.githubusercontent.com/51840139/88140969-53e29280-cbb8-11ea-811a-05e4fb2efad6.png)


Durante este paso, programaremos el comportamiento de SignPost para que cuando se haga clic en SignPost se reinicie el juego.

1.	El SignPost no se puede ver ni interactuar antes de que se abra la puerta. Cuando se hace clic en SignPost, la escena se restablece a su estado inicial para que el juego se pueda volver a jugar.
2.	Abra el script SignPost y lea todo el script, incluidos todos los comentarios. 
3.	Programe el comportamiento SignPost completando todos los comentarios TODO en el script.




8.	Crear la funcionalidad del juego
Durante este paso, armaremos todo y convertiremos nuestro proyecto en un juego real. Laberinto
•	El laberinto está diseñado de tal manera que el usuario no puede identificar una ruta a la llave desde la posición de inicio.

Waypoints
•	Los puntos de referencia se colocan en todo el laberinto de tal manera que los usuarios pueden navegar desde la posición inicial a todos los objetos del juego con los que se puede interactuar, es decir, todas las monedas, la llave, la puerta y el SignPost.

Monedas

•	Hay un mínimo de cinco monedas en el laberinto.

Llave

•	Hay un mínimo de una clave en el laberinto.

Puerta

1.	La puerta evita que el usuario navegue hasta SignPost hasta que se haya abierto.

SignPost

El cartel no se puede ver ni interactuar antes de que se abra la puerta.
1.	los objetos de juego Maze para diseñar un laberinto.
2.	Mueva el jugador, es decir, el objeto del juego GvrEditorEmulator, a la ubicación de inicio deseada.
3.	Agregue más Waypoints para que el jugador pueda navegar a todas las partes del Laberinto.
4.	Agrega más monedas para que el jugador tenga muchas monedas para coleccionar.
5.	Mueva la llave a una ubicación para que sea un tanto difícil para el jugador encontrarla.
6.	Agregue paredes (cubos) para asegurarse de que los usuarios tengan que navegar para encontrar la llave y las monedas.

![image](https://user-images.githubusercontent.com/51840139/88140980-5ba23700-cbb8-11ea-83a7-dd60d75a51ae.png)
























 










Nombre de Usuario GitHub: johnasce
URl: https://github.com/johnasce/Practica08-Laberinto-VR-.git


RESULTADO(S) OBTENIDO(S):

Creacion de un juego en Virtual Reality.

Correcto funcionamiento de desplazamiento por el mapa

Diversion con desarrollo del juego en unity

CONCLUSIONES:

Con esta practica se consolida lo aprendido en clases y se interactua con diferentes tipos de objetos que ayudan a un mejor aprendizaje de la herramienta Unity.


Nombre de estudiante: John Henry Chiqui C


Firma de estudiante:  
