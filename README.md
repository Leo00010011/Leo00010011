# Hi there 👋

Hola, mí nombre es Leonardo y estoy a punto de graduarme de Licenciatura en Ciencias de la Computación en La Universidad de La Habana

- Tengo experiencia trabajando con Python, C# and C.

- Actualmente estoy trabajando en mi tesis de grado sobre medición de ulceras de pié diabético utilizando Visión por Computadora, Reconstrucción 3D y camaras RGBD intel realsense.

- Estoy interesado en aprender y ganar experiencia en el mundo de la Inteligencia Artificial, específicamente en la Visión por Computadora y la Reconstrucción 3D.

- Me apasiona usar mis conocimientos para ayudar crear un mundo mejor.


<a href = "https://github.com/Leo00010011/Leo00010011/blob/main/CV%20Leonardo%20Ulloa%20Ferrer.pdf"> ➡️ Entra aquí para ver mi curriculum </a>

<h3>Acerca de mis proyectos:</h3>
      <details style="margin-left: 40px">
            <summary>
                  <a href="https://github.com/Leo00010011/my_shell">Shell: </a>Este es un proyecto de la asignatura <b>Sistemas Operativos</b> donde tuvimos que implementar un <b>Shell</b> para <b>Linux</b>, bastante completo, usando <b>C</b>.
                  <div>
                        <img alt="Static Badge" src="https://img.shields.io/badge/C-grey?logo=C&labelColor=white"><img alt="Static Badge" src="https://img.shields.io/badge/linux-grey?logo=linux&logoColor=black&labelColor=white"><img alt="Static Badge" src="https://img.shields.io/badge/bash-grey?logo=gnubash&logoColor=black&labelColor=white">
            </summary>
                  <hr>
                  <p style="margin-left: 40px">
                        Nuestro Shell teniene funcionalidades como <b>multi-pipe</b>, <b>redirección de entrada y de salida</b>, concatenación de comandos, posibilidad de poner procesos en <b>background</b> y <b>foreground</b> y un <b>historial</b> de comandos.
                  </p>
                  <p style="margin-left: 40px">
                        Para interpretar el comando de entrada se parsea y se almacena en una <b>estructura de datos</b> que permite ejecutar cada instrucción de la concatenación <b>secuencialmente</b>, y <b>desacoplando</b> el procesamiento de un "<b>átomo</b>" del comando, del procesamiento de los <b>conectores</b> "&&", "||", ";", "|". Los <b>pipes</b> y las <b>redirecciones de entrada y salida</b> las implementamos trabajando con la <b>tabla de file descriptors</b> y los métodos <b>dup2</b> y <b>pipe</b>.
                  </p>
                  <p style="margin-left: 40px">
                        Los comandos se ejecutan usando nuevos procesos usando los métodos <b>fork</b> y <b>execv</b>. Hicimos un <b>handler</b> para <b>SIGCHLD</b> para <b>cosechar</b> los procesos terminados. Se necesita ejecutar los comandos en procesos separados para que el <b>proceso raíz</b> se quede  manteniendo el <b>estado</b> de la ejecución, pues puede haber conjunto de comandos <b>concatenados</b> o incluso varios procesos ejecutandose en el <b>background</b> en el momento que se pidió el comando.
                  </p>
                  <p style="margin-left: 40px">
                        Para implementar los <b>jobs</b> y el <b>foreground</b> se utilizó una <b>pila</b> para almacenar los procesos en <b>background</b>, la cual se mantiene actualizada con el <b>handler</b> de <b>SIGCHLD</b> y el método <b>waitpid</b> con el flag <b>WNOHANG</b>, siempre teniendo cuidado con las <b>condiciones de carrera</b> que pueden ocurrir. La funcionalidad de enviar un método al <b>foreground</b> se implementó llamando <b>waitpid</b> con <b>pid</b> <b>-1</b>, de forma tal que se iban <b>cosechando</b> procesos hasta que se cosechase el proceso que fue enviado al <b>foreground</b>
                  </p>
                  <p style="margin-left: 40px">
                        El <b>historial</b> se implementó guardando en un archivo la información de los comandos que se iban ejecutando. El formato que diseñamos para esto consiste en siempre escribir el tamaño antes y después los datos es decir (<b>{size}{value}{size}{value}</b>). Size siempre es un <b>unsigned int</b> indicando el tamaño que ocupa su value correspondiente, de forma que se puede leer el archivo facilmente.
                  </p>
                  <p style="margin-left: 40px">
                        Más detalles de la implementación en el <b>readme</b> del proyecto
                  </p>
      </details>
      <details style="margin-left: 40px">
            <summary>
                  <a href="https://github.com/Leo00010011/WebServer-FTP">Web Server:</a> Este es un proyecto de la asignatura de <b>Sistemas Operativos</b>, en el que tuvimos que diseñar e implementar un <b>Servidor FTP</b> solo usando <b>C</b> y funcionalidades del <b>kernel de linux</b>.
                  <div>
                  <img alt="Static Badge" src="https://img.shields.io/badge/C-grey?logo=C&labelColor=white"><img alt="Static Badge" src="https://img.shields.io/badge/linux-grey?logo=linux&logoColor=black&labelColor=white"><img alt="Static Badge" src="https://img.shields.io/badge/networking-grey"><img alt="Static Badge" src="https://img.shields.io/badge/http-grey">
            </summary>
                  <hr>
                  <p style="margin-left: 40px">
                  El objetivo principal de este proyecto era implementar un servidor que permita navegar por un conjunto de carpetas y descargar archivos usando un navegador. Para poder resolver este proyecto nos tuvimos que enfrentar a varios retos: el trabajo con <b>sockets</b>, el protocolo <b>http</b>, mucho trabajo con <b>punteros</b>, manejo de <b>memoria</b> y la <b>paralelización</b> de las funcionalidades. 
                  </p>
                  <p style="margin-left: 40px">
                  El funcionamiento del servidor consiste en aceptar constantemente conexiones y crear un  proceso a parte para atenderlas. Para poder terminar el servidor correctamente implementamos un <b>handler</b> de <b>SIGINT</b> y guardamos el <b>pid</b> de cada proceso creado para poder terminarlos enviando <b>SIGKILL</b> y cosecharlos, pues pueden estar ejecutando algo que demora, como la descarga de un archivo . El cliente puede hacer dos tipos de peticiones: cambiar de dirección o descargar un archivo y esta distinción se hace por un caracter en la <b>url</b>.
                  </p>
                  <p style="margin-left: 40px">
                  Una de las funcionalidades que nos pidieron fue implementar distintas formas de dar orden a los archivos que se muestran, nosotros implementamos 3: ordenar por nombre, ordenar por tamaño y ordenar por fecha de modificación. Quisimos que se pudieran agregar nuevos métodos de ordenación con facilidad, por lo que intentamos <b>desacoplar</b> esta parte del código lo más posible del resto. La mejor manera que encontramos de lograr esto fue que cada método de ordenación fuera un programa que que recibiera la dirección como parámetro y que respondiera el correspondiente respuesta http con el código <b>html</b>. Para poder facilitar esto creamos un conjunto de funcionalidades para generar el diseño de la ventana en <b>html</b> y enviarlo usando el protocolo <b>http</b>. También implementamos un <b>sort</b> que recibe un <b>delegado</b> con el criterio de comparación. De esta forma solo hay que agregar un programa con el nuevo criterio de comparación y reutilizar los métodos que brindamos para crear y enviar la página.
                  </p>
                  <p style="margin-left: 40px">
                  Se hicieron structs para representar los <b>http_request</b> y <b>http_response</b> y los métodos correspondientes para parsear el <b>request</b> y serializar el <b>response</b> para enviarlo. Para leer eficientemente el <b>request</b> se usa un <b>buffer</b> para el cual se creó un <b>struct</b> y varios métodos para leer del <b>socket</b>, como un método remplazando el <b>lseek</b> y otro para leer hasta que se encuentre con cierto caracter. Los <b>header</b> se guardan en una <b>linked list</b> de <b>pair key-values</b>. En el caso de la respuesta, el comportamiento depende de si se quiere descargar un archivo o cambiar de directorio. Para enviar un archivo primero se construye un <b>struct</b> <b>http_response</b> con el <b>request line</b> y los <b>header</b> necesarios, para después de serializarlo y enviarlo, y después se empieza a enviar el archivo con el método <b>sendfile</b>. En el caso de cambiar de directorio se utilizan los métodos de ordenación que fueron comentados que fueron comentados anteriormente.
                  </p>
      </details>  
      <details style="margin-left: 40px">
            <summary>
                  <a href="Por Subir">Skyrim: </a>
 este es el proyecto correspondiente a la asignatura de <b>Ingeniería de Software</b> en el que tuvimos que diseñar una <b>base de datos</b> y una <b>pagina web</b> con la que se puedan recolectar datos de batallas ficticias en el juego y mostrar de manera atractiva varios insights a partir de los datos.
                  <div>
            <img alt="Static Badge" src="https://img.shields.io/badge/python-grey?logo=python&labelColor=white"><img alt="Static Badge" src="https://img.shields.io/badge/django-grey?logo=django&logoColor=black&labelColor=white">
            </summary>
                  <hr>
                  <p style="margin-left: 40px">
                        🚧Writting in progress ...🚧
                  </p>
      </details>
      <details style="margin-left: 40px">
            <summary>
                  <a href="https://github.com/Leo00010011/3Models-SRI">3Models-SRI:</a>Este es el proyecto correspondiente a la asignatura
                  de <b>Sistemas de Recuperación de Información</b> donde tuvimos que estudiar e implementar dos <b>modelos de recuperación de información</b> que permitieran recomendar documentos de una colección a partir de una <b>Query</b>
                  <div>
                        <img alt="Static Badge" src="https://img.shields.io/badge/C%23-grey?logo=csharp&logoColor=black&labelColor=white">
            </summary>
                  <hr>
                  <p style="margin-left: 40px">
                        🚧Writting in progress ...🚧
                  </p>
      </details>
      <details style="margin-left: 40px">
            <summary>
                  <a href="https://github.com/tonycp/IFSL">IFSL:</a>
