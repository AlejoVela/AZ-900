# Curso AZ 900

- **Conceptos Cloud**
    - ¿Qué es la nube?
        
        La computación en la nube como modelo es solo un conjunto de servidores que se ejecutan y tienen las personas que están desarrollando servicios sobre ese hardware.
        
        Capacidad de alquilar en la nube recursos informáticos bajo demanda y en la que solo pagas por lo que usas.
        
    - Responsabilidad Compartida
        1. Building Security
        2. Physical Network Security
        3. Physical Computer Security
        4. Operating System Patches
        5. Network and Firewall Settings
        6. Application Settings
        7. Authentication Platform
        8. User Accounts
        9. Devices
        10. Data
        
        **NOTA:** 
        
        ***Cuando quieres ejecutar un servicio en instalaciones propias, tu eres responsable de toda la lista anterior.***
        
        ***Cuando quieres ejecutar un servicio en la nube usando VM (servidor windows, linux o un servidor básico), eres responsable del rango de la 4 a la 10.***
        
        ***Cuando quieres ejecutar un servicio en la nube de aplicaciones, eres responsable del rango de la 5 a la 10.***
        
        ***Cuando quieres usar un software como servicio, tu eres responsable del rango de la 7 a la 10.***
        
        IMPORTANTE: Cuanto mas alto es el nivel de abstracción menor control tienes, es decir menos responsabilidad
        
    - Nube Publica - Public Cloud
        
        Servicios informáticos ofrecidos por un proveedor externo a través de Internet publica poniendolos a disposición de cualquiera que quiera usarlos o comprarlos
        
        se paga como un servicio por lo que se consume,
        no tiene costos iniciales por infrastructura y es escalable
        
        ***Cualquiera puede usarla***
        
        Servicios informáticos ofrecidos a través de internet o una red privada y solo disponible para usuarios selectos.
        
    - Nube Privada - Private Cloud
        
        ***Propiedad privada, NO cualquiera puede usarla***
        
        Se le llama On-premises
        
        ***NOTA: Hay nubes específicas para los trabajadores del Gobierno***
        
    - Nube Hibrida - Hybrid Cloud
        
        Combinación de una nube publica y una privada. Es decir, mezcla on premises y el uso de algunos servicios de la nube publica.
        
        En el lado privado no necesariamente debe estar lleno se software en la nube si se está ejecutando aplicaciones en su propio hardware, pero luego aprovecha los servicios en la nube para cosas seleccionadas.
        
        Ejemplo. Una base de datos donde tiene instalado un servidor SQL localmente y todos sus datos se están ejecutando local, pero luego necesita tener un conjunto de datos de archivo o necesita hacer copia de seguridad (en nube).
        
    - Cloud Pricing - Precios en Nube
        
        NOTA: Existen al menos 2 o 3 métricas que miden y cobran.
        
        Si se está ejecutando un servicio en sus instalaciones, generalmente el costo se predice fácilmente.
        
        1. Servicios Gratuitos - Free Services
            
            Algunos servicios o son siempre gratuitos o tienen nivel gratuito o son gratuitos por debajo de cierto limite
            
            1. Virtual Network
            2. Private IP address
            3. Azure Migrate
            4. Inbound Internet Traffic
            5. 5GB of Outbound Internet Traffic
            6. Azure Policy
            7. Azure AD
            8. 1 Million Executions Azure Functions
            9. Azure App Service
            
            NOTA: Una ventaja de la nube es que hay cosas que puedes hacer que son gratis.
            
        2. Pago por un tiempo - Pay for Time
            
            Algunos servicios cobran por tiempo.
            
            1. Virtual Machine
            2. App Services
            3. Databases
            4. Load Balancers
            5. Managed Storage
            6. Public IP Address
            
            NOTA: Existen servicios que cobran por minuto o por hora.
            
        3. Pago por GB - Pay per GB
            
            Alguno servicios cobran por Gb usada.
            
            1. Database Storage
            2. Backups
            3. Unamaged Disks
            4. Network trafic (Entre regiones)
            5. Network Trafic (por mas de 5GB por mes
        4. Pago por operación - Pay for Operations
            
            Cada operacion puede tener un costo
            
            1. Unamaged Storage (leer, escribir, eliminar)
            2. Databases (queries)
            3. Messagin
            
            Nota: Cuanto mas usas algo, mas cuesta.
            
        5. Pago por ejecución - Pay per Execution
            
            Si no usas algo, no pagas
            
            1. Azure Functions (consumption model)
            2. Serverless Databases
            3. Messaging Services
            4. Logic Apps (consumption model)
        6. Otras métricas
            
            Si empiezas a buscar, podrías encontrar otras formas de pago en Azure, pero las anteriores son las mas comunes e importantes.
            
        
        NOTA: Hay que tener en cuenta los servicios entre regiones, puede que los servicios que se ejecutan en América del Norte sean mucho mas baratos que los que se ejecuten en America del Sur o Asía, por eso hay distintos costo dependiendo de la región.
        
    - High availability (alta disponibilidad)
        
        Azure tiene un SLA alto, esto se logra a través de la redundancia de los datos, por ejemplo tener varias instacias de una base de datos.
        
    - SLA
        
        Mide la calidad del servicio (disponibilidad, caidas de tiempo, etc) azure suele estar sobre el 99.99% de SLA
        
    - Scalability (escalabilidad)
        
        Capacidad de crecimiento vertical y horizontal de los recursos necesarios (infrastructura) para el funcionamiento del sistema
        
        - Vertical
            
            Incrementando la capcidad de computo, por ejemplo añadiendo más memoria RAM o CPUs
            
            Nota: la escalabilidad vertical tiene un limite, ya que hay restricciones (a nivel de fabricación) sobre por ejemplo, cuanta RAM le puedes añadir a un servidor
            
        - Horizontal
            
            Incrementa la capacidad de computo añadiendo
            más instacias de recursos
            
    - Elasticity (elasticidad)
        
        Capacidad de auto-escalmiento bajo demanda, podemos configurar que al llegar a cierto nivel de utilización de nuestros servicios, se escale horizontal o verticalmente
        
    - Agility (agilidad)
        
        Capacidad de provisionar rapidamente recursos para una app
        
    - Geo-distribution (geodistribución)
        
        Podemos almacenar replicas de nuestros datos en diferentes localizaciónes por si tenemos fallas en alguna o queremos ubicarnos en un lugar especifico
        
    - Disaster Recovery
        
        Se maneja la redundancia al igual que en la alta disponibilidad, disaster recovery permite que a través de un centro de datos alterno e independiente del centro de datos primario, este se active al momento de que el centro de datos principal falle permitiendo que se siga cumpliendo con la disponibilidad del servicio.
        
    - Capital Expenditure (CapEx - Costo de activos, infrastructura fisica)
        
        El capex es un gasto inicial en infrastructura realizado por las empresas que trabajan con infrastructura propia o on premises. Estos activos se deprecian en el tiempo.
        
    - Operational Expenditure (OpEx - Costo Operacional)
        
        Este costo hace referencia a servicios (como netflix o servicios de luz), en estos pagas por lo que consumes. Los servicios en la nube funcionan de esta forma, no pierden la calidad en el tiempo y permiten renovaciones.
        
    - Consumption based model (Modelo basado en consumo, caracteristicas)
        - No tiene costos iniciales
        - No necesitas comprar y administrar infrastructura que los usuarios no utilizarán
        - Tienes la capacidad de pagar por recursos adicionales cuando los necesites
        - Puedes dejar de pagar recursos adicionales cuando NO los necesites
    - Cloud Services Models (Modelos de Servicio en la nube)
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled.png)
        
        - Infrastructure as a service - IaaS (Infrastructura como servicio)
            
            Posee las siguientes caracteristicas:
            
            - Agility: Velocidad de aprovicionamiento
            - Consumption based-model (OpEx model): Pagas lo que usas
            - Elasticity: Crecimiento Horizontal y vertical
            - Management: Los usuarios puede administrar y mantener servicios aprovisionados
            - Skills: No se necesitan habilidades tecnicas para desplegar, usar y obtener beneficios de la nube publica
            - Cloud benefits: Las organizaciones pueden garantizar que sus servicios serán seguros y altamente disponibles en todo momento.
        - Platform as a Service - Paas (Plataforma como servicio)
            
            Más orientado a desarrolladores y al desarrollo de apps
            
            - Tiene las mismas opciones que el modelo IaaS
            - Ofrece más agilidad que el modelo IaaS y no requiere configurar servidores
            - No necesitamos configurar redes, recursos ni maquinas virtuales para nuestras aplicaciones
            - Los desarrolladores pueden enfocarse en el desarrollo sin preocuparse de la infrastructura
            - Acceso a muchas herramientas de desarrollo para todo el ciclo de vida de la aplicacion
            
            **Desventajas**
            Platform limitations: limitaciones de lenguajes, frameworks, dependencias o entornos de desarrollo. No necesarimente significará que si queremos usar un lenguaje no compatible, no podremos usarlo sino que nos veremos en la necesidad de usar el módelo IaaS para configurar todo manualmente.
            
        - Software as a Service - SaaS (Software como servicio)
            
            Aqui pagamos por el software que usamos (al igual que office o netflix)
            
            - Pay-as-you-go pricing model: los usuarios pagan solo por el software que usan
            en el modelo de suscripción que contratan
            - Las licencias suelen ser mensuales o anuales
            - No tiene CapEx
            - Los usuarios pueden acceder a la data de la aplicación desde cualquier lugar
            
            **Desventajas**
            Software limitations: El software ofrecido por las Microsoft muchas veces es dificil de migrar al software ofrecido por la competencia de este, esto suele atar la empresa que lo paga y hace dificil desacoplarce de este.
            
        - Serverless computing (Computo sin servidor)
            
            Es un esquema en el ya no nos precupamos por el ambiente de desarrollo, sino solo nos preocupamos del codigo. Estos se  componen de varios bloques de codigo que esteremos conectando.
            Los bloques deben estan formados por:
            
            - Triggers (Eventos)
            - Azure funtions (funciones)
            - conectores
            
            Por ejemplo, podemos recibir una imagen en trigger que la pasara a la azure funtion que extraera los objetos en la imagen para que la procese. Posterior a esto. será enviada a otra funcion o bloque de codigo que analizará los amigos en comun en la imagen para preguntarte si quieres etiquetarlos (todos estos bloques estarán unido por conectores)
            Esto es llamado "Serverless" por que en teoria no configuramos un servidor o infrastructura para usarlo en nuestros bloques de codigo, pero de fondo, todo servicio de azure usa recursos del servidor.
            
            Nota: El serverless computing, solo se cobra por el tiempo que tarde en ejecutarse nuestro código,
            
    - ¿Que es azure?
        
        Es un conjunto de servicios en la nube que ayuda a las organizaciones a cumplir sus objetivos de negocio.
        
