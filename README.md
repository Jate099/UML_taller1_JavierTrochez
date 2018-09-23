# Descripcion del UML_taller1_JavierTrochez
Diagrama de clases para el taller #1 de la clase de ecosistemas de aplicaciones

Aplicacion en eclipse
==============
Main
- Settings():void: Define el tamaño del lienzo de la aplicacion
- Setup():void: Se definen todas las cosas que se deben ejecutan al iniciar el codigo
- Draw():void: Recibe todo lo que se pintara en pantalla ciclicamente
- MousePressed():void: Permite realizar acciones que se realizaran con el mouse
- keyPreseed():void : Permite el uso de las teclas del teclado para realizar acciones

Logica
- Logica(PApplet): Construcctor de la logica
- ejecutar():void: En este metodo van todos los metodos de las clases, los cuales se deben presentar en pantalla o ejecutar
- agregarEnemigo():void: Este metodo agrega objetos del tipo enemigo en areas random del mapa conforme pasa el tiempo
- removerEnemigo():void: Este metodo remueve los objetos de tipo enemigo una vez son derrotados
- agregarRecogibles(): void: Este metodo permite agregar los objetos de tipo recogible
- colision():void: Permite validar cuando un proyectil del jugador toca un enemigo
- dano():void: Permite validar cuando un enemigo choca con el jugador
- clicked():void: permite hacer click sobre elementos

Tanque
- Tank(int x, int y): contructor de la clase tanque
- moverse( ): void: permite mover por el lienzo los objetos que pertenezcan la clase tanque
- disparar( ): void: permite que la clase dispare un arrayliste de proyectiles
- recoger( ): void: permite recoger elmentos
- Morir( ): void: valida cuando el personaje ya no tiene vida
- pintar( ):  abstract void<<abstract>>: Metodo abstracto de pintar de la clase padre "tanque"

Rojo
- Rojo (int x, int y): constructor de la clase rojo que hereda de tanque
- pintar ( ) :void: en este metodo van todos los elementos que vayan a aparecer en la parte grafica de la clase, como imagenes o formas

Azul
- Azul (int x, int y): constructor de la clase Azul que hereda de la clase Tanque
- pintar ( ) :void: en este metodo van todos los elementos que vayan a aparecer en la parte grafica de la clase, como imagenes o formas

Enemigo
- Enemigo(int x, int y): constructor de la clase enemigo
- mover( ): void: permite mover por el lienzo los objetos que pertenezcan la clase enemigo
- atacar( ): void: permite que el enemigo le quite puntos de vida al tanque
- Morir( ): void: valida cuando el personaje ya no tiene vida
- pintar( ):  abstract void<<abstract>>: Metodo abstracto de pintar de la clase padre "Enemigo"

Normal
- Normal (int x, int y):  constructor de la clase Normal que hereda de Enemigo
- pintar ( ) : void: en este metodo van todos los elementos que vayan a aparecer en la parte grafica de la clase, como imagenes o formas

Medio
- Medio (int x, int y):  constructor de la clase Medio que hereda de Enemigo
- pintar ( ) : void: en este metodo van todos los elementos que vayan a aparecer en la parte grafica de la clase, como imagenes o formas

Dificil
- Dificil (int x, int y):  constructor de la clase Dificil que hereda de Enemigo
- pintar ( ) : void: en este metodo van todos los elementos que vayan a aparecer en la parte grafica de la clase, como imagenes o formas

Recogible
- Recogible (int x, int y): constructor de la clase Recogible
- pintar( ):  abstract void<<abstract>>: Metodo abstracto de pintar de la clase padre "Recogible"

Vida
- Vida (int x, int y):  constructor de la clase Vida que hereda de Recogible
- pintar ( ) : void: en este metodo van todos los elementos que vayan a aparecer en la parte grafica de la clase, como imagenes o formas

Daño
- Daño (int x, int y):  constructor de la clase Daño que hereda de Recogible
- pintar ( ) : void: en este metodo van todos los elementos que vayan a aparecer en la parte grafica de la clase, como imagenes o formas

Servidor
- Servidor( ): constructor de la clase Servidor
- run ( ): void: envia los datos obtenidos por los botones al servidor

Receptor
- Receptor(Socket s): constructor de la clase Receptor
- run ( ):void: hilo por el cual se reciben los datos que envia el cliente de android studio

Aplicacion en Android Studio
==============
MainActivity
- Oncreate (Bundle): metodo que ejecuta la aplicacion
- arriba (view): void:  detecta las acciones del boton
- abajo (view): void: detecta las acciones del boton
- izquierda (view): void: detecta las acciones del boton
- derecha (view): void: detecta las acciones del boton

Cliente
- Cliente (activity): contructor de la clase Cliente que recive el elemento activity de la clase MainActivity
- run ( ): void: recibe los datos enviados por parte del servidor
- enviar ( ): void envia los datos de los botones al servidor

Receptor
- Receptor(Socket s): constructor de la clase Receptor
- run ( ):void: hilo por el cual se reciben los datos que envia el servidor