Este es el proyecto correspondiente a la asignatura
                  de <b>Inteligencia Artificial</b>. Utilizamos <b>Inteligencia Artificial Clásica</b> para desarrollar un simulador de batallas en el que un conjunto de <b>agentes</b> trabajaban en <b>cooperativo</b> para derrotar un enemigo.
                  <div>
            <img alt="Static Badge" src="https://img.shields.io/badge/python-grey?logo=python&labelColor=white">
            </summary>
                  <hr>
                  <p style="margin-left: 40px">
                  El entorno del <b>simulador</b> consiste en una cuadrícula donde algunas casillas son obstáculos. Los <b>agentes</b> tienen características variables, como salud, daño, debilidad,rango de visión y velocidad(cantidad de turnos que necesita para avanzar una casilla). Para implementar el simulador <b>desacoplamos</b> el comportamiento del agente, del comportamiento del entorno, de forma tal que el agente "interactue" con el "entorno" y el "entorno" se encargue de comprobar si la interacción es válida, realizar los cambios en el estado y retornar la información para la retroalimentación del agente. Este simulador lo utilizamos para probar las capacidades de una IA para agentes cooperativos que desarrollamos usando <b>IA clásica</b>.
                  </p>
                  <p style="margin-left: 40px">
                  El problema de explorar el mapa es conocido como <b>Coverage Path Planning</b>. Para resolverlo utilizamos la descomposición de "<b>Boustrophedon</b>" del mapa y modelamos el problema como un <b>Travelling Salesman Problem(TSP)</b> en el grafo de las celdas adyacentes. Para encontrar una solución suficientemente buena utilizamos un <b>algorítmo genético</b> para <b>TSP</b>(Más info sobre la exploración <a href = "https://github.com/tonycp/IFSL/blob/main/Informe.md#explorar-el-territorio-en-busca-de-enemigos">aquí</a>)
                  </p>
                  <p style="margin-left: 40px">
                  El movimiento cooperativo de los agentes presenta varios retos, como lograr que no se obstaculicen unos a otros y a la vez llegen en el menor tiempo posible. Para resolver este problema usamos una adaptación de <b>A*</b>, específicamente Windowed Hierachical Cooperative A* o <b>WHCA*</b>. La idea central es darle un orden de prioridad a los agentes y solo planificar con más exactitud tramos cortos(Más info sobre el movimiento cooperativo <a href = "https://github.com/tonycp/IFSL/blob/main/Informe.md#mover-a-las-unidades-a-sus-posiciones-en-la-formaci%C3%B3n-whca">aquí</a>)
                  </p>
                  <p style="margin-left: 40px">
                  Los <b>agentes</b> usan el movimiento cooperativo para formarse en un lugar pero estos pueden ocupar distintas posiciones en la formación. Para asignar posiciones convenientes diseñamos una función para aproximar cuantas interrupciones iban a tener los caminos óptimos de los agentes. Luego intentamos encontrar la asignación que hace esa métrica 0, modelandolo como un problema de <b>Satisfacción de Restricciones(CSP)</b> y en caso de que no exista intentamos encontrar una buena asignación usando con un algoritmo de <b>Busqueda Local</b>, <b>Stocastic Hill Climbing</b>.(Más info sobre asignación <a href = "https://github.com/tonycp/IFSL/blob/main/Informe.md#asignaci%C3%B3n-de-posiciones-en-las-formaciones">aquí</a>)
                  </p>
                  <p style="margin-left: 40px">
                  Ya formados los <b>agentes</b> y encontrado el enemigo toca mover a la formación, alejándonos lo más posible de los obstáculos, para esto calculamos el <b>Diagrama de Voronoi</b> del mapa y nos movimos por los bordes de las celdas. Para el combate cooperativo generalmente se usa Aprendizaje Reforzado pero necesitabamos una solución con <b>IA clásica</b> por lo que usamos una adaptación de <b>MiniMax</b>(Más info sobre el combate cooperativo <a href = "https://github.com/tonycp/IFSL/blob/main/Informe.md#combate-entre-ej%C3%A9rcitos">aquí</a>)
                  </p>
      </details>
      <details style="margin-left: 40px">
            <summary>
                  <a href="https://github.com/Alejandra1113/FormationDSL/">FormationDSL: </a>
 Este es el proyecto
                  correspondiente a la asignatura de <b>Compilación</b> en el que se diseñamos un <b>Domain Specific Language(DSL)</b> e implementamos un <b>transpilador</b> de ese lenguaje a <b>Python</b>.
                  <div>
                  <img alt="Static Badge" src="https://img.shields.io/badge/python-grey?logo=python&labelColor=white"><img alt="Static Badge" src="https://img.shields.io/badge/compilers-grey">
            </summary>
                  <hr>
                  <p style="margin-left: 40px">
                        Nosotros decidimos crear un lenguaje <b>Turing Completo</b> que permitiera especificar rutinas de formaciones complejas. El <b>transpilador</b> luego generaría el correspondiente código en <b>Python</b> que usara los códigos del proyecto <b>IFSL</b> que acabábamos de terminar para hacer los cálculos y las animaciones.
                  </p>
                  <p style="margin-left: 40px">
                        Para permitirle al usuario crear formaciones con el nivel de complejidad que desée, hicimos que la declaración de formaciones tuviera la sintaxis de un método, en el que pueda pasar parámetros para que el usuario pueda tener mayor reusabilidad del mismo código. Además dentro de la declaración de la formación se pueden usar <b>ciclos while</b>, y condicionales, además de que también puede declarar variables del tipo <b>int</b>, <b>bool</b>, <b>array</b>, y <b>group</b> que es un tipo especial utilizado para referirse a conjuntos de agentes.
                  </p>
                  <p style="margin-left: 40px">
                        Crear nuestro propio lenguaje nos permitió añadir características específicas para el trabajo con
                        <b>groups</b>, creando dinámicas más intuitivas y expresivas con los conjuntos de agentes. Dentro de
                        la definición de una formación el usuario se puede referir a la variable especial <b>G</b>, la cual es
                        el <b>group</b> que va a realizar la formación. Restrigimos la creación de variables de este tipo, de
                        forma que en todo momento estas constituyecen una partición del <b>group G</b> original. También
                        creamos operadores especiales para definir las <b>posiciones relativas</b> entre agentes como si
                        fueran ordenes naturales como "down of" o "all_of G at down of prev".
                  </p>
                  <p style="margin-left: 40px">
                        Para poder compilar el lenguaje tuvimos que definir una
                        <b>gramática</b>, la cual como era de esperar por su complejidad no pudo ser <b>LL(1)</b>.
                        Implementamos un tokenizer con <b>expresiones regulares</b>, un parser <b>LR(1)</b> y aprovechamos su
                        recorrido <b>bottom-up</b> para ir construyendo el <b>Abstract Sintax Tree(AST)</b>. Luego se usa el
                        <b>Patrón Visitor</b> para realizar varios checkeos en el <b>AST</b>, como el checkeo de tipos,
                        checkeo semántico y un checkeo para saber si las variables o funciones que se usan están definidas, y
                        en el caso de las variables se tiene en cuenta el scope donde se llaman. Luego para facilitar la
                        generación de código en Python se realizaron unas transformaciónes en el <b>AST</b> como, renombrar
                        algunas funciones, declarar otras y reemplazar instrucciones como all_of por otras más cercanas a
                        python. El código en python se generó recursivamente usando también el <b>Patrón Visitor</b> y un
                        sistema de plantillas que implementamos usando el módulo de <b>expresiones regulares</b> de python.
                  </p>
      </details>
      <details style="margin-left: 40px">
            <summary>
                  <a href="https://github.com/Leo00010011/Distributed-Twitter/">Distributed Twitter: </a>
                  Este es el
                  proyecto correspondiente a la asignatura de <b>Sistemas Distribuidos</b> en las que se nos pidió
                  realizar una implementación de una versión simplificada de Twitter con las que se debería poder:
                  <div>
                        <img alt="Static Badge" src="https://img.shields.io/badge/python-grey?logo=python&labelColor=white"><img alt="Static Badge" src="https://img.shields.io/badge/docker-grey?logo=docker&logoColor=black&labelColor=white"><img alt="Static Badge" src="https://img.shields.io/badge/networking-grey">
            </summary>
            <hr>
            <p style="margin-left: 40px">
                  Era un requerimiento que las funcionalidades estén listas para un crecimiento de la demanda y la consecuente
                  incorporación de recursos, además de ser capaz de seguir funcionando a pesar del fallo de una cantidad
                  determinada de servidores. Por esta razón optamos por la <b>replicación</b> de servicios y por un
                  <b>almacenamiento distribuido</b> basado en una <b>Distributed Hash Table</b> (DHT).
            </p>
            <p style="margin-left: 40px">            
                  La arquitectura por la que optamos consistía en un conjunto de servidores que hacían de intermediarios entre
                  el cliente y los servicios y otro conjunto que iban a mantener la <b>DHT</b> y la <b>base de datos</b>, los
                  cuales se implementaron para funcionar en <b>procesos</b> separados para lograr un diseño más
                  <b>desacoplado</b>.
            </p>
            <p style="margin-left: 40px">            
                  Por motivos didácticos nuestro equipo decidió implementar todo sin ayuda de alguna librería externa que no
                  sea la que utilizamos para consultar y modificar la base de datos local en SQLite pues no era objetivo del
                  trabajo. Con este objetivo, a base de <b>candados</b>, diseñé para mi equipo un conjunto de clases que nos
                  permitían tener un comportamiento parecido a el de una <b>función callback</b> que era totalmente
                  independiente del contexto en el que era usado(Ver <a href="https://github.com/Leo00010011/Distributed-Twitter#threadholder-y-state-storage">ThreadHolder y State Storage</a>). Siguiendo con la idea de implementarlo todo a mano también hice un objeto que nos permitía a mí y a mis compañeros abstraernos del hecho de que todo se estaba ejecutando en <b>multiples hilos</b> y solo preocuparnos por la función que debía recibir el socket de la conexión a atender. El diseño de este objeto giraba en torno a una <b>multiproducer-multiconsumer queue</b> y nos permitía
                  reutilizar los <b>hilos</b> cuando terminaban de atender a un cliente(Ver <a href = "https://github.com/Leo00010011/Distributed-Twitter/#multithreaded-server">MultithreadedServer</a>).
            </p>
            <p style="margin-left: 40px">            
                  Ya con estas herramientas pude enfocarme en el desarrollo de la <b>Distributed Hash  Table</b> que iba a encargarse de organizar en que servidor se debían almacenar que datos. Para su diseño me basé en la idea  de <b>Chord</b>, pero realicé algunas modificaciones. Su función en el sistema era que el EntryServer le preguntaba a cualquiera de los servidores que estuviera participando en el almacenamiento distribuido por las <b>direcciones IP</b> de los servidores que debían responder por el dato que quería almacenar o consultar. También en el momento de incorporar una replica o un nuevo nodo en el almacenamiento distribuido la <b>DHT</b> jugaba un papel fundamental, pues en el caso de incorporar una replica, la esta se encargaba de encontrar las <b>direcciones IP</b> de las otras <b>réplicas</b> que contenían los datos de los nodos que querían replicar y en el caso de incorporar un nuevo nodo la <b>DHT</b> resolvía las direcciones de las replicas del nodo que iba a ser su sucesor (Ver <a href = "https://github.com/Leo00010011/Distributed-Twitter/   #chord-dht">Chord DHT</a>)
            </p>
            <p style="margin-left: 40px">Para poder probar todo de forma local utilizamos <b>containers</b> de <b>Docker</b> y es mi responsabilidad estudiarme esta herramienta, crear la <b>imagen</b> y un pequeño script para permitir a mis compañeros
            utilizarlo de manera sencilla.
            </p>
      </details>
      <details style="margin-left: 40px">
            <summary>
                  <a>DAA Solutions:</a> 📖 