- **Servicios Core en Azure**
    - Gerarquia Básica de Suscripciones y servicios
        - Management groups (grupos de administración)
            
            Nos permite agrupar varias suscripciones, por ejemplo
            suscripciones para qa, produccion o staging.
            Las politicas creadas en los management groups serán heredadas por sus suscripciones que a su vez serán heredadas tambien por sus grupos de recursos y recursos.
            
            Caracteristicas
            
            1. Tenemos un limite de 10,000 management groups en un solo directorio
            2. Un management group puede tener hasta 6 niveles de profundidad, es decir no podemos tener una jerarquía de management groups que superen estos 6 niveles.
            3. Cada suscripción debe pertenecer a un management group y solo puede estar asignado a ese mismo management group.
        - Suscriptions (suscripciones)
            
            Al crear una cuenta de azure, tenemos por defecto una suscripción que pagaremos mes a mes, cada suscripción se factura por aparte y dentro de estas crearemos los grupos de recursos y los recursos de nuestras organización. Estas tambien abarcan cuentas de acceso, usuarios y politicas y tienen ciertos limites o cuotas dependiendo del tipo de suscripción.
            
            - Billing boundary
                
                Puedes crear diferentes tipos de suscripciones y tener un cobro independiente por cada una de estas.
                
            - Acces control boundary
                
                Podemos manejar el acceso de los usuarios y controlar roles en las suscripciones que se ajusten a las necesidades de nuestra organización.
                
        - Resource Groups (Grupos de recursos)
            
            Nos permiten agrupar los recursos, por ejemplo por dominio, si tenemos una aplicación de e-comerce que use maquinas virtuales y storageaccount, podemos separar estos recursos de otra aplicación que use por ejemplo deeplearning y otros tipos de recursos.
            
        - Resources (Recursos)
            
            Todas las instancias de los servicios que podemos crear, editar y eliminar en azure (maquina virtual, almacenamiento, red, etc)
            
        - Azure Resource Manager
            
            Se encarga de aprovisionar los recuros que tenemos, nos permite crear actualizar y eliminar recursos en nuestra cuenta de azure. Poseé caracteristicas como control de accesso, bloqueo de recursos, etiquetas, seguridad y organización para nuestros recursos después del despliege. Podemos usarlo a través de la interfaz grafica de azure portal o a través de Azure PowerShell, Azure CLI y REST clients (Comunicandonos con una API).
            
            Podemos usar templates JSON donde guardemos la configuración de la infrastructura de un servicio y replicarlos cuando queramos usando por ejemplo azure power shell. Aplica control de accesos a los servicios a través de RBAC que esta integrado nativamente.
            
        - Diferencias entre Azure Resource y Azure Resource Manager
            
            Azure resource son los servicios o items que creamos ya sean maquinas virtuales, web apps, databases, networks, etc. Mientras que Azure Resource Manager es el sistema que usa Azure para aprovisionar y en general, administrar los servicios que creamos.
            
    - Caracteristicas de la geo localización de azure
        - Available region (Región disponible)
            
            Regiones habilitadas actualmente
            
        - Announced Region (Región anunciada)
            
            Regiones que estan por construirse
            
        - Availability zones (Zonas de disponibilidad)
            
            Son regiones con más de un centro de datos, esto se hace para proporcionar mayor disponibilidad de los servicios. Tienen la infrastructura aislada entre si para que en caso de tener problemas con un data center, el otro pueda funcionar con normalidad.
            No todas las regiones tienen availability zone, esto se debe a que acarrean un costo extra y a que no todos los servicios son criticos y que pueden ser aprovisionados en lugares sin availability zones.
            
        - Regiones Especiales
            - GOV: Regiones especiales para el gobierno
            - China: Regiones especiales para china (se administran a través de otro proveedor)
            
            Estan regiones se aislan del resto y tienen una infrastructura distinta
            
        - Region Pair (Regiones pares)
            
            Es en sí el mismo concepto de availability zones, pero extendido al nivel de region, es decir, mientras que un availability zone funciona en una sola región, un "region pair" funciona en dos regiones que estan conectadas, de tal forma de que, al tener caidas en una region completa con sus availability zones, seguiremos teniendo disponibilidad en su región par.
            
    - Servicios de Computo Azure
        - ¿Que tanto necesitamos conocer los servicios para el examen AZ-900?
            
            Si dividimos el conocimiento de los servicios en 3 niveles
            
            - Primer Nivel
                
                Conocer el nombre del servicio y su funcionalidad
                
            - Segundo Nivel
                
                ¿Que tanto sabes utilizar el servicio? conocer limitaciones (temas más tecnicos)
                
            - Tercer Nivel
                
                Trouble-shooting, sabemos resolver temas tecnicos relacionados
                
            
            Para este examen unicamente requerimos el nivel 1, de conocimiento en servicios y además saber escoger que servicio es mejor en situaciones especificas.
            
        - Azure virtual machines (Maquinas virtuales)
            
            Simula computadoras fisicas
            Consta de:
            
            1. Sistema operativo
            2. Disco duro
            3. Memoria RAM
            4. Procesador
            
            **Desventajas**
            la VM al tomar recursos completos de un hardware real y no virtual, por ejemplo asignando 8gb de RAM, si usamos solo 1gb, igualmente seguiremos acaparando las otras 7gb para esa maquina virtual por lo que estaremos consumiendo más recursos de los que necesitamos realmente.
            
            - Virtual machine scale sets
                
                Podemos aumentar o disminuir la cantidad de maquinas virtuales bajo demanda de acuerdo a las necesidades de nuestra aplicacíon
                
            - ¿Cuando usar maquinas virtuales?
                1. A través del desarrollo y el testing: este puede ser un ambiente controlado para probar nuestras aplicaciones
                2. Para poder correr aplicaciones en la nube: Muchas veces esto esta relacionado con aplicaciones donde las cargas de trabajo o calculos que realiza son elevadas, por ejemplo, si tenemos una aplicacion on premises para el analisis de datos, si esta maquina corre en un appservices y tarda bastante en generar reportes, esto lo podemos solucionar corriendo la app desde una maquina virtual en la nube, donde realizará este trabajo mucho más rapído agregando más recursos.
                3. Cuando queremos extender los centros de datos en la nube: Si una empresa necesita de más centros de datos, pero el costo de infrastructura para adquirirlos es elevado, puede contratar los servicios de la nube creando recursos adicionales para convivir en un ambiente hibrido.
                4. Durante un distaster recovery: podemos configurar un centro de datos secundario en la nube que almacene
                una copia de nuestros datos on premises. A nivel de costos, tiene la ventaja de que no se nos cobrará nada
                hasta que el centro de datos secundario sea encendido.
        - Azure virtual desktops
            
            Podemos virtualizar equipos para que un usuario final se conecte a este y pueda trabajar sin problemas desde él. Nos permite virtualizar equipos en windows, android, IOS o linux. Tambien es posible accesder a este escritorio virtual desde cualquier parte y desde cualquier dispositivo.
            
            Para muchas organizaciones es más barato habilitar por ejemplo 300 escritorios virtuales para sus trabajadores que adquirir estos 300 equipos y asignarlos, además si después de un tiempo dejan de
            necesitarlos, simplemente pueden inactivarlos.
            
        - Containers and Kubernetes (Contenedores y orquestadores)
            
            A diferencia de una maquina virtual donde vamos a emular todos los aspectos de una computadora, los contenedores, solamente van a emular las dependencias (plataformas o tecnologias necesarios
            para emular una aplicación), solo instalamos lo estrictamente necesario para el funcionamiento de nuestra aplicación y no necesitamos acaparar más recursos de los que necesitamos.
            Podemos escalarlos y apagarlos cuando queramos. Kubernetes nos permite desplegar y administrar (orquestar) esos un grupo de contenedores.
            
            - ¿Cuando usar azure container instance o Azure Kubernetes service?
                
                Los contenedores soporta la arquitectura de microservicios por lo que es muy conveniente usarlo para este tipo de desarrollo.
                Azure kubertes service se encarga de orquestar y crear estos contenedores (o pods), cada pod puede tener un contenedor o más.
                
        - App service
            
            Sirve para construir aplicaciones (ya sean moviles o web), desarrollo de apis y web jobs
            
            - Web APP
                
                Cuando queremos crear una aplicación web, aqui no es conveniente usar una maquina virtual ya que lo unico que requerimos es seleccionar nuestro lenguaje de programación y subir nuestro codigo.
                
            - API APP
                
                Para construir y consumir de una API
                
            - Webjobs
                
                Son pequeños (.exe, Java, PHP, Python, or nodejs) programas o scripts (.cmd, .bar, PowerShell, or bash) que se ejecutan del lado del backend pueden programar tareas a una hora especifica y ejecutar más piezas de codigo.
                
            - Mobile apps
                
                Podemos configurar servicios para las aplicacione mobiles como servicios de notificaciones o construir el backend de una aplicacione  iOS o android.
                
        - Serverless
            
            Ejecutamos aplicaciones basadas en funciones que se accionan a través de eventos.
            No requerimos simular hardware, solo ejecutamos piezas pequeñas de codigo
            
            - Azure funtions (Funciones)
                
                Solo corren pedacitos de codigo que pueden programarse cada cierto tiempo activarse a través de triggers.
                
                1. Deshacernos de la capas de servidores/SO: Con una azure function, nunca hacemos la reserva explicita de un servidor o instacias, es decir, nunca vamos a crear una VM, configurar un SO, instalar aplicaciones o entornos de desarrollo
                2. Even-driven scale (Escala bajo eventos): Permite que el codigo se ejecute solamente cuando el evento se activa, por ejemplo cada cierto tiempo, a través de una solicitud Http, a través de colas y muchas más
                3. Micro-billing(micro costos): Solo pagamos por el consumo del tiempo en el que se ejecute esa funcion, es decir, si nuestra aplicacion se ejecuta en 5 segundos, solo pagaremos el costo de esos 5 segundos.
                Solo pagamos por el tiempo que se ejecute nuestro codigo, si no se esta ejecutando el costo será cero.
            - Azure logic Apps
                
                Es otra modalidad de serverless, permite crear flujos de trabajo de forma visual.
                Funciona a través de conectores o pequeños contenedores que esperan entradas o salidas. Es decir, es una forma más visual de hacer azure functions sin código.
                
    - Networking
        - Azure virtual networks (resdes virtuales de azure)
            
            En azure no manejamos router, moden o switch, sino que usamos redes virtuales para conectar nuestras app o servicios entre si, las caracteristicas más importantes de las virtual networks son:
            
            - Isolation and segmentation: Poder segmentar o aislar aplicaciones o recursos y poder manejar la comunicación
            entre estos.
            - Internet Communications: Comunicación a través de internet
            - Communicate between azure resources: Comunicacion entre servicios de azure
            - Communicate with on-premises resources: Comunicacion con servicios on premises
            - Route network traffic: Redireccionar el trafico de red
            - Filter network traffic: Filtrar el trafico de red
            - Connect virtual networks: Conectar redes virtuales
        - Isolation and segmentation
            - Isolation:
                
                Podemos crear redes privadas o publicas, los recursos dentro de las redes privadas podran comunicarse entre sí y estarán aislados de las demas redes.
                
            - Segmentation
                
                Si queremos partir nuestra red en varios segmentos donde podamos incluir recursos que solo sean capaces de comunicarse con entre sí en el mismo segmento, esto podemos hacerlo a través de la "segmentation"
                
        - Communicate between azure resources
            - Virtual networks:
                
                Las virtual networks no solo comican maquinas virtuales entre si, sino que tambien pueden comunicar otros tipos de recursos como app services, power apps, azure kubernetes service y mucho más.
                
            - Service endpoints
                
                Tu puedes usar un "service endpoint" para conectarte con otro tipo de recuso de azure comolos "Azure SQL databases" y las "storage accounts". Esto permite unir multiples recursos de azure a virutal networks para mejorar la seguridad y proveer un optimo direccionamiento entre los recursos.
                
        - Communiocate with on-premises resources
            
            Permiten la connección entre sitios/recursos on-premise y recursos de azure de forma segura, encriptada y privada. Al ser privada esta información no pasa por internet, por lo que creamos una conneción que solo nosotros podemos usar y nadie más debería poder ver.
            
            - Point-to-site virtual private networks:
                
                Las redes virtuales de punto a sitio funcionan de tal forma que permiten que un recurso que esta en azure pueda conectarse a la infrastructura que esta on-premise. Por ejemplo una app service en azure que requiera de autentificación que sea manejada desde on-premise, el recurso podría conectarse al sitio
                para realizar la autentificación correctamente.
                
            - Site-to-site virtual private networks:
                
                Las redes virtuales de sitio a sitio permiten conectar todo un conjunto de usuarios o recursos de azure con nuestro grupo de recursos on-premises a través de una vpn.
                
            - Azure express router
                
                a través de un cable. Esto nos garantiza tener el maximo ancho de banda disponible con los recursos de ese centro de azure.
                
        - Route network traffic
            - Route tables
                
                Son tablas donde especificamos (dependiendo del destino o origen de los datos) las reglas o saltos
                
            - Border gateway
                
                Este funciona de igual forma que el route tables pero a nivel de una VPN (redes virtuales privadas)
                
        - Filter network traffic
            
            El filtrado de red podemos observarlo comunmente cuando alguien dentro de nuestra organización bloquea ciertas paginas para que no podamos acceder a estas.
            
        - Network security groups
            
            Es el elemento donde de especificamos si dejamos pasar o bloqueamos un trafico de entrada o salida a nuestra red. Esto lo hacemos a través de reglas que configuramos a nivel de puertos o configurando segmentos de red
            
        - Network virtual appliances
            
            Su unica funcion es filtrar trafico, funciona como una computadora que esta entre dos redes el cual esta constantemente revisando el trafico entre estas y determinando de acuerdo a las reglas si les dejara entrar o no.
            
        - Connect virtual networks (peering)
            
            Podemos conectar redes virtuales con otras redes virtuales para poder compartir recursos o simplemente comunicarlas entre si. Por ejemplo si queremos conectar una red "A" con una red "B", necesitamos hacer peering de la red "A" a la red "B" pero tambien es necesario hacer peering de la red "B" a la "A" para que la comunación sea correcta.
            Nota: De forma nativa las redes virtuales estan aisladas entre sí, por ello es necesario el peering.
            
            - UDR (user-defined Routing)
                
                Nos permite manejar tablas de ruteo entre redes virtuales, las tablas de ruteos suelen funcionar solo con redes virtuales aisladas pero con UDR podemos hacerlo tambien entre varias redes virtuales.
                
        - Azure VPN gateway fundamentals
            
            Es un tipo de red virtual que permite conectar recursos de azure con recursos de un centro virtual on-premise
            aparte de site-to-sete y point-to-site, podemos conectar redes a redes.
            Podemos manejar este trafico a través de de politicas donde especificaremos las ips o las direcciones de los
            paquetes para que sean encriptados en la red. La otra manera de hacer esto es través de rutas de forma
            similar a las tablas de ruteo.
            
            - Active/Standby
                
                Por defecto, nos crea una replica secundaria del azure vpn gateway que estará inactiva, al momento de fallar el vpn gateway principal, esta replica secundaria se activara y tomara su lugar permitiendo una alta disponibilidad. Con esta arquitectura podría tardar algunos segundos en levantar la red (hasta 90s en casos
                extremos)
                
            - Active/Active
                
                Funciona similar a la arquitectura active/standby pero en esta ambos vpn gateway estarán siempre activos, aumentando aun más la alta disponibilidad en caso de que uno de los dos falle permitiendo que este disponible la vpn de forma inmediata cuando una de las dos se caiga. (esto puede resultar más costoso)
                
    - Azure Storage
        - Disk storage (Disco de almacenamiento)
        - Azure Storage Service:
        Los servicios de almacenamiento de azure (dejando de lado los discos duros) se dividen principalmente en 4:
        - Azure Blob storage (Servicio de almacenamiento de proposito general)
            
            Podemos almacenar información no estructurada de forma masiva
            por ejemplo videos, musica o archivos con un formato especifico
            para que nuestra aplicación funcione. En el 80%-90% de los casos necesitaremos un blob storage. Blob hace referencia en ingles a cualquier elemento no estructurado.
            Una pregunta común en el examen es si azure blob storage funciona similar a un directorio o carpeta de nuestro equipo, la respuesta esto es un no. 
            
            A pesar de que azure blob storage es una gran solución, no cuanta con un sistema de archivos con el cual podamos organizarlo
            a través de carpetas o directorios logicos. Lo que si tenemos en este caso es una especie de sistema de archivos en el cual en el mismo nombre del archivo podemos irlo segmentando para ir creando una especie de directorios virtuales.
            
            - Azure Blob Tiers
                - Hot Access Tier
                    
                    Esta optimizado para cuando la informacion debe ser accedida de forma frecuente La informacion aqui será almacenada de forma indefinida y su latencia será de milisegundos. 
                    
                    El costo de las consultas es menor pero el costo de almacenamiento es mayor.
                    
                - Cool Access Tier
                    
                    Esta optimizado para que el acceso a la información no sea tan frecuente pero que tampoco se consultara de forma historica La informacion aqui será almacenada hasta por 30 dias y su latencia será de milisegundos. 
                    
                    El costo del almacenamiento cuesta menos pero el costo de consulta es mayor
                    
                - Archive Access Tier
                    
                    Apropiado para informacion o data que será accedida de forma historica.
                    La información aquí será almacenada por 180 dias y su latencia de acceso puede ser hasta de 15 horas.
                    El costo del almacenamiento cuesta menos pero el costo de consulta es mayor que cool tier.
                    
        - Azure File storage
            
            Nos permite crear archivos o servicios de servidores compartidos, esto es parecido a tener en nuestra computadora un disco duro o aun espacio en disco duro de forma virtual.
            
        - Azure Queue storage
            
            Un azure queue nos permite manejar mensajes. Su uso más comun es cuando necesitamos crear una aplicación que se comunica o interactua con otras aplicaciones. Generalmente crearemos un medio de transporte entre estas, en este caso podemos tener un servicio intermediario que puede ser el Queue storage.
            Esto se usa para si tenemos aplicaciones con grandes cantidades de transacciones y necesitamos organizar la información o las solicitudes en un cierto orden y no perder los mensajes.
            
        - Azure Table storage
            
            Podemos almacenar información en forma de una table pero sin ser sql.
            
    - Databases
        - Azure Cosmos DB
            
            Es una base de datos no sql globalmente distribuida (es decir, puede ser accesdido desde cualquier region disponible de azure) y multimodal
            
        - Azure SQL Database
            
            Es el servicio de microsoft para trabajar con bases de datos relacionales de SQL server. Tiene 99.99% de disponibilidad.
            
        - Azure database for MySQL
            
            Es el servicio de microsoft para trabajar con bases de datos relacionales con Mysql.
            Tiene 99.99% de disponibilidad.
            
        - Azure database for PostgreSQL
            
            Es el servicio de microsoft para trabajar con bases de datos relacionales con PostgreSQL.
            La escalabilidad en postgresql funciona implementando un sistema llamado particion o sharding, esto toma las tablas de datos y las divide en varias tablas pero teniendo un apuntador que las une y hace invisible este proceso para el que este consultando en la base de datos.
            Tiene 99.99% de disponibilidad.
            
        - Azure SQL managed instance
            
            Permite migrar la base da datos tal cual esta en una maquina virtual on premise a la nube. Esto involucra crear redes virtuales, almacenamiento, etc. Un termino comun para este tipo de procesos en el lift and shift, este termino se usa para nombrar a servicios que tienen la capacidad de prender y levantar el servicio en la nube.
            Permite realizar una transicion rapida de Iaas a Iaas desde on-premise a la nube.
            
