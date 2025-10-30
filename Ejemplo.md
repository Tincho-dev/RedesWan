Trabajo Práctico

Conectividad WLAN

Deberá realizar un proyecto de conectividad WLAN utilizando un radio enlace para vincular el sitio de nuestra facultad con otro predio que corresponde a un futuro campus, todavía en proceso de definición y desarrollo.

Utilizará la herramienta para realizar los cálculos de conectividad provista por Ubiquiti (<https://link.ui.com/>). Los sitios para vincular son los siguientes:

- Estimara la altura de las torres necesarias considerando los edificios y arboledas que hay entre ambos sitios.
- Analizará el alcance, y los Anchos de Banda que se pueden dar en función de diferentes equipos disponibles en la plataforma, eligiendo el más conveniente.
- Propondrá otra opción de radio enlace buscando otro punto que resulte más conveniente para que un repetidor en el caso no tenga una cobertura adecuada.
- Elaborará un informe correspondiente a los datos obtenidos.

Con el objetivo de expansión de nuestra Facultad UTN Regional hacia un nuevo polo Tecnológico ubicado a 8 km, hemos considerado fundamental establecer una conexión eficiente entre las instalaciones actuales y el nuevo predio.

Tras evaluar diversas opciones tecnológicas se ha optado por la implementación de un enlace de radio directo punto a punto. Esta solución permitirá una comunicación rápida y efectiva, garantizando la transmisión de datos necesaria para el desarrollo de nuestras actividades académicas y administrativas.

Como primera alternativa, hemos optado por trazar el enlace de manera directa y en línea recta uniendo los dos puntos:

**_TORRES:_**

Para determinar la altura de las torres necesarias para el enlace entre los sitios, se han recopilado datos sobre los distintos obstáculos presentes en el trayecto. Tras un análisis exhaustivo, se estableció que la altura de las mismas debían ser:

- _Torre #1_ en Predio Principal: Altura estimada **60 metros**
- _Torre #2_ en Predio Polo Tecnológico: Altura estimada **30 metros**

Para llegar a estos resultados se tuvieron en cuenta las distintas alturas de edificios y vegetación que cortaban el enlace entre los dos puntos

- **Primer punto de análisis:**

Edificio ubicado en Av. Sarmiento esquina Monteagudo. El mismo cuenta con 6 pisos más terraza y se estima una altura aproximada de 20 metros. Se encuentra a 220 metros en línea recta del predio principal.

- **Segundo punto de análisis:**

Edificio ubicado en Monteagudo al 800 a mitad de cuadra, de 15 pisos más terraza con altura aproximada de 50 metros. Ubicado a 360 metros en línea recta del predio principal

La línea pasa a 6 metros de altura del edificio más alto, por lo que no tiene corte de señal.

- **Tercer punto de análisis:**

Edificio ubicado en Honduras al 27, de 9 pisos más terraza con altura aproximada de 30 metros. Ubicado a 880 metros en línea recta del predio principal

- **Cuarto punto de análisis:**

Edificio ubicado en Honduras al 47, de 13 pisos más terraza con altura aproximada de 45 metros. Ubicado a 900 metros en línea recta al predio principal.


La línea pasa a 10 metros de altura de la planta superior del edificio más alto.

**_EQUIPOS:_**

Se consideraron el análisis de prestacion de 3 equipos de conexión de la marca UBIQUITI:

- **AirFiber 60**


**_Características:_**

El AF60 LR es una radio de **60 GHz** diseñada para proporcionar conectividad de alto rendimiento en un rango extendido. El airFiber 60 LR cuenta con la antena parabólica de alta ganancia integrada para enlaces punto a punto (PtP) de alta velocidad y rendimiento de largo alcance a distancias de hasta 12 km. La nueva tecnología Wave permite un rendimiento increíble de largo alcance dentro del espectro de 60 GHz.

**_Ancho de Banda:_**

El enlace ofrece un ancho de banda de hasta **1.95 Gbps** operando en la banda de frecuencia de 60 GHz, lo que lo hace ideal para transmisiones a alta velocidad en distancias cortas a medias. Esta frecuencia permite una alta capacidad de transmisión y baja latencia.

**_Señal Esperada:_**

Un nivel de señal de -57 dBm es, efectivamente, un buen indicador para enlaces a distancia. Este valor sugiere que la señal es suficientemente fuerte para mantener una comunicación estable y de calidad. En general, se considera que las señales por encima de -70 dBm son aceptables, mientras que -60 dBm y -50 dBm son ideales para un rendimiento óptimo. Si las dos antenas están recibiendo esta potencia, es probable que el enlace esté funcionando bien y que no haya problemas significativos de interferencia o atenuación.

- **Wave Pro**


**_Características:_**

Radio de 60 GHz de alta capacidad que admite enlaces PtP (puente) y PtMP de larga distancia. Alcance máximo del enlace:

- PtP: hasta 15 km
- PtMP: hasta 8 km (Wave AP), hasta 6 km (Wave AP Micro)

**_Ancho de Banda:_**

El enlace ofrece un ancho de banda de hasta **3.20 Gbps** operando en la banda de frecuencia de 60 GHz.

**_Señal Esperada:_**

Un nivel de señal de -49 dBm es, efectivamente, un buen indicador para enlaces a distancia. Este valor sugiere que la señal es suficientemente fuerte para mantener una comunicación estable y de calidad.


**_Ancho de Banda:_**

El enlace ofrece un ancho de banda de hasta **404 Mbps** operando en la banda de frecuencia de 5 GHz, lo que se descarta para el análisis del trabajo con esta frecuencia.

- **AirFiber 60 Xtreme**


**_Características:_**

Puente multigigabit de 60 GHz diseñado para crear enlaces de larga distancia y ofrecer un rendimiento total de 5,4 Gbps (dúplex de 2,7 Gbps) a través de ellos. Alcance del enlace de más de 15 km

**_Ancho de Banda:_**

El enlace ofrece un ancho de banda de hasta **2.70 Gbps** operando en la banda de frecuencia de 60 GHz

**_Señal Esperada:_**

Un nivel de señal de -47 dBm es, efectivamente, un buen indicador para enlaces a distancia. Este valor sugiere que la señal es suficientemente fuerte para mantener una comunicación estable y de calidad.

**_CLIMA:_**

Uno de los aspectos más críticos que puede afectar la calidad y la estabilidad de estas conexiones es el factor climático. Las condiciones meteorológicas, como la lluvia, la nieve, la niebla y la variabilidad de la temperatura, pueden interferir significativamente en la propagación de las señales de radiofrecuencia. Este fenómeno se debe a la atenuación de la señal, la dispersión y otros efectos que resultan de la interacción entre las ondas electromagnéticas y el ambiente atmosférico. Por lo tanto, entender cómo el clima impacta estas conexiones no solo es esencial para optimizar su rendimiento, sino también para diseñar sistemas de comunicación más resilientes ante los desafíos que presenta la naturaleza.


Teniendo en cuenta el promedio de lluvias que se da en las zonas de instalación de los equipos, según se muestra en el cuadro hemos procedido a analizar cómo se comparta la señal ante esta interferencia.


Podemos observar que la pérdida que se produciría en el ancho de banda no es significativa.

Si bien los valores que hemos obtenido satisfacen nuestras expectativas, y con el propósito de continuar en la investigación de la mejor opción hemos definido una alternativa a la ya propuesta.


La misma consiste en colocar un repetidor en el predio de **Lince Rugby Club** donde actualmente ya se encuentra montada una antena que podría ser de Telecom o Claro de 30 metros aproximadamente de altura. (que demandaría algún convenio o acuerdo con la UTN para su uso) u opcionalmente montar una antena adicional de 20-30 metros de altura en un radio de 15 metros a la redonda del punto. Lo que demandaría de igual forma un acuerdo con terceros.


No consideramos la colocación de la antena en la zona oeste de la Av. Circunvalación ya que la zona es propensa al vandalismo.

**_TORRES:_**

- _Torre #1_ en Predio Principal: Altura estimada **60 metros**
- _Torre #2_ en Predio Lince Rugby Club: Altura estimada **30 metros**
- _Torre #3_ en Predio Polo Tecnológico: Altura estimada **20 metros**

Para el análisis de las alturas, se consideraron los distintos obstáculos que se presentan en los enlaces a los puntos de conexión

- **Primer punto de análisis:**


- Edificio ubicado sobre calle Monteagudo entre Santa Fe y Marcos Paz de 15 pisos más terraza con altura aproximada de 45 metros. Ubicado a 500 mtros en línea recta del punto principal de conexión


- **Segundo punto de análisis:**


- Edificio ubicado sobre calle Balcarce y Corrientes de 13 pisos más terraza con altura aproximada de 45 metros. Ubicados a 700 metros en línea recta


- Edificio ubicado sobre calle Balcarce y Marcos paz de 13 pisos más terraza con altura aproximada de 45 metros ubicados a 600 metros en línea recta.


- **Tercer punto de análisis:**


- Edificio ubicado sobre Av. Soldati y Cuba de 15 pisos más terraza con altura aproximada de 45 metros. Ubicado a 1400 mtrs de punto de inicio.


Dado que las alturas del trazado estaban muy cercanas a la altura de los edificios se extendió la altura de la torre a 30 metros.

**_EQUIPOS:_**

Para el análisis se consideraron los mismos equipos enunciados en la primera opción:


La evaluación de la alternativa muestra que, a pesar de la reducción en la potencia de señal del segundo enlace en un promedio de -**10 dBm**, esta alternativa sugiere acuerdos con terceros para el uso de espacio y antena.

Aun así, sin tener en cuenta estos acuerdos. La alternativa propuesta brinda una mejor solución al desafío de conectar los dos puntos.

Además, al compararlo con un radio enlace directo, que presenta una señal más débil y susceptible a variaciones, el segundo enlace punto a punto no solo cumple con los requisitos de ancho de banda, sino que también minimiza las interrupciones y maximiza la calidad de la conexión.
