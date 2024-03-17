Pequeña app que simula un simon says usando canvas para la creacion de la aplicación

1: Sound Manager /Raw directory: Directiorio donde se guardan los archivos de sonido. Sound manager es el encargado de 
gestionar los sonidos, es decir tanto cargarlos como la reproducción

2: En MainActivity se encuentra toda la logica de la aplicacion agena a la gestión de sonidos

3: OnDraw, canva, donde se estrucutra como sera visualmente la aplicación, boton de inicio de juego/ gestión de sequencias
scores... Todo esto solo se pinta en la pantalla, aun no se puede interactuar con ello

4: OnTouchEvent: Se encarga de gestionar los inputs del usuario, por lo tanto de detectar donde se ha clicado, comprobar si 
coincide con la posicion de alguno de los elementos pintados, y en caso de que sea asi, llamar a la lógica que sea necesaria

5: StartGame: crea una nueva partida asegurandose de reiniciar la sequencia que se enseñara en la partida llamando a createGame

6: ContinueGame, solo se llama en caso de que se haya pasado la última sequencia enseñada, simplemente augmenta el numero de
colores en este caso que se van a enseñar, y llama a la función showSequence para que lo haga

7: ShowSequence, se encarga de esenñar las sequencia que el jugador tiene que recordar, tambíen bloquea los inputs del jugador
para evitar problemas

8: HighlightButton: es llamada tanto al clicar un boton, como a la hora de enseñar la sequencia, ilumina el cuadrado grande para
enseñar al jugador que color se ha de tocar en la sequencia, y llama al sonido que corresponda usando la clase SoundManager

9: CompareClick: comprueba el click respecto a la sequencia que se ha de introducir, se encarga tambien de decidir cual es el
siguiente paso en la partida dependiendo de cual haya sido el click, habilitar el continuar, perder, reiniciar juego...