- **Servicios Principales y de administración en Azure**
    - Azure synapse analytics (anteriormente llamado "azure sql warehouse")
        
        Su principal proposito es apoyar los temas de BI permitiendo realizar consultas complejas a una base de datos o almacenar grandes cantidades de información.
        
    - Azure data factory
        
        Tiene como objetivo la integración de flujos de datos, permitiendo el movimiento de estos y su orquestación hacia donde queremos moverlos. Este servicio no guarda nada de información sino que nos permite crea flujos de datos a través de los azure data pipelines. 
        
        Este servicio funciona a través de conectores lo que nos permite no solo conectarlo con otros servicios sino tambien conectarlo con servicios on premise, ademas nos provee de una interfaz grafica para definir nuestros flujos y conectores.
        
    - Azure databricks
        
        Funciona como apache spark pero en AZ permitiendonos procesar, almacenar y utilizar motores analiticos para analizar información a gran escala (como hacemos en temas de big data).
        
        Se usa a través de algunos lenguajes concretos como SQL, Python, scala, R y java.
        
    - Azure Data Lake Storage & Analytics
        - Azure Data Lake Storage
            
            Una vez que analizamos y tranformamos la informamos los datos, estos deben ser almacenados en alguna parte, en esos casos usamos azure data lake storage, que nos permite almacenar estos
            
        - Azure Data Lake Storage Analytics
            
            Es un servicio de analitica bajo demanda al igual que databricks (que depende del formato de apache spark) pero bajo el formato de azure.
            
    - IoT - Internet of Things
        
        Permite a cualquier dispositivo existente, conectarse con internet.
        
        - Azure IoT Hub
            
            Nos permite la recoleccion de mensajes o data proviniente de dispositivos IoT para construir aplicaciones compatibles con dichos dispositivos. Permite que el dispositivo IoT se conecte con Azure y biseversa, ya que azure tambien puede enviar información al dispositivo IoT (Comunicación bidireccional). Esta un poco más orientado al backend.
            
        - Azure IoT Central
            
            Adiferencia de IoT HUB, IoT central nos permite administrar y analizar nuestros dispositivos Iot a través de una interfaz grafica. Es decir funciona como IoT Hub pero con una solución pre-elaborada para que no gastemos tiempo construyendo todo desde cero
            
        - Azure IoT Sphere
            
            Azure Sphere es una colección de servicios que tienen como objetivo crear una solución "end-to-end", es decir, que tanto el dispositivo este hecho para el servicio que lo va a recibir como toda la parte del ecosistema este hecha o mapeada para que nos exista algo que no podamos controlar a través de esta solución. Azure sphere nos provee el
            hardware de dispositivo IoT, So y la capa de seguridad para asegurarnos de que la información se maneja correctamente. 
            
            El sistema operativo de azure sphere es una distro de linux.
            Una de sus caracteristicas más importantes es que puede operar sin estar conectado directamente a internet, de forma que seguira recolectando datos para sincronizarlos una vez tenga conexión
            
    - Machine Learning
        - Azure Machine Learning
            
            Es una plataforma que nos ayuda a crear predicciones a través del machine learning, si hicieramos un homologo con los lenguajes de programación, Azure machine learning seria el lenguaje "C" de los servicio de ML de azure. Se debe provisionar de una data previa para que el algoritmo sea capas de realizar las predicciones.
            
        - Azure Cognitive Services
            
            A diferencia de azure manchine learning en donde empezamos a entrenar y desarrollar nuestros modelos desde cero, azure machine learning ya nos provee de una capa intermedia que nos permite empezar mucho más rapido y poder trabajar con ML sin ser necesariamente un especialista.
            Como desarrollador nosotros definiremos que tipo de servicio queremos usar, ya sea un servicio de lenguaje, de habla de vision de desiciones, etc.
            
            - Language
                
                Podemos hacer que azure analice en por ejemplo el audio de un video para que nos genere los
                subtitulos de este.
                
            - Speech
                
                Tambien este relacionado al lenguaje, aqui podemos por ejemplo, hacer que azure sincronice los subtitulos con la voz de una persona que esta hablando en un video y traducirlo a más idiomas.
                
            - Vision
                
                Podemos identificar objetos dentro de una imagen.
                
            - Desicion
                
                Sobre todo se usa para temas de recomendacion, como los algoritmos de recomendación que usa youtube o netflix.
                
            
            Todas estas funcionan a través de APIs
            
        - Azure Bot Service
            
            Este es un servicio listo para usar en nuestras aplicaicones, implementando un bot framework.
            Por ejemplo, de estos bots es en temas de soporte, cuando queremos delegar las preguntas sencillas a un bot.
            
        - ¿Cuando usar que servicio de Manchine Learning?
            - Si necesitamos un asistente virtual que interactue con una persona? usaremos azure bot service.
            - Si necesitas un servicio que pueda entender el contenido de una imagen, video o audio y traducir su
            text a difrentes indiomas? usamos azure cognitive services
            - Necesitas predecir el comportamiento de un usuario o proveer a usarios con recomendaciones en
            nuestra aplicación?, usamos azure cognitive services
            - Necesitas construir un modelo usando tu propia información o datos para un uso particular de tu empresa?
            usamos azure machine learning
            - utilizaras tu app para predecir los resultados futuros basados en los datos historiales privados?
            usaremos azure machine learning
    - Azure DevOps (herramientas de desarrollo de azure)
        - Azure DevOps Services
            
            Es un SaaS que nos ayuda en todo el ciclo de vide de una aplicación, se compone principalmente de los siguientes servicios:
            
            - Azure Repos: Almacena los repositorios de código (al igual que github)
            - Azure Boads: Funciona como un tablero kanban para gestionar proyectos y HU.
            - Azure Pipelines: Gestiona todo el proceso CI/CD de las aplicaciones
            - Azure Artifacts: Es un repositorio que gestiona los artefactos. Codigo externo de otras organizaciones Como por ejemplo, npm, pip, nuget, etc.
            - Azure Test Plans: Es un servicio de automatización usado para asegurar que los pipelines
            esten siendo ejecutados correctamente. Nos ayuda a conecer los estandares de calidad de nuestros
            despliegues.
        - Github and Github actions
            
            Github es una solución similar azure devops pero más orientada en la colaboración a nivel de open-source.
            
            - Tiene opciones para gestionar tareas a través de un tablero kanban.
            - Al igual que los pipelines de azure devOps, usa algo llamado github actions para el proceso de CI/CD
            - Cuanta con una amplia documentación
            - Puede usarse en la nube o on-premises
        - Azure Dev Test Labs
            
            Se enfoca exclusivamente en testing, creando test automaticos o manuales de pruebas en diferentes ambientes.
            Se apoya mucho del uso de maquinas virtuales u otros servicios a nivel de infrastructura para probar nuestras nuestras aplicaciones, creando laboratorios de pruebas.
            
        - ¿Que servicios de desarrollo usariamos en situaciones determinadas?
            - ¿Necesitas automatizar y administrar laboratorios de test?, usamos Azure Dev test lab
            - ¿Estas construyendo software open source?, usamos github
            - ¿Que tipo de servicio te puede garantizar una granularidad más grande a nivel de permisos?, azure DevOps
    - Configure and Manage Azure
        - Azure Portal/Mobile app
            
            Es toda la interfaz grafica que nos permite acceeder a nuestros servicios de manera visual.
            La aplicación mobile de azure nos permite monitorear recursos o recibir alertas, esta esta más enfocada a dar un vistazo rapido a nuestros servicios en la nube.
            
        - Azure PowerShell/Azure CLI
            
            Al igual que azure portal, nos permite acceder, administrar, eliminar y actualizar todos nuestros servicios, ya no desde una interfaz grafica sino desde una consola de azure power shell desde nuestro navegador o pc windows/linux/mac donde podremos ejecutar comandos y crear scripts.
            Azure CLI funciona de maneara similar a Azure powershell, pero es un terminal totalmente dedicada a temas de azure a difrencia de powershell en donde iremos habilitando con comandos solo lo que queramos usar.
            Nota: la sitaxis de los comandos serán diferentes.
            
        - ARM Templates
            
            A diferencia de la terminal donde creamos scripts, en los templates ARM (Azure Resources Manager) creamos en formato JSON un archivo donde declaramos las caracteristicas y servicios que crearemos.
            
        - ¿Bajo que escenarios usariamos uno u otro de estos servicios?
            - ¿Necesitas realizar una acción administrativa una sola vez u obtener un reporte?, usamos Azure Poweshell/Azure CLI, si bien a través del portal de azure podemos hacerlo, solamente a través de las terminales podemos observar el estado completo de un servicio
            - ¿Necesitas una forma de configurar repetivamente uno o más servicios y asegurarte de que todas las dependencias son creadas en
            el orden correcto? Usamos ARM templates, recomendado para realziar acciones repetitivas.
            - ¿Cuando creamos scripts, que opcion usariamos si venimos de un entorno como windows?, Azure powershell o CLI
    - Monitoring - Monitoreo de servicios
        - Azure advisor
            
            Advisor es un servicio gratuito que nos ayudara a obtener recomendaciones y evaluar los servicios que actualmente tenemos actualmente dentro de la plataforma para mejorar ya sea la:
            
            1. Reliability (Fiabilidad): La manera en que nosotros aseguramos que un servicio se comporte de una forma determinada
            2. Security (Seguridad): Detectar amenazas que puedan llegar a ser un peligro para nuestro ambiente (funciona como un complemento
            de azure security center, pero su diferencia principal es que azure advisor es un servicio gratuito)
            3. Performance: Que tanto podemos optimizar los recursos de por ejemplo, nuestras maquinas virtuales
            4. Cost (Reducir Costos):Aqui podemos observar como reducir costos, por ejemplo de servicios que no utilicemos
            5. Operational Excellence(Escelencia operacional): Da recomendaciones sobre configuración, estado deseado, eficiencia y buenas practicas
            para nuestros servicios activos actualmente.
            
            Nos da un panorama más general de lo que podemos mejorar, a diferencia de azure security center que se centra en temas más especificos de seguridad.
            
        - Azure Monitor
            
            Es una plataforma que tenemos en azure para recolectar, analizar y visualizar decisiones basadas en la información (logs) que generan los demas servicios que tengamos activos en la nube. Tambien podemos usarlo de forma on-premise instalando un agente en nuestro data center. 
            
            Este es un servicio tambien orientado a proposito general a diferencia de azure sentinel que es un servicio totalmente enfocado a la recoleccion de datos y eventos de seguridad.
            Podemos alamacenar información de;
            
            1. Insights: Información de aplicaicones como rendimiento o patrones
            2. Visualize: Permite visualizar la información que recolectamos y presentarla en dasboards
            3. Analyze: Podemos analizar esa información
            4. Respond: Podemos a apartir de ciertas alertas que genere la aplicación, responderle a nuestros usuarios o autoescalar los recursos
            5. Integrate: Podemos intregrar la información de los logs a través de logic apps u APIs propias.
        - Azure Service Health
            
            Como tal no es un servicio disponible en azure sino es un dashboard que nos muestra el estado de nuestros servicios al rededor del mundo, esto nos permitira visualizar de forma sencilla si hay alguna incidencia en nuestros servicios a nivel de azure de forma global o en ciertas regiones.
            
            - Service issues: Problemas que este presentando azure que puedan afectar nuestros servicios.
            - Planned maintenance: Eventos de mantenimiento que pueden afectar la disponibilidad de nuestros servicios desde aqui nos avisará el equipo de microsoft si tiene mantenimientos planeados.
            - Health advisories: Sugerencias para serguir teniendo nuestros servicios en optimas condiciones.
        - ¿Cuando usar uno u otro de estos servicios?
            - ¿Si necesitamos analizar como estamos usando azure para reducir costos, mejorar la seguridad o la resilencia?
            Usamos azure advisor.
            - ¿Si queremos monitorear el estado de nuestros servicios?
            Usamos azure monitor o azure service health
            - ¿Si quieres medir a través de eventos personalizados eventos a través de metricas?
            Usamos azure monitor
