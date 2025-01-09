# AeroSpace-Cybersecurity--ESP

# Una introduccion de ciberseguridad aeroespacial, los satélites y temas relacionados.

Hola compas, durante los últimos 2 años, he estado aprendiendo de forma autodidacta en tecnología aeroespacial y he dedicado mucho tiempo a investigar este campo con enfoque a ciberseguridad ofensiva (area de mi especialización). Este repositorio es una recopilación de ideas, notas e información que he reunido durante este viaje. He organizado el material de una manera clara y coherente (¡espero que así sea! XD), comenzando con la tecnología satelital, seguido por la seguridad aeroespacial general y, finalmente, explorando cómo hackear satélites (esto se detallará en futuras publicaciones con laboratorios satelitales caseros). ¡Espero que este recurso les resulte útil para mejorar su comprensión y conocimiento de este fascinante campo! :)

Este proyecto está destinado únicamente a fines educativos. El autor no es responsable de ningún mal uso o daños causados por este contenido. Asegúrese siempre de tener la autorización adecuada antes de realizar cualquier prueba de seguridad.

## Contenidos

- Introducción
- Tipos de órbitas utilizadas en la comunicación por satélite
- Tipos de satélites, categorías y servicios
- Componentes clave de hardware de los satélites
- Componentes clave de software de los satélites
- Componentes clave de las comunicaciones por satélite entre satélites y estaciones terrestres.
- Tipos y formatos de datos enviados o utilizados por satélites
- Tipos de antenas utilizadas en estaciones terrestres para comunicaciones por satélite
- Introducción a la ciberseguridad en la tecnología satelital
- Ciberseguridad ofensiva en la industria aeroespacial y tecnología satelital
- Herramientas y técnicas
- Referencias y recomendaciones

## Introducción

**¿Qué es la ciberseguridad aeroespacial?**

La ciberseguridad aeroespacial es fundamental para proteger la integridad de las operaciones de aeronaves y naves espaciales. En una época en la que las amenazas cibernéticas evolucionan constantemente, es vital implementar medidas de seguridad sólidas para salvaguardar los sistemas y datos confidenciales dentro del sector aeroespacial. Al priorizar la ciberseguridad aeroespacial, podemos garantizar la seguridad y la confiabilidad de nuestras industrias aéreas y espaciales, lo que a su vez ayuda a mantener la confianza pública y promueve la innovación tecnológica.

## Órbitas y tecnologías de los satélites

Los satélites son objetos que orbitan alrededor de un planeta u otros cuerpos celestes. Pueden ser naturales, como las lunas o artificiales que son dispositivos creados por el hombre y lanzados al espacio con diversos fines. Los satélites artificiales cumplen muchas funciones, entre ellas la comunicación, el control del clima, la navegación, la investigación científica y la observación de la Tierra.

Las órbitas de los satélites describen las trayectorias que recorren los satélites alrededor de cuerpos celestes como la Tierra. Estas trayectorias están determinadas por la interacción entre la fuerza gravitacional del planeta y la velocidad del satélite. Las órbitas son clave para determinar el propósito de un satélite, su área de cobertura y cuánto tiempo puede funcionar. Técnicamente las órbitas se caracterizan por la altitud, la inclinación y el tiempo que tarda en completar una vuelta al planeta completa.

## Tipos de órbitas utilizadas por satélite

**LEO - Órbita baja terrestre**

- **Elevación de los satélites**: Entre 160 km y 2.000 km sobre la superficie de la Tierra.
- **Características principales**:
    - Periodo orbital corto: 90 a 120 minutos, lo que permite múltiples visitas diarias a la misma región.
    - Baja velocidad relativa respecto a la superficie de la Tierra.
    - Alta resistencia atmosférica, especialmente a altitudes inferiores a 500 km, lo que provoca una degradación orbital más significativa y requiere sistemas de propulsión para mantenerla.
- **Funciones clave de esta órbita**:
    - Constelaciones de comunicaciones: Diseñadas para proporcionar conectividad de banda ancha global.
    - Satélites de observación de la Tierra: Incluyen misiones científicas que monitorean el cambio climático, las actividades agrícolas y los desastres naturales.
    - Satélites espía: Utilizados por agencias gubernamentales debido a su alta resolución de imagen desde bajas altitudes.
- **Limitaciones en esta órbita**:
    - Necesidad de grandes constelaciones de satelites para una cobertura continua.
    - Mayor riesgo a choques debido a la densidad de objetos en esta región.

**MEO - Órbita media terrestre**

- ***Elevación de los satélites**: Entre 2.000 km y 35.786 km.
- **Características principales**:
    - Dependiendo de la altitud, un período orbital de 2 a 12 horas ofrece una estabilidad orbital mayor en comparación con LEO.
    - Menor interferencia atmosférica, lo que extiende la vida útil del satélite y reduce la necesidad de maniobras frecuentes.
    - Cobertura regional mejorada debido al mayor rango de visibilidad.
