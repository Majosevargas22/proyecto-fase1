Descripción del Proyecto: Pyroad Driver , Juego 2d de autos creado en Python

Pyroad Driver es un juego desarrollado utilizando la librería Pygame, en el que los jugadores deben controlar un automóvil en una carretera con el objetivo de recoger la mayor cantidad de diamantes posibles, mientras evitan chocar con los autos que circulan por la vía. A medida que el jugador recoge diamantes, el juego se va acelerando, haciendo más difícil esquivar los autos. El juego se presenta con diferentes vistas y funcionalidades interactivas que mejoran la experiencia del usuario.

Funcionalidades del Juego

1.	Vista Inicial del Juego:
o	La primera vista del juego es atractiva y cuenta con un fondo musical que mejora la experiencia inmersiva.
o	El menú principal tiene cuatro opciones:
1.	Jugar: Comienza el juego.
2.	Scores: Muestra los 10 mejores puntajes.
3.	Instrucciones: Proporciona detalles sobre cómo jugar.
4.	Salir: Cierra el juego.

2.	Opción Jugar:
o	Al seleccionar "Jugar", el jugador es redirigido a una pantalla donde debe ingresar su nombre de usuario.
o	Si el jugador intenta continuar sin ingresar un nombre y presiona el botón OK, aparece un mensaje indicando que debe escribir su nombre y tiene la opción de regresar al campo de entrada del nombre.
o	Una vez que se ingresa el nombre correctamente y se presiona OK, el juego comienza en la carretera donde el jugador controla un automóvil que se mueve de izquierda a derecha usando las teclas A (izquierda) y D (derecha).
o	En la parte superior derecha de la pantalla, se muestra el nombre del jugador, la energía restante y la puntuación, que aumenta conforme el jugador recoge diamantes.
o	Energía: Comienza con 100 puntos. Cada vez que el jugador choca contra un auto enemigo, pierde 20 puntos de energía. Si la energía llega a 0, el juego termina.
o	Recoger Diamantes: Al recoger un diamante, se aumenta un punto y se reproduce un efecto de sonido de moneda.
o	Colisiones con Autos: Si el jugador choca con un auto, se produce un sonido de choque y se resta energía.
o	Cuando la energía llega a 0, el juego cambia de vista y muestra una pantalla de "Juego Terminado" con un mensaje que indica que el jugador perdió. También hay un botón de OK que regresa al menú principal.

3.	Opción Puntuaciones:
o	Al seleccionar la opción "Scores", se muestra una lista con los 10 mejores puntajes, junto con el nombre del usuario, los puntos obtenidos, la fecha y la hora en que se alcanzó esa puntuación.
o	En esta vista, el jugador tiene dos botones:
1.	Limpiar los Scores: Borra las puntuaciones almacenadas.
2.	Regresar al Menú Principal: Vuelve al menú principal del juego.


4.	Opción Instrucciones:
o	Al seleccionar "Instrucciones", el jugador ve una pantalla con las reglas y la dinámica del juego.
o	Esta vista tiene un botón para regresar al menú principal.

5.	Opción Salir:
o	La opción "Salir" cierra el juego.

Características Adicionales:
•	Sonidos: El juego incluye efectos de sonido para acciones clave, como el sonido de la moneda al recoger diamantes y el sonido de choque al colisionar con autos enemigos.
•	Interfaz de Usuario: Cada vista tiene botones interactivos que permiten navegar entre las diferentes pantallas del juego.
•	Dificultad Progresiva: A medida que el jugador recoge más diamantes, la velocidad de los autos aumenta, haciendo el juego más desafiante.


Eventos:
Los eventos son una parte central del juego en pygame, ya que permiten que el jugador interactúe con el juego. Algunos de los eventos principales son:
•	pygame.QUIT: Cierra la ventana del juego cuando el jugador intenta salir.
•	pygame.KEYDOWN: Detecta cuando el jugador presiona una tecla.
o	pygame.K_ESCAPE: Detecta si el jugador presiona la tecla Esc para salir o ir al menú principal.
o	pygame.K_a y pygame.K_d: Permiten mover el coche del jugador a la izquierda y derecha, respectivamente.
•	pygame.MOUSEBUTTONDOWN: Detecta si el jugador hace clic con el ratón, útil para interactuar con los botones en el menú o otras pantallas.
 
 Funciones Principales:
•	scores():
o	Muestra los 10 mejores puntajes del juego.
o	Organiza los puntajes en orden descendente y los muestra en pantalla con su nombre, puntaje y un identificador único.
o	Permite borrar los puntajes guardados y regresar al menú principal.
o	Funciona con botones como "Back" y "Clear Score".
•	clearScores():
o	Borra todos los puntajes guardados en el archivo scores.txt y actualiza los datos en el juego.
•	instructions():
o	Muestra las instrucciones del juego, explicando cómo jugar (mover el coche, el objetivo, etc.).
o	También tiene un botón para regresar al menú.
•	enterName():
o	Permite que el jugador ingrese su nombre antes de comenzar a jugar. Si no se ingresa un nombre, muestra un mensaje de error.
o	Tiene botones para confirmar el nombre ("OK") o regresar al menú ("Back").
•	mainLoop():
o	Es la función principal del juego, donde ocurre el bucle principal de ejecución.
o	Maneja el movimiento del coche del jugador, las interacciones con los enemigos, la recolección de objetos y las colisiones.
o	Dibuja los elementos del juego (carretera, coches enemigos, objetos recolectables) y maneja la lógica de las colisiones entre el coche del jugador y otros elementos del juego.
o	Se encarga de cambiar entre pantallas y gestionar las interacciones del usuario.
•	playMusic():
o	Reproduce música de fondo, cambiando la música según la pantalla (por ejemplo, música del menú o música del juego).
•	hud():
o	Dibuja el HUD (Heads Up Display) en la pantalla, mostrando información como el puntaje del jugador, la velocidad, el tiempo o cualquier otro dato importante durante el juego.
•	crash():
o	Gestiona lo que sucede cuando el coche del jugador choca con un enemigo (puede terminar el juego o mostrar un mensaje de pérdida).
•	things():
o	Gestiona lo que ocurre cuando el coche del jugador recoge un objeto (probablemente ganando puntos o algún beneficio).
•	resetGame():
o	Reinicia el juego, restaurando la puntuación y otros datos cuando el jugador comienza una nueva partida.
•	button():
o	Crea y dibuja botones en la pantalla, detectando si el jugador hace clic en ellos. Los botones permiten navegar entre pantallas (por ejemplo, "OK", "Back", etc.).
. 
Estructuras de Datos:
•	data y sortedData:
o	data almacena la información del jugador, incluyendo su nombre y los puntos.
o	sortedData es una lista que contiene los puntajes ordenados para mostrar los mejores puntajes.
•	input_box1:
o	Es un cuadro de texto para que el jugador ingrese su nombre.

 Grupos de sprites:
•	lands_group: Grupo que maneja los objetos relacionados con el fondo de la carretera.
•	enemyCarGroup: Grupo que maneja los coches enemigos que se mueven hacia el jugador.
•	kar_group: Grupo que maneja el coche del jugador.
•	thingGroup: Grupo que maneja los objetos recolectables en el juego.

 Pantallas y Navegación:
•	El juego tiene varias pantallas que se muestran dependiendo de la acción del jugador:
o	Menú principal: Se presenta al iniciar el juego.
o	Pantalla de puntajes: Muestra los mejores puntajes.
o	Pantalla de instrucciones: Muestra las instrucciones del juego.
o	Pantalla de entrada de nombre: Permite al jugador ingresar su nombre antes de jugar.
o	Pantalla de juego: Es donde el jugador juega activamente, moviendo su coche, evitando enemigos y recolectando objetos.
•	changescn(): Función que cambia entre las diferentes pantallas del juego (por ejemplo, de la pantalla de juego al menú principal).
 
 Lógica del Juego:
•	Colisiones:
o	El código maneja las colisiones entre el coche del jugador y otros elementos, como los coches enemigos y los objetos recolectables.
o	pygame.sprite.spritecollide(): Detecta colisiones entre los sprites, como el coche del jugador y los enemigos u objetos.
•	Movimiento del jugador:
o	El coche del jugador se mueve a la izquierda y derecha en la carretera según las teclas A y D.
 Configuración del Juego:
•	screen.fill(): Rellena el fondo de la pantalla con un color específico.
•	pygame.draw.rect(): Dibuja rectángulos en la pantalla (por ejemplo, para los botones o el fondo de las pantallas).
•	pygame.display.flip(): Actualiza la pantalla con los cambios realizados.