- **Servicios principales de red seguridad en Azure**
    - Azure Security Center
        - Permite monitorear la seguridad a través de todos los servicios que tengamos activos, esto incluye tambien los servicio on-premises
        - Automaticamente aplica configuraciones a los recursos apenas sean creados
        - Provee recomendaciones de seguridad para nuestros recursos
        - Podemos revisar dentro de nuestras maquinas virtuales en busca de malware a través de una inteligencia artificial
        - Se conecta con nuestra configuración de red para tener acceso inmediato para el bloqueo de puertos de red.
        - Recomienda como podemos mejorar la seguridad de nuestros servicios.
        - Maneja un puntaje de seguridad (secure score) para saber que tambien tenemos nuestros servicios protegidos.
    - Azure Sentinel
        
        Provee una solución de SIEM (Security Information and event Management) en la nube. Permite a una organización recolectar información de eventos de seguridad para tenerlos de forma centralizada, posterior momente podemos analizar esta data con herramientas que nos permite atacar estas fallas de seguridad.
        
        - Recolecta datos de la nube
        - Detecta y analiza los falsos positivos a través de herramientas de inteligencia artificial
        - Responde rapidamente a los incidentes
        
        A difrencia de azure security center que funciona más como un dashboard o panel de control donde visualizamos recomendaciones, con azure sentinel es un servicio enfocado a recolectar datos o logs de todos los servicios que estamos utilizando para después empezar a analizarlos y encontrar patrones que puedan generar problemas de seguridad. 
        
        SIEM puede incluirse en otros servicio o nubes como aws, citrix VMware, entre otros.
        
    - Azure Key Vault
        
        Nos permite administrar certificados, passwords y cualquier otro tipo dato como si fuera una bobeda secreta (parecido a los secrets de github)
        
        - administra secrets
        - administra llaves de encripción
        - administra certificados SSL/TLS
        - Almacena secretos HSMs (hardware security modules)
    - Azure dedicated host
        
        Permite tener recursos almacenados y funcionando en un servidor dedicado, es decir, en un servidor dedicado tendremos toda la caja fisica reservada para nostros en vez de estarla compartiendo con otros clientes. Esto puede ser util cuando queremos tener todos los recursos aislados (por ejemplo para recursos del gobierno). Una ventaja de esto es que podemos configurar los servidores fisicos como queramos y asignar a una maquina virtual el numero de ram y nucleos a libertad.
        
    - Seguridad de red
        - Defense in depth
            
            El termino defense in depth hace referencia a que nos preocuparemos de la seguridad de todas las capas del modelos OSI, es decir:
            
            - Capa fisica: nuestros centros de datos fisicos u oficinas
            - Capa identidad y acceso: politicas de autentificación y autorización
            - Capa de perimetro: permite detectar ataques de ddos
            - Capa de red: Control de accesos, segmentación de red, etc.
            - Capa de aplicación: Maquinas virtual, que tengan control de acceso y segmentación
            - Capa de datos: Todos los datos de nuestra organización que debemos proteger
        - Azure firewall
            
            Un firewall es un dispositivo de seguridad a nivel de red que nos ayuda sobre todo a centralizar la forma en la que filtramos el trafico  a través de internet o internamente en nuestras redes. El firewall nos ayuda a generar reglar para porder permitir o denegar trafico de salida o entrada. El firewall y los networks security groups se complementan entre si. El primero es un servicio completo dedicado con herramientas para analizar y monitorear todo el trafico de red mientras que los networks security groups nos permiten filtrar el trafico de red basado en ciertas reglas por lo que podría considerarse un subconjunto de azure firewall.
            
        - Azure DDOS Protection
            
            Un ataque ddos funciona cuando un atacante envia desde varios  computadores alrededor del mundo muchas peticiones http a un servicio
            para colapsarlo. Azure ddos protection nos ayuda a proteger nuestros servicioos de estos ataques DDoS tratando de identificar las solicitudes que entran a nuestro servicio para identificar si son o no ataques de DDoS.
            
            - Identifica ataques volumetricos
            - Ataques a nivel de protocolo
            - Ayuda a proteger la capa de aplicaciones con un web application firewall, la cual nos ayuda a identificar ataques a nivel de aplicación