- **Funciones clave de esta órbita**:
    - Sistemas de navegación: GPS, Galileo, GLONASS y BeiDou. Los satélites en MEO ofrecen señales consistentes y precisas para el posicionamiento global.
    - Satélites científicos: Diseñados para misiones de monitoreo a largo plazo, como el análisis de los campos magnéticos de la Tierra.
- **Limitaciones en esta órbita**:
    - Requiere sistemas de telecomunicaciones potentes debido a la mayor distancia de la superficie de la Tierra.
    - Menor resolución espacial en comparación con los satélites LEO.

**GEO - Órbita terrestre geoestacionaria**

- **Elevación de los satélites**: 35.786 km sobre el ecuador terrestre.
- **Características principales**:
    - Los satélites se posicionan con una velocidad angular que se sincroniza con la rotación de la Tierra, permitiendo mantener una posición fija en el cielo.
    - Proporcionan una cobertura continua de un tercio del globo, ideal para la transmisión televisiva y los servicios meteorológicos.
    - La densidad de satélites en esta órbita es menor que en la órbita terrestre baja (LEO), reduciendo el riesgo de colisiones.
- **Funciones clave de esta órbita**:
    - Telecomunicaciones globales: Incluye satélites como Intelsat y SES.
    - Monitoreo meteorológico: Satélites como GOES proporcionan datos esenciales para predicciones meteorológicas en tiempo real.
    - Sistemas de alerta temprana: Cruciales para detectar fenómenos naturales como huracanes y terremotos.
- **Limitaciones en esta órbita**:
    - Costos de lanzamiento elevados debido a la gran cantidad de energía requerida para alcanzar la altitud.
    - Retraso de comunicación de aproximadamente 240 ms o más, lo que podría afectar aplicaciones sensibles al tiempo.

**HEO - Órbita altamente elíptica**

- **Características principales**:
    - Las órbitas con un perigeo bajo (300-1000 km) y un apogeo alto (superior a 35.786 km) permiten períodos prolongados en la región del apogeo.
    - Un ángulo de inclinación alto hace que estas órbitas sean ideales para proporcionar cobertura en regiones polares o de alta latitud.
    - Mayor exposición a la radiación espacial, lo que requiere sistemas robustos para proteger los componentes electrónicos.
- **Funciones clave de esta órbita**:
    - Monitoreo polar: Utilizado por satélites meteorológicos y científicos para observar las regiones polares.
    - Telescopios espaciales: Beneficiados por la larga duración, permitiendo observaciones continuas.
    - Comunicación militar: Ofrece servicios de comunicación estables en regiones inaccesibles para satélites de órbita baja (LEO) o geoestacionarios (GEO).
- **Limitaciones en esta órbita**:
    - Trayectoria compleja que requiere control preciso para la estabilidad orbital.
    - Mayor riesgo de exposición a partículas cargadas del cinturón de Van Allen.
 
  ## Tipos de satélites, categorías y servicios

Esta sección destaca los principales tipos de satélites, sus funciones, propósitos y ejemplos, clasificados según sus aplicaciones específicas y los servicios que brindan a las industrias, gobiernos y usuarios cotidianos.
+
**Satélites de comunicación**

- **Objetivos**:
    - Facilitan la transmisión de datos, televisión, telefonía e internet de alta velocidad.
    - Enlaces intercontinentales que reducen la necesidad de infraestructura terrestre, esencial en regiones remotas o con poca conectividad terrestre.
- **Ejemplos destacados**:
    - Intelsat: Proporciona servicios globales de telecomunicaciones con una vasta red de satélites en GEO.
    - SES: Transmisión de video satelital e Internet, operando satélites en GEO y MEO a través de su constelación O3b.
- **Aspectos técnicos**:
    - Banda de frecuencia: Uso de bandas como Ku (12-18 GHz) y Ka (26-40 GHz) para maximizar el ancho de banda.
    - Unicast: Comunicaciones punto a punto específicas.
    - Broadcast: Transmisión de contenido a grandes audiencias, como televisión satelital.
    - Multicast: Distribución de datos a un grupo definido, común en redes empresariales.

**Satélites de observación terrestre**

- **Objetivos**:
    - Recopilación de imágenes y datos ambientales para monitorear cambios en la superficie terrestre, predecir el clima y realizar estudios de impacto ambiental.
    - Aplicaciones en agricultura, gestión de recursos naturales y monitoreo de desastres naturales.
- **Ejemplos destacados**:
    - Sentinel (programa Copernicus): Captura datos multiespectrales para monitoreo de cambio climático y desastres ambientales.
    - Landsat: Serie de satélites operados por NASA y USGS, pioneros en monitoreo continuo de la superficie terrestre desde 1972.
