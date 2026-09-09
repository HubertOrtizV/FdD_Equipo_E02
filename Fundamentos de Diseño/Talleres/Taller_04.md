# Estado del Arte: Búsqueda de Patentes

Este documento recopila el análisis de patentes y modelos de utilidad relevantes para el desarrollo del proyecto de ingeniería, identificando soluciones técnicas existentes, mecanismos de control y elementos de diseño aprovechables.

---

## Patente 1

* **Título:** Automatic watering type plastic flowerpot
* **Código:** CN213662652U
* **¿Qué aporta?:** 
  * Automatización del riego según la demanda hídrica real del sustrato (lazo cerrado), independientemente de las condiciones climáticas externas (días soleados o nublados).
  * Diseño modular e integrado que consolida en un solo cuerpo el depósito de almacenamiento inferior, el área de cultivo, el mecanismo de drenaje matricial y los compartimentos de actuadores/sensores, reduciendo mangueras externas y riesgo de fugas.
* **Características / Valores:**
  * **Estructura:** Cuerpo de plástico con reservorio inferior integrado, orificios de drenaje matriciales a intervalos regulares en el fondo de la cavidad interna y visor transparente para inspección del nivel de agua.
  * **Detección:** Sensor de humedad fijado lateralmente en la cavidad interna en contacto directo con el sustrato.
  * **Actuación y bombeo:** Bomba de succión conectada mediante acople de 3 vías y tubo guía a un cabezal pulverizador superior para distribución homogénea.
  * **Control:** Controlador lógico programable (PLC) montado en la cara lateral que procesa la lectura de sequedad y comanda el encendido/apagado de la bomba.
* **Imagenen**
<img width="300" height="300" alt="maceta_imagen" src="https://github.com/user-attachments/assets/b6d5389a-283f-4b5b-80c0-d21411675224" />

---

## Patente 2 

* **Título:** Intelligent watering flowerpot based on Internet of Things (Red de cosas inteligencia regando maceta)
* **Código:** CN205179867U
* **¿Qué aporta?:** 
  * Resuelve la falta de automatización y la necesidad de supervisión humana constante en el cuidado de macetas domésticas mediante el monitoreo remoto por Internet de las Cosas. Aporta una solución de bajo costo para regar de manera precisa y oportuna según los requerimientos biológicos de la planta, permitiendo al usuario monitorear el estado del sustrato y activar el riego a distancia desde una plataforma o dispositivo inteligente.
* **Características / Valores:**
  * **Estructura / Material:** Cuerpo de maceta estructural con cavidad de plantación superior y reservorio de almacenamiento hídrico en la base; incorpora canales de distribución de líquido internos y ranuras de montaje para alojar la circuitería sin invadir el volumen radicular.
  * **Sensores / Detección:** Sensor de humedad del suelo insertado en el sustrato para medir el contenido hídrico y sensor de nivel de agua para supervisar la reserva del depósito.
  * **Actuadores / Mecanismos:** Microbomba de agua sumergible de bajo voltaje conectada a tuberías de conducción y boquillas de microgoteo para dosificación localizada.
  * **Unidad de procesamiento:** Módulo de control microcontrolado con interfaz de comunicación inalámbrica (transceptor de red/IoT) que recopila las lecturas de los sensores, transmite los datos a la red y comanda la etapa de potencia de la bomba.
<img width="1107" height="552" alt="imagen_de_patente" src="https://github.com/user-attachments/assets/a550c71b-7dd4-4262-acad-fa23c19c153e" />

---

## PATENTE 3

### 3.1 TÍTULO

**Sistema portátil basado en IoT para riego y fertilización automáticos**

### 3.2 CÓDIGO

**AU2021103425A4**

### 1.3 ¿QUÉ APORTA?

Esta patente propone un sistema portátil que automatiza el riego y la fertilización mediante tecnología IoT. Utiliza sensores para medir las condiciones del suelo y del ambiente, permitiendo controlar el suministro de agua según las necesidades detectadas. También permite transmitir y almacenar los datos obtenidos para realizar el monitoreo del cultivo. Con este sistema se busca utilizar el agua de manera más controlada y reducir el riego innecesario.

### 3.4 CARACTERÍSTICAS / VALORES

| Característica | Valor / Descripción |
|---|---|
| **Humedad del suelo** | Medida mediante sensor y comparada con un valor límite configurable |
| **Temperatura** | Monitoreada mediante sensores |
| **Humedad ambiental** | Monitoreada por el sistema |
| **pH del suelo** | Escala de 1 a 14 |
| **pH para la mayoría de plantas** | Aproximadamente entre 5 y 7 |
| **Nivel de agua** | Sensor para detectar el nivel del tanque |
| **Radiación** | Considerada como variable ambiental |
| **Velocidad del aire** | Considerada como parámetro de entrada |
| **Comunicación** | ZigBee y Wi-Fi |
| **Módulo Wi-Fi** | ESP8266 |
| **Sistema de control** | Red neuronal artificial (ANN) |
| **Accionamiento** | Bomba/motor y válvulas con control ON/OFF |
| **Riego** | Microirrigación automatizada |
| **Fertilización** | Sistema de fertirrigación integrado |
| **Monitoreo** | Almacenamiento y transmisión de los datos obtenidos |
**IMAGEN**
<img width="541" height="387" alt="Captura de pantalla 2026-09-09 110524" src="https://github.com/user-attachments/assets/043e8e2b-9579-4f1f-8b54-7c6c2e0eb1e3" />