En estos repos están las soluciones y los respectivos análisis de un conjunto
                  de problemas que formaban parte del sistema de evaluación de la asignatura <b>Diseño y Análisis de
                        Algoritmos</b>
                  <div>
                        <img alt="Static Badge" src="https://img.shields.io/badge/python-grey?logo=python&labelColor=white">
            </summary>
            <hr>
            <ul>
                  <li><b><a href="https://github.com/Leo00010011/DAA-Solution">DAA-Solution: </a></b>Este primer
                        problema es de <b>combinatoria</b>. Para la creación de un tester se implementó un generador de
                        casos y una solución con <b>backtrack</b>, que es menos eficiente pero al menos se conoce su
                        correctitud con facilidad. Como parte del problema se analizó la <b>complejidad</b> y la
                        <b>correctitud</b> de la solución con <b>backtrack</b>. La solución eficiente que se encontró
                        fue hecha usando <b>programación dinámica</b> basada en propiedades de unas particiones en las
                        que dividí en conjunto a contar. La explicación del problema, la solución y las demostraciones
                        están en el readme del repo. (github renderiza mal las notaciones, pero otras herramientas como
                        la extensión de MarkDown de VsCode lo muestra bien)</li>
                  <li><b><a href="https://github.com/Leo00010011/DAA-Solution2">DAA-Solution2: </a></b>Este segundo
                        problema es basado en <b>grafos</b>. Para resolverlo aprovechamos propiedades del recorrido que
                        realiza el <b>Algoritmo de Dijkstra</b> para calcular ciertos valores correspondientes a cada
                        <b>vértice</b> del <b>grafo</b>, para luego acumular los valores correspondientes a los
                        <b>vértices</b> que cumplían cierta propiedad. Para testear los resultados se implementó un
                        generador de <b>grafos</b> aleatorio y una solución que también usa el <b>Algoritmo de
                              Dijkstra</b> pero se basa en una idea más intuitiva. La explicación del problema, la
                        solución y las demostraciones están en el readme del repo.(github renderiza mal las notaciones,
                        pero otras herramientas como la extensión de MarkDown de VsCode lo muestra bien)
                  </li>
                  <li><b><a href="https://github.com/Leo00010011/DAA-Solution3">DAA-Solution3: </a></b>El tercer
                        problema consistía en demostrar la <b>NP-Completitud</b> de un problema de un problema de
                        satisfacibilidad de expresiones booleanas, implementar un solver y encontrar alguna
                        <b>k-aproximación</b>. La NP-Completitud se demostró <b>reduciendo</b> nuestro problema al
                        <b>3-CNF-SAT</b>. Para la solución de nuestro problema decidi usar una reducción conocida de
                        <b>SAT</b> a <b>3-CNF-SAT</b> para generar una expresión equissatisfacible a la original pero
                        que se encuentra en 3ra forma normal conjuntiva y utilizar un solver que aprovecha esta forma.
                        Para obtener esta expresión se tuvo que crear una <b>gramática</b> para expresiones booleanas e
                        implementar un <b>parser LL(1)</b>, pues se necesitaba el <b>árbol de derivación</b> de la
                        expresión. Luego se implementaron 2 algoritmos y se demostró pq eran <b>k-aproximaciones</b> del
                        <b>problema de optimización asociado a nuestro problema</b>. La explicación del problema, la
                        solución y las demostraciones están en el readme del repo.(github renderiza mal las notaciones,
                        pero otras herramientas como la extensión de MarkDown de VsCode lo muestra bien)</li>
            </ul>
      </details>