- **Aspectos técnicos**:
    - Resolución espacial: Variaciones de 10 m (Sentinel-2) a 30 m (Landsat-8).
    - Frecuencia de revisita: Capacidad para observar la misma área cada pocos días en LEO.
    - Sensores: Equipados con cámaras ópticas, radiómetros infrarrojos y radares de apertura sintética (SAR).

**Satélites de navegación**

- **Objetivos**:
    - Proporcionar servicios de posicionamiento global (GNSS) y sincronización de tiempo precisa.
    - Esenciales para aplicaciones civiles y militares, como navegación aérea, marítima y terrestre, además de sistemas críticos como redes eléctricas y financieras.
- **Ejemplos destacados**:
    - GPS: Sistema pionero con cobertura global y 24 satélites activos en MEO.
    - GLONASS: Alternativa al GPS con una constelación activa para servicios globales.
    - Galileo: Sistema en desarrollo enfocado en alta precisión para aplicaciones civiles.
    - BeiDou: Proporciona servicios regionales y globales en Asia desde 2020.
- **Aspectos técnicos**:
    - Constellaciones distribuidas en MEO, garantizando cobertura global con múltiples satélites visibles.
    - Transmisión de señales en bandas L1, L2 y L5 para reducir interferencias y mejorar la precisión.

**Satélites científicos**

- **Objetivos**:
    - Diseñados para estudios astronómicos, análisis climático y exploración de fenómenos físicos en el espacio.
    - Realizan observaciones detalladas desde el espacio, eliminando distorsiones atmosféricas.
- **Ejemplos destacados**:
    - Telescopio Espacial Hubble: Órbita LEO para estudios astronómicos en luz visible y ultravioleta.
    - SOHO: Satélite en el punto de Lagrange L1, dedicado a la observación continua del Sol.
- **Aspectos técnicos**:
    - Equipados con instrumentos especializados como espectrómetros, telescopios y detectores de partículas.
    - Localización en LEO o GEO dependiendo de los objetivos científicos.
    - Sistemas redundantes para evitar fallos críticos en misiones de larga duración.

**Satélites militares**

- **Objetivos**:
    - Realizan actividades de vigilancia, espionaje, comunicaciones seguras y apoyo táctico.
    - Proporcionan información crítica en tiempo real para operaciones militares.
- **Ejemplos destacados**:
    - Keyhole: Satélites de reconocimiento óptico operados por Estados Unidos.
    - Milstar: Satélites de comunicaciones militares resistentes a interferencias.
- **Aspectos técnicos**:
    - Altamente cifrados para proteger datos sensibles.
    - Equipados con sistemas avanzados de radar y monitoreo multiespectral.
    - Maniobras orbitales frecuentes para evitar detección o rastreo.

**Nanosatélites y CubeSats**

- **Aspectos técnicos**:
    - Nanosatélites con masa menor a 10 kg diseñados para ser compactos y eficientes; CubeSats son un tipo específico de nanosatélite construido en unidades modulares de 10x10x10 cm (llamadas 1U).
    - Arquitectura modular permite configuraciones escalables, adaptándose a diversas aplicaciones científicas, educativas y comerciales.
    - Costos reducidos: Uso de componentes comerciales estándar (COTS) para minimizar el costo de fabricación y lanzamiento.
    - Flexibilidad: Ideales para experimentos de corta duración en órbita baja (LEO) o pruebas de nuevas tecnologías.
    - Despliegue: Lanzados frecuentemente como cargas secundarias en cohetes comerciales.
- **Ejemplos destacados**:
    - Científicos: Observación de fenómenos atmosféricos, medición de radiación espacial y estudio de dinámicas orbitales.
    - Educativos: Ofrecen plataformas asequibles para formación práctica en ingeniería aeroespacial.
    - Diseñados para monitorear calidad del aire en áreas urbanas usando sensores ópticos y espectrometría, enviando datos en tiempo real a estaciones terrestres vía enlaces de radiofrecuencia en banda S.
- **Desafíos técnicos**:
    - Limitaciones en capacidad de carga útil y generación de energía debido a su tamaño.
    - Mayor vulnerabilidad a fallos mecánicos y radiación en comparación con satélites más grandes.

**Satélites comerciales y gubernamentales**

- **Aspectos técnicos**:
    - Diseñados específicamente para cumplir misiones complejas y de larga duración, integrando tecnologías avanzadas y sistemas redundantes para alta fiabilidad.
    - Los satélites comerciales suelen enfocarse en telecomunicaciones, navegación y observación terrestre, mientras que los gubernamentales abarcan también aplicaciones científicas, meteorológicas y de defensa.
    - Sistemas de carga útil: Incluyen cámaras de alta resolución, sensores espectrales multibanda y equipos de telecomunicaciones de gran ancho de banda.
    - Subsystems de control: Sistemas de control de actitud y orientación (ADCS) para asegurar alineación correcta con objetivos de misión.
    - Generación de energía: Paneles solares de triple unión de alta eficiencia y sistemas avanzados de almacenamiento de energía.
