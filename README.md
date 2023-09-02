### Hi there 👋

Hi my name is Leonardo , I’m a senior at University of Havana studying Computer Science

- I’ve experience working with Python, C# and C

- I'm currently working in my thesis degree project about an automated system to measure Diabetic Foot Ulcers with intel
  realsense cameras

- I'm eager to learn and gain experience in Computer Vision and 3D Reconstruction

<details>
      <summary>
            Acerca de mis proyectos:
      </summary>
      <details style="margin-left: 40px">
            <summary>
                  <a href="asdas">Shell: </a>Este es un proyecto de la asignatura <b>Sistemas Operativos</b> donde tuvimos que implementar un <b>Shell</b> para <b>Linux</b> bastante completo usando <b>C</b>.
            </summary>
                  <hr>
                  <p style="margin-left: 40px">
                        🚧Work in progress ...🚧
                  </p>
      </details>
      <details style="margin-left: 40px">
            <summary>
                  <a href="asdas">Web Server:</a> Este es el proyecto de correspindiente a la asignatura de <b>Sistemas Operativos</b> en el que tuvimos que diseñar e implementar un <b>Servidor FTP</b> solo usando <b>C</b> y funcionalidades del <b>kernel de linux</b>.
            </summary>
                  <hr>
                  <p style="margin-left: 40px">
                        🚧Work in progress ...🚧
                  </p>
      </details>
      <details style="margin-left: 40px">
            <summary>
                  <a href="Por Subir">Skyrim: </a> este es el proyecto correspondiente a la asignatura de <b>Ingeniería de Software</b> en el que tuvimos que diseñar una <b>base de datos</b> y una <b>pagina web</b> que la utilice.
            </summary>
                  <hr>
                  <p style="margin-left: 40px">
                        🚧Work in progress ...🚧
                  </p>
      </details>
      <details style="margin-left: 40px">
            <summary>
                  <a href="https://github.com/tonycp/IFSL">IFSL:</a>Este es el proyecto correspondiente a la asignatura
                  de <b>Inteligencia Artificial</b> donde se nos pidió idear un proyecto en el que utilizaramos
                  conocimientos de <b>Inteligencia Artificial Clásica</b>
            </summary>
                  <hr>
                  <p style="margin-left: 40px">
                        🚧Work in progress ...🚧
                  </p>
      </details>
      <details style="margin-left: 40px">
            <summary>
                  <a href="https://github.com/Alejandra1113/FormationDSL/">FormationDSL: </a> Este es el proyecto
                  correspondiente a la asignatura de <b>Compilación</b> en el que se nos pidió diseñar un <b>Domain Specific Language(DSL)</b> y un <b>transpilador</b> hacia al lenguaje de nuestra preferencia.
            </summary>
                  <hr>
                  <p style="margin-left: 40px">
                        Nosotros decidimos realizar un lenguaje que permitiera especificar rutinas de
                        formaciones y que el <b>transpilador</b> generara el correspondiente código en <b>Python</b> que
                        hiciera los cálculos necesarios y mostrara una animación 2D de como se vería la rutina aprovechando el
                        código del proyecto <b>IFSL</b> que acababamos de terminar.
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
                        (Las partes)(Explicacion de tokenicer, parser)Para poder compilar el lenguaje tuvimos que definir una
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
                  <a href="https://github.com/Leo00010011/Distributed-Twitter/">Distributed Twitter: </a>Este es el
                  proyecto correspondiente a la asignatura de <b>Sistemas Distribuidos</b> en las que se nos pidió
                  realizar una implementación de una versión simplificada de Twitter con las que se debería poder:
                  <ul>
                        <li>Registrarse</li>
                        <li>Iniciar Sesión</li>
                        <li>Cerrar Sesión</li>
                        <li>Publicar un Tweet</li>
                        <li>Re-publicar un Tweet</li>
                        <li>Seguir a otro usuario</li>
                        <li>Ver el perfil de otro usuario</li>
                        <li>Pedir nuevos Tweets</li>
                  </ul>
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
                  <b>DAA Solutions:</b> 📖 En estos repos están las soluciones y los respectivos análisis de un conjunto
                  de problemas que formaban parte del sistema de evaluación de la asignatura <b>Diseño y Análisis de
                        Algoritmos</b>
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