- **Servicios de Identidad, gobierno, privacidad y cumplimiento en Azure**
    - Diferencias entre autentificación y autorización
        
        Atentificación: es el proceso que establece la identidad de una persona o servicio que quiera acceder a un recurso Autorización: Una vez identificado, la autorización define cuales son los recursos a los que tiene acceso esa persona
        dependiendo de su rol y tipo de usario Intraducción a azure AD (Azure active directory)
        
    - Introducción a azure AD (Azure active directory)
        
        Es el servicio de administración de identidad que permite a los usuarios logear y acceder a las aplicaciones de la nube de microsoft y a las aplicaciones que nosotros desarrollamos en la nube. Este servicio es un SaaS 
        
        **¿Cual es la diferencia de Azure AD y Active directory?**
        Active directory funciona de forma on-premise, mientras que azure active directory funciona en con nuestros servicios en la nube y aplicaciones
        que desarrollamos y permite conectarse con las aplicaciones on-premises.
        
        - Servicios en Azure active directory
            - Autentificación
            - Single sign-on: loggearnos entodas las plataformas y recursos de azure a través de unas mismas credenciales, en lugar de manejar una por cada uno de nuestros servicios.
            - applications management: Permite a través de azure ad, gestionar aplicaicones creadas en azure o aplicaciones de terceros
            - Device management: Permite administrar recursos o quipos que no esten conectados a la red corporativa.
        - Azure AD Connect
            
            Nos permite conectar directorios activos locales con Azure active directory (En la nube). Es decir, sincronizamos nuestra identidad on-premise con nuestra identidad en la nube.
            
    - Factor multiple de autentificación MFA
        
        MFA tienes tres pilares fundamentales:
        
        - Something the User knows - algo que el usuario conoce, como una contraseña o pin
        - Something the user has - algo que el usuario tiene, como un telefono o un email
        - Something the user is - algo que el usuario es, como huella digital o rasgos faciales
    - Conditional Access - Acceso Condicional
        
        Es una herramienta que permite garantizar el acceso o no a ciertos recursos dependiento de ciertas condiciones que se cumplan indiferentemente del dispositivo en el que se acceda.
        
    - Ofertas Azure AD
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%201.png)
        
        Posee direntes tipos de ofertas/variantes:
        
        - Version gratuita
            - Protección MFA y acceso mobile como segundo factor
        - Integrado en office 365 o Azure AD Free- Global administrators only
            - Mismas caracteristicas que la Version gratuita
            - Incluye llamadas como segundo factor de autentificación
            - SMS como segundo factor de autentificación
            - Administración de controles sobre los metodos de verificación
            - Recuerda MFG para dispositivos de confianza
        - Azure AD P1 (premium 1) o Azure AD P2 (premium 2)
            - Mismas caracteristicas que Integrado en office 365
            - reportes MFA y fraud alerts
            - Custom greeting for phone calls and custom caller ID for phone calls
            - IPs de confianza
            - MFA para aplicaciones on-premises