- **Ejemplos destacados**:
    - Satélites comerciales: Intelsat para telecomunicaciones globales y PlanetScope para imágenes de alta frecuencia.
    - Satélites gubernamentales: GOES para meteorología y Keyhole para vigilancia.
- **Desafíos técnicos**:
    - Altos costos de desarrollo y lanzamiento.
    - Requisitos estrictos de seguridad y protección de datos para prevenir intercepciones o sabotajes.
 

  ## Componentes clave del hardware de los satélites

El hardware de los satélites abarca los sistemas físicos necesarios para su operación, asegurando su funcionalidad y éxito en la misión.

- **Estructura o plataforma**: Proporciona un marco rígido que integra y soporta todos los subsistemas del satélite. Resiste el estrés mecánico durante el lanzamiento y protege los componentes internos en órbita. Ejemplos: Spacebus (Thales Alenia) y la plataforma SSL 1300.
- **Sistema de energía**: Genera y gestiona la energía eléctrica mediante paneles solares y baterías recargables, asegurando un suministro ininterrumpido para todos los componentes. Ejemplos: Paneles solares Spectrolab usados en misiones de la NASA y baterías de iones de litio Saft.
- **Sistema de propulsión**: Proporciona empuje para correcciones orbitales, mantenimiento de posición y desorbitado. Utiliza propulsión química o eléctrica. Ejemplos: Propulsor iónico RIT-10 (propulsión eléctrica) y sistemas bipropelentes MON/MMH.
- **Sistema de control térmico**: Regula las temperaturas internas para garantizar un rendimiento óptimo en condiciones extremas del espacio. Ejemplos: MLI (Aislamiento Multicapa) para minimizar la pérdida de calor y tubos de calor de bucle para transferir calor a los radiadores.
- **Sistema de comunicación**: Facilita el intercambio de datos entre el satélite y las estaciones terrestres mediante antenas, transceptores y moduladores. Ejemplos: Antena de matriz en fase de banda Ka de Airbus y el modulador/demodulador iQRF utilizado para telemetría.
- **Sistema de control de actitud y órbita (ADCS)**: Permite al satélite mantener su orientación y trayectoria previstas mediante dispositivos como ruedas de reacción y rastreadores de estrellas. Ejemplos: Ruedas de reacción HR16 de Honeywell y rastreadores de estrellas de Ball Aerospace.
- **Sistema de carga útil**: Lleva equipos específicos de la misión, como cámaras, sensores o instrumentos científicos. Ejemplos: Sensor óptico WorldView-3 para imágenes terrestres y carga útil SAR en Sentinel-1 para mapeo por radar.
- **Computación y control a bordo**: Procesa datos de la misión, gestiona subsistemas y ejecuta comandos. Ejemplos: Procesador LEON3 y CPU RAD750, una computadora resistente a la radiación utilizada en muchos satélites de la NASA.
- **Sensores y actuadores**: Recopilan datos para orientación y navegación, mientras que los actuadores controlan movimientos físicos. Ejemplos: Sensores solares Adcole para seguimiento de posición y motores paso a paso para el despliegue de antenas.
- **Sistema de almacenamiento de datos**: Almacena telemetría y datos de la carga útil para su transmisión posterior a las estaciones terrestres. Ejemplos: Unidades de estado sólido (SSD) utilizadas en los satélites meteorológicos GOES y módulos de memoria flash de alta capacidad para CubeSats.

## Componentes clave del software de los satélites

El software de los satélites es fundamental para la gestión de operaciones, control del sistema y comunicación, permitiendo que los componentes de hardware operen de manera sincronizada y eficiente. Dado el entorno extremo y la complejidad de las misiones espaciales, estos sistemas deben ser robustos, confiables y seguros.

- **Sistema operativo de misión (Flight Software)**: Gestiona las operaciones generales del satélite, como la ejecución de comandos, la gestión de energía y el control de subsistemas. Ejemplos: VxWorks y RTEMS.
- **Software de control de actitud y órbita (AOCS)**: Regula la orientación y posición del satélite en su órbita mediante algoritmos avanzados.
- **Software de gestión de datos de misión**: Administra la recopilación, almacenamiento y transmisión de datos generados por los sistemas de carga útil.
- **Software de comunicación y telemetría**: Controla la transmisión y recepción de señales entre el satélite y las estaciones terrestres. Ejemplo: Protocolos basados en CCSDS.
- **Software de diagnóstico y monitoreo**: Realiza monitoreo en tiempo real de todos los subsistemas, detecta fallas y ejecuta protocolos de recuperación.
- **Software de control térmico**: Coordina los sistemas de regulación térmica para mantener las condiciones óptimas del hardware.
- **Software de seguridad y cifrado**: Protege las comunicaciones y datos contra accesos no autorizados o interferencias maliciosas.
- **Software de gestión de propulsión**: Monitorea y controla los sistemas de propulsión durante maniobras orbitales. Ejemplo: Sistemas de propulsión RIT-22.
- **Software de carga útil**: Controla los instrumentos específicos de la misión, como cámaras, sensores o radares.
- **Interfaz de control en tierra**: Permite a las estaciones terrestres enviar comandos y recibir datos de telemetría eficientemente. Ejemplo: Sistemas SCOS-2000 usados en misiones de la ESA.

## Componentes clave de la comunicación satelital entre satélites y estaciones terrestres

La comunicación satelital se refiere a la transferencia de datos entre satélites y estaciones terrestres, así como entre los propios satélites. Este proceso es facilitado por diversos protocolos diseñados para satisfacer necesidades específicas de telemetría, comandos, transmisión de datos científicos y control operacional en misiones espaciales.

- **Enlace ascendente (Uplink)**: Permite la transmisión de comandos y configuraciones desde estaciones terrestres al satélite, diseñado para alta fiabilidad mediante técnicas de redundancia y codificación.
- **Enlace descendente (Downlink)**: Facilita la transmisión de datos recopilados por el satélite, incluidos telemetría y datos científicos, a las estaciones terrestres. Está optimizado para minimizar la pérdida de datos y maximizar la velocidad de transferencia.
- **Comunicación por enlace directo**: El satélite se comunica directamente con una estación terrestre o terminal de usuario sin dispositivos intermedios.
- **Comunicación vía satélites de retransmisión**: Método que implica la comunicación entre estaciones terrestres a través de un satélite intermediario, común en redes de radiodifusión y comunicaciones a gran escala.
- **Comunicación inter-satelital**: Permite que los satélites intercambien datos entre sí, como en constelaciones satelitales o redes de malla que facilitan la retransmisión de datos o mejoran la cobertura.

**Frecuencias de radio satelitales**: Son porciones del espectro electromagnético utilizadas para la comunicación entre satélites y estaciones terrestres, así como entre los propios satélites. Estas frecuencias permiten la transmisión de señales de telemetría, comandos, datos científicos, información de navegación y comunicaciones generales.

- **Banda L (1–2 GHz)**: Usada principalmente en sistemas GNSS (GPS y Galileo) y comunicaciones móviles satelitales. Ofrece buena penetración atmosférica y es menos susceptible a la atenuación por lluvia, aunque con capacidad limitada para transmisión de datos.
- **Banda S (2–4 GHz)**: Utilizada en aplicaciones comerciales y militares, incluyendo telemetría y retransmisión de datos. Es robusta frente a condiciones climáticas adversas y adecuada para transferencias de datos de baja capacidad.
- **Banda C (4–8 GHz)**: Común en televisión satelital y enlaces de datos seguros entre estaciones terrestres y satélites. Resistente a la atenuación por lluvia, confiable para satélites geoestacionarios.
- **Banda X (8–12 GHz)**: Usada en aplicaciones militares, científicas y de radar, así como en sistemas de comunicación satelital para imágenes de alta resolución y transmisiones seguras.
- **Banda Ku (12–18 GHz)**: Empleada para TV satelital, internet de banda ancha y comunicaciones de alta capacidad. Admite altas tasas de datos, aunque es más susceptible a la atenuación por lluvia.
- **Banda Ka (26–40 GHz)**: Enfocada en comunicaciones de alta capacidad y aplicaciones intensivas en datos. Ideal para internet satelital de alta velocidad, aunque muy sensible a la atenuación por lluvia.
- **Banda V (40–75 GHz)**: Usada principalmente en sistemas experimentales de comunicación y tecnologías emergentes. Ofrece tasas de datos muy altas, pero es sensible a la atenuación atmosférica.

**Protocolos de comunicación satelital**: Métodos estandarizados para el intercambio de datos entre satélites, estaciones terrestres y otros sistemas espaciales. Estos protocolos especifican cómo se transmiten datos de telemetría, comandos, señales científicas y de comunicación.

- **CCSDS (Consultative Committee for Space Data Systems)**: Protocolo que establece estándares para sistemas de telemetría y comando, operando en bandas S y X.
- **SpaceWire**: Protocolo de alta velocidad para subsistemas internos de satélites, ampliamente usado por ESA y NASA.
- **PUS (Packet Utilization Standard)**: Protocolo que gestiona datos mediante empaquetado de información, crucial para misiones científicas y de observación terrestre.
- **SLE (Space Link Extension)**: Mejora la comunicación entre estaciones terrestres y satélites, vital para misiones interplanetarias.
- **DTN (Delay Tolerant Networking)**: Maneja retrasos de comunicación en misiones de exploración espacial, almacenando datos para retransmisión.
- **HDLC (High-Level Data Link Control)**: Garantiza integridad de datos en sistemas de telemetría para misiones científicas de larga duración.
- **TCP/IP Adaptado**: Usado en redes espaciales modernas para transferencia eficiente de datos científicos, operando principalmente en banda Ka.
- **ECSS (European Cooperation for Space Standardization)**: Fomenta la interoperabilidad entre sistemas espaciales en misiones de la ESA.
- **TDM (Time Division Multiplexing)**: Permite que múltiples señales compartan una frecuencia al dividirla en intervalos de tiempo.
- **ARINC 653**: Estandariza la partición en sistemas satelitales en tiempo real para garantizar seguridad en aplicaciones críticas.
- **LoRa**: Protocolo de bajo consumo para CubeSats, que permite comunicación de baja tasa de datos en banda UHF.
- **DVB-S**: Protocolo para radiodifusión televisiva satelital, operando en bandas Ku, C y Ka.
- **DVB-RCS**: Facilita comunicación bidireccional a través de satélites para servicios interactivos.
- **IPoS**: Protocolo para transmitir datos basados en IP sobre enlaces satelitales en bandas L, Ku y Ka.