- **Servicios de administración de costos y niveles de servicio en Azure**
    - Azure role-based access control - RBAC
    - Etiquetas
    - Azure Policy
    - Azure blueprint
    - Azure cloud framework
        
        Es una estrategia para organizar la forma en la que desplegaremos servicios en azure. Nos permite definir como estaremos realizando la migración de nuestros servicios a azure. Conta de los siguientes pasos:
        
        1. Define your strategy
            - Define y documenta tus motivaciones
            - Resultados basados en negocio
            - Evalua consideraciones financieras
            - Entender consideraciones tecnicas
        2. Make a plan
            - Estado digital: crea un inventario de tus recursos digitales
            - Alineamientos organizacioneles: Asegurate de que los stake holdes tengan pleno conocimiento sobre las nociones de la migracion
            - Skills readiness plan: Se debe tener en cuenta el conococimiento del equipo sobre azure para poder solventar los vacios de habilidades que se tengan
            - Pland de adopción de la nube: Como adaptaremos nuestras operaciones para convivir con servicios en la nube o servicios hibridos
        3. Ready your organization
            - Azure setup guide
            - Azure landing zone
            - expand the landing zone
            - best practices
        4. Adopt the cloud
            - Migra tu primera carga de trabajo
            - Escenarios de migracion
            - buenas practicas
            - Mejorar proceso
            - evaluar el valor que nos proporcionan los servicios de azure
            - guia de innovationd de azure
            - buenas practicas
            - feedbacks
        5. Govern and manage your cloud enviroments
            - Methodologia
            - mediciones (benchmarks)
            - base de gobernanza inicial inicial
            - mejorar la gobernanza inicial
            - establecer politicas, controles y accesos
    - Seguridad y privacidad de Azure
        
        Microsoft Privacy statement: aqui microsoft nos dice que nuestros datos serán recolectados para temas de mejoras en nuestros servicios.
        Online services Terms: Como se manejan temas como consumo de datos, fallas de servicios y SLA.
        Data Protection Addendum: Explica como azure, en cumplimiento con las leyes de otros paises, usa la información recolectada solo para propositos de mejorar sus productos. Ademas de politicas, niveles de encriptación y temas de seguridad.
        
    - Azure government y China
        
        Azure government fue creado especificamente para cumplir las necesidades y reglamentaciones necesarias para el gobierno de estados unidos, de igual forma Azure china 21Vianet fue creado para el manejo de azure en el gobierno chino. Como dato adicional, por reglamentación china, los data centers de azure en china sonadministrados por una empresa nacional y no  por el propio azure.
        
    - Consejos para reducir consumo en Azure
        
        Hay 5 caracteristicas principales que influyen en el costo:
        
        1. Tipos de recursos
        2. Uso de recursos
        3. Tipo de suscripción de azure
        4. Localización
        5. Ancho de banda
        - Podemo usar la calculadora de azure
        - Podemos usar azure advisor y limitar nuestro uso, configurando que se apaguen los recursos después de llegar a cierto nivel de uso.
        - Podemos pagar varios años por adelantado y microsoft nos ofrecerá descuentos
        - Es importante saber donde ubicamos nuestros recursos ya que todas las ubicaciones no tienen el mismo costo
        - Podemos suscribirnos a las notificaciones y boletines de azure para estar atentos a las promociones
        - tra estrategia seria migrar servicios de IaaS a PaaS
        - Podemos usar licencias propias para evitar el uso de rentas de licencias en la nube o usar distros de linux
    - Que es el TCO - Total Cost of Ownership
        
        A través de la calculadora de microsoft, nos da una idea estimada segun ciertos escenarios de los costos que podriamos tener con los servicios que vayamos a configurar
        
    - Tipos de suscripciones
        - Free trial
            
            Suscripción de prueba de 30 días, podemos usar los servicios de azure de forma gratuita.
            Adionalmente, una vez terminados los 30 días, azure nos permite usar servicios gratuitos por 1 año sin cobrarnos por el consumo generado de estos.
            
        - Pay-as-you-go
            
            Es el modelo usado para cualquier usuario o pequeña empresa.
            
        - Member offers
            
            Ofrece credito para ciertos servicios. Se usa por ejemplo para instituciones educativas o para partners de microsoft
            
        - Suscripción enterprise
            
            Para aquellas organizaciones que nesecitan muchos recursos de azure.
            
        - Directamente desde la web
            
            Compras servicios directamente desde la pagina de azure portal y pagas los precios estandar por ellos.
            
        - Proveedor de soluciones de nube
            
            Un partner o empresa certificada por microsoft puede ser contratada para que pueda crear y administrar tus suscripciones.
            
        