## Tipos y formatos de datos enviados o utilizados por satélites

La recopilación, transmisión y procesamiento de datos son funciones cruciales en los sistemas satelitales, apoyando aplicaciones científicas, comerciales y de defensa. Los niveles y formatos de procesamiento están diseñados para mejorar la eficiencia, precisión y compatibilidad con varios sistemas de análisis y usuarios finales.

- **Datos de telemetría**: Información en tiempo real enviada desde el satélite a las estaciones terrestres para monitorear el estado y salud del satélite. Incluyen parámetros como temperatura, voltaje, actitud y órbita. Generalmente se formatean utilizando protocolos como CCSDS.
- **Datos de comandos**: Instrucciones enviadas desde las estaciones terrestres para controlar las operaciones del satélite, como ajustar su orientación, activar o desactivar cargas útiles o cambiar modos operativos. Estos comandos suelen transmitirse en formato binario y encapsulados en paquetes de datos.
- **Datos científicos**: Los satélites recopilan varios tipos de datos científicos, como imágenes, mediciones y lecturas de sensores. Estos datos pueden estar en formatos como:
    - **Datos sin procesar**: Datos directamente de los sensores, a menudo almacenados en formatos binarios o científicos.
    - **Datos procesados**: Datos analizados o convertidos en formatos utilizables, como CSV, NetCDF o HDF5.
    - **Datos de imágenes y video**: Satélites de observación terrestre o científicos que envían imágenes (JPEG o TIFF) y videos (MPEG-4 o H.264).
    - **SAR (Radar de Apertura Sintética)**: Datos en formatos especializados para imágenes de radar.
- **Datos de navegación**: Incluyen información de posición, tiempo y velocidad, transmitidos en formatos binarios específicos como NMEA o RTCM.
- **Datos para servicios de comunicación**: Datos utilizados para servicios de comunicación satelital (como internet o radiodifusión) transmitidos en forma de paquetes, generalmente usando IP. Los formatos incluyen MPEG-2 o MPEG-4 para video.
- **Datos de carga útil**: Datos recopilados por instrumentos específicos de la misión del satélite, con formatos que varían según la misión.
- **Informes de estado y registros**: Datos operativos enviados en texto o binario para monitoreo del rendimiento del sistema. Formatos comunes incluyen XML o JSON para facilitar la interpretación.
- **Datos para comunicación intersatelital**: Datos intercambiados entre satélites en una constelación, siguiendo protocolos como SpaceWire o CCSDS.

## Tipos de antenas utilizadas en estaciones terrestres para la comunicación satelital

Las estaciones terrestres dependen de sistemas de antenas avanzados para establecer y mantener enlaces de comunicación confiables con los satélites. La selección de una antena se basa en la órbita del satélite, la banda de frecuencia utilizada y los requisitos específicos de la misión.

- **Antenas parabólicas**: Enfocan ondas de radio hacia un receptor, siendo altamente direccionales. Usadas en satélites de comunicación, radiodifusión y observación terrestre.
- **Antenas de matriz**: Pueden dirigir electrónicamente la dirección del haz sin necesidad de movimiento físico. Comúnmente empleadas en satélites LEO, como Starlink.
- **Antenas helicoidales**: Diseñadas para polarización circular, ideales para comunicación en bandas S y L, como en la constelación Iridium.
- **Antenas planas (patch antennas)**: Ofrecen cobertura de amplio ángulo y son comunes en pequeños satélites y CubeSats.
- **Antenas de bocina**: Con alta ganancia y capacidades direccionales, son usadas en frecuencias altas para comunicación intersatelital y misiones científicas.

## Introducción a la ciberseguridad en tecnología satelital

La intersección entre la tecnología satelital y la ciberseguridad es un área crítica, especialmente a medida que los sistemas satelitales se vuelven esenciales para comunicaciones globales, navegación y observación terrestre. La creciente sofisticación de los ciberataques dirigidos a sistemas espaciales exige una seguridad reforzada. La complejidad de las infraestructuras satelitales requiere comprender los puntos de ataque y las amenazas potenciales.

La ciberseguridad en tecnología aeroespacial, con énfasis en satélites, puede dividirse en cuatro segmentos clave:

### Segmento de usuario: terminales y dispositivos de usuario

Incluye los dispositivos y sistemas empleados por los usuarios finales para interactuar con redes satelitales. Este segmento es vulnerable, ya que sirve como interfaz entre los usuarios y la red satelital.

**Componentes clave**:
- **Terminales terrestres**: Estaciones fijas o móviles que transmiten y reciben señales satelitales.
- **Equipos de usuario**: Teléfonos satelitales, sensores IoT, dispositivos con GPS y módems satelitales.
- **Sistemas de procesamiento de datos**: Equipos y software usados para interpretar datos satelitales.

**Vectores de ataque**:
- Acceso no autorizado a terminales terrestres debido a autenticación débil o firmware obsoleto.
- Explotación de vulnerabilidades en dispositivos como teléfonos satelitales o sensores IoT.
- Intercepción o suplantación de señales de comunicación.
- Manipulación física de terminales terrestres en ubicaciones desprotegidas.
- Ataques MitM (hombre en el medio), permitiendo la manipulación o intercepción de datos.

**Desafíos en la seguridad del segmento de usuario**:

- Diversidad de dispositivos y configuraciones.
- Limitaciones de recursos en dispositivos IoT.
- Vulnerabilidad física en ubicaciones remotas.
- Falta de protocolos de seguridad estandarizados.

### Segmento de enlace: canales de comunicación y enlaces RF

Se refiere a las vías de comunicación entre satélites, estaciones terrestres y dispositivos de usuario, usando enlaces de radiofrecuencia (RF). Dividido en:

**Componentes clave**:
- **Enlace ascendente (uplink)**: Comunicación de estaciones terrestres al satélite.
- **Enlace descendente (downlink)**: Comunicación del satélite a las estaciones terrestres.

**Vectores de ataque**:
- **Interferencias**: Señales RF de alta potencia para interrumpir comunicaciones.
- **Escucha clandestina**: Captura de señales no encriptadas.
- **Suplantación de señales**: Réplicas maliciosas para alterar datos o comandos.
- **Ataques de repetición**: Reenvío de señales legítimas capturadas.

**Desafíos en la seguridad de enlaces RF**:
- Apertura inherente de las señales RF.
- Restricciones de ancho de banda.
- Sistemas heredados sin características de seguridad modernas.

### Segmento terrestre: estaciones y red de infraestructura

Incluye las instalaciones terrestres responsables de la operación satelital, siendo un objetivo de alto valor.

**Componentes clave**:
- Centros de control de la misión.
- Estaciones terrestres para telemetría y control.
- Centros de procesamiento de datos.

**Vectores de ataque**:
- Compromiso de centros de control para alterar operaciones.
- Ataques DoS en redes terrestres.
- Explotación de vulnerabilidades en estaciones terrestres.

**Desafíos en la seguridad del segmento terrestre**:

- Infraestructura heredada difícil de actualizar.
- Alta interconectividad y dependencia de redes globales.
- Presupuestos limitados que dificultan implementar medidas avanzadas.

## Ciberseguridad ofensiva en tecnologías aeroespaciales y satelitales

La seguridad ofensiva en tecnología aeroespacial y satelital es un área de ciberseguridad que busca emular a adversarios reales para identificar y explotar vulnerabilidades en sistemas críticos. Este dominio es único, ya que combina prácticas tradicionales de ciberseguridad con la complejidad de los sistemas espaciales, las comunicaciones satelitales y las redes de control terrestre. Con la creciente comercialización y militarización del espacio, la seguridad en este ámbito se ha convertido en una prioridad estratégica.

A continuación, se detallan algunas de las técnicas más utilizadas en ciberseguridad ofensiva en este sector:

### **Intercepción de señales y espionaje**

- **Objetivo**: Capturar señales de comunicación satelital para obtener información sensible.
- **Técnicas y metodología**:
    - Usar radios definidas por software (SDRs) para interceptar señales descendentes.
    - Identificar bandas de frecuencia (p. ej., L-band, C-band, Ku-band) utilizando analizadores de espectro.
    - Demodular señales con software como GNURadio.
    - Decodificar protocolos de datos.
- **Herramientas**:
    - **Hardware**: HackRF One, BladeRF, RTL-SDR, USRP.
    - **Software**: GNURadio, SatDump.
    - **Antenas**: Plato parabólico de alta ganancia, antenas Yagi.

### **Jamming y ataques de denegación de servicio (DoS)**

- **Objetivo**: Interrumpir comunicaciones satelitales inundando la señal con ruido o transmisiones maliciosas.
- **Técnicas y metodología**:
    - Identificar frecuencias objetivo y tipos de modulación.
    - Utilizar amplificadores de alta potencia y antenas direccionales para transmitir señales interferentes.
    - Generar ruido aleatorio o señales RF dirigidas.