- **Extra: Preguntas Interesantes en examentes de practica**
    - Estas en una entrevista para ingresar a la empresa como un “Azure Administrator” y necesitas describir las regiones
        
        ¿Cuales 3 descripciónes son más las más indicadas para las Azure Regions?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%202.png)
        
        1. Las regiones siempre se entan pareadas con otras regiones
        2. Cada región contiene uno o más datacenters}
        3. Las regiones especifican la localización de un recurso
    - Para cada una de las siguientes afirmaciones sobre “Azure Networking”, seleccione “Si” si la oración es verdadera, de otra forma escoja “No”
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%203.png)
        
        1. ¿El trafico de red del “ExpressRoute” es direccionado a través de una conneción privada?, Esto es verdadero
        2. ¿El trafico entre redes virtuales que tienen configurado un “Peering” entre sí, es direccionado sobre la internet publica?, Esto es falso
        3. ¿Una VNET (red virtual) es creada dentro del scope (ambito) de una región?, Esto es verdadero
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%204.png)
        
    - Application Security Groups te permite:
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%205.png)
        
        Organizar applicaciones y servidores similares para poder aplicarles posteriormente y de forma sencilla politicas a estos grupos
        
    - ¿Cuales caracteristicas de monitoreo usarías para cada escenario?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%206.png)
        
        Necesitas saber cuantas veces tu web app ha presentado indisponibilidad durante el mes pasado: Usas Health History
        
        Quieres que tu y tu equipo reciban mensajes de texto cuando azure presente mantenimientos programados: Usas Health alerts
        
        Quieres ver las caracteristicas de Azure que estan por volverse obsoletas: Usas Health Advisories
        
    - Tu compañia esta consuderante mover sus servicios e infrastructura on-premises a Azure. Sin embargo, antes de hacerlo tu quieres conocer el ahorro en los costos (Si es que los hay). ¿Qué herramienta usarías?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%207.png)
        
        Total Cost of Ownership (TCO) calculator: Esta es la opción que debes escoger, ya que te permite comparar la diferencia entre los costos actuales de la infrastructura on-premises y predecir los costos que tendrás con la infrastructura en la nube.
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%208.png)
        
    - Estas investigando las metodologias de gobernancia en Azure y  quieres entender el acceso basasdo en roles (RBAC), politicas (policies),  iniciativas (initiatives) y locks (bloquos) ¿Qué herramienta usarías para cada escenario?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%209.png)
        
        Quieres asegurate de que solo las maquinas virtuales con cierto tamaño defiunido sean desplegadas en un grupo de recursos: Defines una politica (policy)
        
        Quieres administra una colleción de politicas: Usas iniciativas (initiative)
        
        Quieres prevenir que las maquinas virtuales sean eliminadas por cualquier pesona despupes de que estas sean desplegadas: Usas un bloqueo (lock)
        
    - Marca cada uno de los beneficios de la computación en la nube con sus respectivas descripciones
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2010.png)
        
        Manualmente incrementas o decreamentas los recursos siendo concientes de que estos tendrán una sobre carga de trabajo: Escalabilidad (Scalability)
        
        Automaticamente incrementas o decrementas recursos bajo demanda: Elasticidad (Elasticity)
        
        Velocidad y flexibilidad de asignación y desasingación de recursos requiridos: Agilidad (Agility)
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2011.png)
        
    - ¿Qué herramienta grafica de azure provee una interfaz grafica para desplegar, administrar y monitorear nuestros recursos?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2012.png)
        
        El portal de azure
        
    - Tu compañia usa “Azure Blueprints” para facilitar su migración a Azure. El Usuario definido como “User1” debería ser capaz de asignar  “Blueprints” publicados. Tu necesitas asignarle al “User1” el RBAC (rol-based access control) necesario para proveer estos permisos. ¿Qué role deberías asignarle al “User1”?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2013.png)
        
        Seleccionamos el rol de “Bluepruint Operator”, ya que los usarios con este role puede assignar “Blueprint” existentes que han sido publicados pero ellos no podrán crear sus propios bluprints.
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2014.png)
        
    - ¿Qué oración describe mejor lo que el recurso “Lock” hace a una maquina virtual?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2015.png)
        
        El recurso “Lock” previene que una maquina virtual sea eliminada.
        
    - Tu mueves algunas maquinas virtuals con windows server desde tu infrastructura on-premises a azure. Las maquinas virutales que tienes on-premises están autorizados por el acuerdo de garantía de software de Microsoft activo de su empresa. Tu necesitas reducir el costo de tus maquinas virtuales ¿Qué deberías hacer?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2016.png)
        
        Deberías la configuración de beneficios de Azure hibrido (Azure hibrid benefit)
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2017.png)
        
    - ¿Cuales 2 opciones son ejemplo de “Conditional access policies”? (politicas de acceso condicional)
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2018.png)
        
        Require compliant devices: Verifica si accedes desde un dispositivo de confianza
        
        Block access by location: Si se detecta que accedes desde una localización totalmente alejada de la localización en la que accediste hace poco, bloqueará el acceso a la cuenta
        
    - Estas planeando mover las aplicaciones web de tu empresa a Azure y quires usar las caracteristicas de seguridad que ofrece azure. Necesitas entender la diferencia entre autorización y autentificación.
        
        Para cada oración selecciona verdadero/false dependiendo del caso.
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2019.png)
        
        La autentificación asegura que la combinación de correo y contraseña son correctos: Esto es verdadero
        
        La autorización asegura que una cuenta tiene suficientes permisos para acceder a un recurso: Esto es verdadero
        
        La autentificación puede usar certificados para identificar a una persona o servicio: Esto es verdadero
        
        La Authorización puede usar contraseñas para identificar a una persona: Esto es falso
        
    - ¿Cuál solución de seguridad de Azure provee recomendaciones generales de seguridad y sugerencias para mejorar la seguridad de tus recursos?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2020.png)
        
        Microsoft defender for cloud provee recomendaciones de seguridad y sugieres acciones a tomar en cuenta. Esta diseñado para ayudarte a proteger los recursos de la nube de azure, nubes que no son de azure y nubes hibridas a través de un set de herramientas de seguridad.
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2021.png)
        
    - Para mejorar el desempeño de una aplicación critica, tu organización implemento “Cloud bursting”, ¿Cuál oración que describe mejor los beneficios que provee Cloud bursting?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2022.png)
        
        Con “Cloud Bursting” activo, los servicios en la nube son provisionados cuando los servidores on-premises llegan al 100% de su capacidad. Cloud bursting es usado en modelos de nube hibrida.
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2023.png)
        
    - ¿Cuales dos conocimientos a nivel de organización pueden derivar del panel de control de cumplimiento normativo de Microsoft Defender for Cloud?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2024.png)
        
        En el dashboard de Microsoft defender for cloud podemos encontrar una puntuación de cumplimiento normativo (Compliance Score) y el numero de evaluciones fallidas y cumplidas.
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2025.png)
        
    - ¿Cual recurso puede ser desplegado como Infrastructura como servicio (IaaS)?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2026.png)
        
        Maquinas virtuales
        
    - Dado los requerimientos de cada departamento, ¿Cuál solución recomendarías?
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2027.png)
        
        Usar hardware administrado para correr una base de datos personalizada: IaaS
        
        Usar un calendario para programar nuestras tareas y reuniones: SaaS
        
        Usar servicios de BI para analizar tendencias de marketing: PaaS
        
        ![Untitled](Curso%20AZ%20900%208d76fb233020479281e8491c5f6e6950/Untitled%2028.png)