- **Herramientas**:
    - **Hardware**: USRP (Universal Software Radio Peripheral), amplificadores RF de alta potencia.
    - **Software**: GNURadio, SigGen.
    - **Antenas**: Antenas direccionales de alta ganancia.

### **Suplantación e inyección de señales**

- **Objetivo**: Imitar señales satelitales legítimas para manipular receptores o interrumpir comunicaciones.
- **Técnicas y metodología**:
    - Analizar señales satelitales para comprender su estructura y modulación.
    - Replicar señales inyectando datos o comandos falsos.
    - Aplicar técnicas de suplantación GPS para confundir sistemas de navegación.
- **Herramientas**:
    - **Hardware**: HackRF, BladeRF.
    - **Software**: GPS-SDR-Sim, GNSS-SDR.
    - **Antenas**: Antenas omnidireccionales de banda ancha.

### **Secuestro de comandos y control**

- **Objetivo**: Acceso no autorizado a la interfaz de control del satélite para emitir comandos o alterar su trayectoria.
- **Técnicas y metodología**:
    - Capturar y analizar señales de telemetría usando SDRs.
    - Explotar credenciales por defecto o mecanismos de autenticación débiles.
    - Usar ataques de fuerza bruta o diccionario contra interfaces expuestas.
- **Herramientas**:
    - **Hardware**: SDRs, USRP.
    - **Software**: GR-Satellites, analizadores de red.
    - **Scripts**: Python para emulación de protocolos.

### **Ataques al bus del satélite**

- **Objetivo**: Explotar vulnerabilidades en los sistemas a bordo del satélite.
- **Técnicas y metodología**:
    - Analizar firmware mediante ingeniería inversa.
    - Realizar ataques de canal lateral para extraer claves de cifrado.
    - Explotar fallos conocidos en protocolos como CAN, I2C o SPI.
- **Herramientas**:
    - **Hardware**: Adaptadores JTAG, analizadores lógicos.
    - **Software**: Herramientas de análisis binario y reversa.
    - **Kits de ataque**: ChipWhisperer, Bus Pirate.

### **Ciberataques a redes de comunicación satelital**

- **Objetivo**: Explorar vulnerabilidades en redes como terminales VSAT y enlaces intersatelitales.
- **Técnicas y metodología**:
    - Realizar reconocimiento y escaneo de terminales VSAT abiertos.
    - Explotar protocolos de red inseguros como FTP, Telnet o SNMP.
- **Herramientas**:
    - **Software**: Kali Linux.
    - **Herramientas de reconocimiento**: Shodan.

### **Ataques de repetición (Replay)**

- **Objetivo**: Capturar y reutilizar comandos legítimos para ejecutar acciones maliciosas.
- **Técnicas y metodología**:
    - Interceptar señales de comandos con SDR.
    - Reproducir comandos con modificaciones mínimas.
    - Explotar la falta de cifrado en protocolos de comunicación.
- **Herramientas**:
    - **Hardware**: HackRF, BladeRF.
    - **Software**: GNURadio, scripts en Python para automatización.

### **Manipulación de telemetría y telecomandos**

- **Objetivo**: Alterar datos de telemetría o comandos para impactar las operaciones del satélite.
- **Técnicas y metodología**:
    - Interceptar datos de telemetría con herramientas SDR.
    - Inyectar comandos modificados utilizando protocolos reversados.
    - Explotar canales de telecomando sin autenticación.
- **Herramientas**:
    - **Hardware**: BladeRF, HackRF.
 
# Referencias y recomendaciones

Aquí hay una lista de referencias que incluye excelentes blogs de colegas, compilaciones de herramientas, videos y materiales adicionales para ayudarlo a sumergirse más profundamente en el fascinante mundo de la ciberseguridad aeroespacial.

Comunidades

- https://hackasat.com/
- https://dc506.org/
- https://www.hackspacecon.com/HackSpaceCon
- https://www.aerospacevillage.org/

Herramientas y proyectos:

- https://tools.g4lxy.space/
- https://hackaday.io/list/4321-satellite-projects

Videos:

- https://www.youtube.com/watch?v=V4jXVrUJsfM
- https://www.youtube.com/@AerospaceVillage
- https://www.youtube.com/watch?v=Au43CmiOO_g

Referencias:

- https://www.rtl-sdr.com/about-rtl-sdr/
- https://www.nasa.gov/wp-content/uploads/2017/03/nasa_csli_cubesat_101_508.pdf?emrc=05d3e2
- https://lucasteske.dev/satcom-projects/satellite-projects
- https://github.com/OpenSatKit/OpenSatKit
- https://github.com/nasa/nos3
- https://github.com/orbitalindex/awesome-space
- https://github.com/deptofdefense/hack-a-sat-library
- https://sparta.aerospace.org/
- https://spaceshield.esa.int/
- https://www.spacesecurity.info/
- https://github.com/Peco602/awesome-space-security
- https://attack.mitre.org/matrices/ics/  
