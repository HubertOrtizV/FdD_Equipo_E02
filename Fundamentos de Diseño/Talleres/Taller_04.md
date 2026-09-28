# Búsqueda de Patentes

Este documento recopila el análisis de patentes relevantes para el desarrollo del **Sistema Inteligente de Riego Automatizado y Monitoreo para Espacios Verdes Urbanos**, identificando soluciones técnicas existentes, mecanismos de control y elementos de diseño aprovechables.

---

## Patente 1

* **Título:** System and method for garden monitoring and management
  *(Sistema y método para el monitoreo y manejo de jardines)*
* **Código:** US 2015/0164009 A1
* **Tipo de documento:** Solicitud de patente (EE. UU.). Presentada el 11-dic-2014 y publicada el 18-jun-2015.
* **Autores / Titulares:** A. Chandran y R. R. Brimble (Robert Bosch GmbH y Fiskars Oyj).

### ¿Qué aporta?
* Resuelve el problema del riego con temporizador estático, que gasta agua cuando llueve y no considera el estado del suelo.
* Une en un solo sistema el riego automatizado y el monitoreo remoto: el usuario ve las lecturas de los sensores y controla el riego desde el celular o el computador.
* Después de una etapa de aprendizaje puede seguir regulando el riego sin sensores, con el historial guardado y el pronóstico del clima.

### ¿Cómo funciona?
1. **Medición:** los sensores, clavados en el suelo cerca de cada planta, miden humedad, temperatura, pH y luz, y envían los datos por Wi-Fi a un servidor.
2. **Evaluación:** el servidor compara cada lectura con los valores recomendados para esa planta (base de datos hortícola) y la clasifica como buena, mala o pobre. Si es mala, avisa al usuario por mensaje de texto o correo.
3. **Riego:** el temporizador programable se enciende cuando la humedad baja del nivel recomendado y se apaga cuando lo supera. El usuario también puede encenderlo o apagarlo a mano.
4. **Ajuste por clima y agua:** el servidor consulta el servicio meteorológico y pospone el riego si se espera lluvia. También consulta las restricciones del servicio de agua (volumen y horario) y puede fijar un tope de gasto mensual.
5. **Aprendizaje:** el servidor guarda el historial de riego, humedad y lluvia. Luego estima la humedad con el pronóstico, sin necesitar el sensor, que puede moverse a otra planta.
6. **Respaldo:** si falla la red, sensores y temporizadores se comunican punto a punto por Bluetooth o Zigbee.

### Características / Valores
* **Estructura / Sistema:** sensores distribuidos en el jardín, temporizadores programables, punto de acceso inalámbrico, servidor y dispositivo del usuario (celular o PC).
* **Sensores / Detección:** humedad del suelo, temperatura del suelo y del aire, pH e intensidad de luz.
* **Actuadores / Mecanismos:** temporizadores programables que controlan el riego, el fertilizante, la temperatura y la iluminación.
* **Unidad de procesamiento / Comunicación:** servidor web o en la nube (también puede estar dentro de un temporizador). Comunicación Wi-Fi 802.11 y, como respaldo, Bluetooth o Zigbee.
* **Fuentes de datos externas:** base de datos de requerimientos de plantas, servicio de agua municipal y servicio meteorológico.
* **Ejemplos de restricción de agua:** 5 galones por 100 pies² en 24 h y riego solo de 4 a 6 AM y de 8 a 10 PM.

### Imagen
<img width="788" height="652" alt="Captura de pantalla 2026-09-27 223530" src="https://github.com/user-attachments/assets/203a38c5-54c9-4c1d-a025-2808db6b285d" />

**Figura 1.** Esquema del sistema de monitoreo y manejo del jardín. Fuente: US 2015/0164009 A1.

| N.° | Parte |
|---|---|
| 102 | Jardín |
| 104A–104C | Sensores en el suelo |
| 108 | Temporizadores programables |
| 112 | Sistema de control de temperatura |
| 116 | Sistema de control de luz |
| 118 | Sistema de riego |
| 119 | Sistema de fertilizante |
| 120 | Router inalámbrico |
| 124 | Servidor |
| 128 | Dispositivo del usuario (celular o PC) |
| 132 | Red de área amplia (Internet) |
| 136 | Base de datos hortícola |
| 140 | Servicio de agua municipal |
| 144 | Servicio meteorológico |

---

## Patente 2

* **Título:** Irrigation system with soil moisture based seasonal watering adjustment
  *(Sistema de riego con ajuste estacional según la humedad del suelo)*
* **Código:** US 8,660,705 B2
* **Tipo de documento:** Patente concedida (EE. UU.). Presentada el 6-jun-2011 y concedida el 25-feb-2014.
* **Autores / Titulares:** P. J. Woytowitz, J. J. Kremicki y L. D. Porter (Hunter Industries, Inc.).

### ¿Qué aporta?
* Resuelve el problema del horario fijo: corrige automáticamente el tiempo de riego con la humedad real del suelo, sin que el usuario tenga que reajustar el porcentaje estacional a mano.
* Conserva el controlador con horario que el usuario ya conoce y le agrega un módulo de humedad de suelo, en lugar de reemplazarlo.
* Reduce el desperdicio de agua sin dejar las plantas sin riego.

### ¿Cómo funciona?
1. **Programación base:** el usuario escribe en el controlador el horario de riego (hora de inicio, tiempo de riego y días).
2. **Medición:** un sensor enterrado a la profundidad de la raíz mide la humedad del suelo; opcionalmente se agrega un sensor de temperatura del suelo o del aire.
3. **Cálculo:** la unidad de humedad calcula un valor de requerimiento de humedad con esa lectura.
4. **Corrección:** la unidad envía un valor de ajuste al controlador, que aumenta o disminuye por porcentaje el tiempo de riego del horario.
5. **Riego:** durante el tiempo de riego, el controlador activa las válvulas con 24 V AC para que el agua llegue a los aspersores.
6. **Autoajuste:** si el suelo no alcanza la humedad correcta al terminar el ciclo, sube el porcentaje. Si el suelo ya estaba húmedo mientras el riego seguía, lo baja después, hasta que el tiempo de riego coincida con el necesario.
7. **Restricciones:** una ventana sin riego permite anular el calendario en los horarios prohibidos, y el usuario puede subir o bajar el ajuste general con dos botones.

### Características / Valores
* **Estructura / Sistema:** controlador de riego independiente, unidad independiente de humedad de suelo y sensor de humedad. También puede ser un módulo insertable o una sola caja con todo integrado.
* **Sensores / Detección:** humedad del suelo y, de forma opcional, temperatura del suelo o del aire. Para sensores resistivos mide con polaridad alterna, de modo que el voltaje promedio sea cero y se evite la corrosión galvánica.
* **Actuadores / Mecanismos:** válvulas solenoide de 24 V AC activadas con interruptores de estado sólido (triacs).
* **Unidad de procesamiento:** microcontrolador PIC18F65J90 en la unidad de humedad y batería de respaldo CR2032 para mantener el reloj.
* **Valores de ajuste:** el ajuste estacional manual típico va de cerca de 10 % a 150 % o más. La unidad de humedad puede llevar el riego desde 0 % hasta más de 100 % del horario.

### Imágenes

<img width="958" height="564" alt="Captura de pantalla 2026-09-27 224804" src="https://github.com/user-attachments/assets/d99740e9-8e8c-44f3-b7b2-e516cf5e4da5" />


**Figura 1.** Diagrama de bloques simplificado del sistema de riego. Fuente: US 8,660,705 B2.

| N.° | Parte |
|---|---|
| 10 | Sistema de riego |
| 12 | Controlador de riego independiente |
| 14 | Cable entre el controlador y la unidad de humedad (lleva energía, datos y comandos) |
| 16 | Unidad independiente de control de humedad del suelo |
| 18 | Cable entre la unidad de humedad y el sensor |
| 20 | Sensor de humedad del suelo (enterrado a la profundidad de la raíz) |
| 22 y 24 | Enlaces de comunicación inalámbrica opcionales entre el controlador, la unidad y el sensor |
| 25 | Transformador que convierte 110 V AC de la red en 24 V AC para el controlador |

<img width="898" height="573" alt="Captura de pantalla 2026-09-27 224812" src="https://github.com/user-attachments/assets/2e068c76-f84e-42b9-9f57-6a4a5cd98ad6" />


**Figura 2.** Vista frontal del controlador de riego con la puerta abierta para mostrar el panel frontal removible. Fuente: US 8,660,705 B2.

| N.° | Parte |
|---|---|
| 26 | Puerta frontal (con bisagra en un borde vertical) |
| 28 | Panel posterior |
| 30 | Panel frontal removible (contiene la interfaz y el procesador) |
| 31 | Perilla giratoria para programar |
| 32a–32g | Botones pulsadores (32c y 32d suben y bajan el ajuste estacional) |
| 34 | Interruptor deslizante para puentear (desactivar) el sensor |
| 36 | Pantalla LCD donde se ven los horarios de riego |

<img width="746" height="768" alt="Captura de pantalla 2026-09-27 224839" src="https://github.com/user-attachments/assets/96cce0ef-3e95-48c1-9f23-1ca62dbe7075" />


**Figura 3.** Vista en perspectiva del panel posterior del controlador con un módulo base y un módulo de estación conectados. Fuente: US 8,660,705 B2.

| N.° | Parte |
|---|---|
| 28 | Panel posterior |
| 44 | Módulo base (puede abrir y cerrar la válvula maestra y varias válvulas de estación) |
| 46a | Módulo de estación (conmuta 24 V AC hacia las válvulas solenoide) |
| 48 | Terminales de tornillo para los cables de las válvulas |
| 50 | Barra de bloqueo que se desliza entre las posiciones bloqueado y desbloqueado |
| 52 | Salientes de la barra de bloqueo para moverla con el pulgar |
| 54 | Indicador que señala BLOQUEADO o DESBLOQUEADO |
| 56 | Estructura plástica de soporte con las marcas de bloqueo |
| 58 y 60 | Paredes verticales que forman las ranuras de los módulos y los sostienen |
| 62 | Terminales de tornillo auxiliares para conectar sensores remotos y accesorios |

---

## Patente 3

* **Título:** Method and system for reduction of irrigation runoff
  *(Método y sistema para la reducción del escurrimiento de riego)*
* **Código:** US 9,955,636 B2
* **Tipo de documento:** Patente concedida (EE. UU.). Prioridad del 21-jul-2015.
* **Autores / Titulares:** B. G. Wherley *et al.* (The Texas A&M University System).

### ¿Qué aporta?
* Resuelve el desperdicio que ocurre cuando el agua se aplica más rápido de lo que el suelo puede absorber y se escurre hacia la calle o las propiedades vecinas.
* Aporta una variable que las otras patentes no usan, el escurrimiento, y un método para validar el ahorro con un grupo de control, un caudalímetro y la humedad del suelo antes y después.
* Reporta resultados medidos: 31 % de reducción promedio del escurrimiento y 38 galones de agua ahorrados por evento.

### ¿Cómo funciona?
1. **Riego programado:** el sistema riega según el programa del controlador (en la prueba, 30 minutos).
2. **Medición del escurrimiento:** un sensor en el borde de la zona (cordón de la calle, límite del jardín o tubería de drenaje) mide continuamente el caudal de agua que sale.
3. **Pausa:** si el caudal supera el primer umbral, el controlador ordena al relé cortar la corriente de la válvula, y esta se cierra. El agua se infiltra durante la pausa.
4. **Reanudación:** el sensor sigue midiendo durante la pausa. Cuando el caudal baja del segundo umbral (más bajo que el primero, para evitar que la válvula se encienda y apague sin parar), el controlador reabre la válvula.
5. **Repetición:** el ciclo de riego y pausa continúa hasta completar el tiempo de riego deseado o hasta agotar la ventana permitida de 6 a 24 horas.
6. **Instalación:** puede funcionar solo o como complemento de un controlador existente, conectado mediante un relé.

### Parámetros que miden los sensores
| Parámetro | Qué mide / sensor | Unidad | Uso |
|---|---|---|---|
| Caudal de escurrimiento en el límite de la zona | Sensor de paleta (velocidad de giro de la paleta), de flotador (posición del flotador por la diferencia entre el caudal que entra y uno de salida conocido) o de conductividad | L/s | Variable de control: decide cerrar o abrir la válvula según dos umbrales |
| Volumen de riego aplicado | Caudalímetro totalizador en la válvula | galones | Evaluación del ahorro de agua |
| Volumen de escurrimiento | Caudalímetros de burbujeo (Teledyne ISOC 4230) al pie de cada parcela | galones y L/s | Evaluación de la reducción del escurrimiento |
| Humedad volumétrica del suelo | Sensor SM200 (Delta-T Devices), profundidad de 0 a 2 pulgadas, promedio de cuatro lecturas por parcela | % | Evaluación de la eficiencia de humedecimiento (antes y después de cada prueba) |

La patente no da valores numéricos para los dos umbrales de escurrimiento; los define el diseño del sistema.

### Características / Valores
* **Estructura / Sistema:** sistema de riego con válvula, relé, sensor de escurrimiento en el límite de la zona y controlador. Sensor de tamaño aproximado 6 × 6 × 12 pulgadas para instalarse en un tramo de cordón.
* **Actuadores / Mecanismos:** válvula que se cierra al cortar la corriente y controlador que produce ciclos de riego y pausa (3 a 5 ciclos por evento). Pausas de aproximadamente 10 a 60 minutos.
* **Unidad de procesamiento / Alimentación:** controlador de 1 a n zonas (nueve o más), alimentado por batería, energía solar o la red eléctrica.
* **Resultados de prueba (2 parcelas de césped, suelo franco arenoso fino, pendiente de 3.5 %, riego de 2 pulgadas por hora):**
  * Caudal máximo de escurrimiento: menos de 0.02 L/s con el sistema, frente a 0.25 L/s en el control.
  * Reducción del escurrimiento: de 37 % a 56 % por prueba y 31 % de promedio en 2016.
  * Ahorro de agua: 38 galones por evento en promedio.
  * Eficiencia de humedecimiento del suelo: 63 % mayor en promedio.
* **Nota:** estos resultados son los reportados por la propia patente, en un solo sitio y con un solo tipo de suelo.

### Imagen
<img width="679" height="718" alt="Captura de pantalla 2026-09-27 225519" src="https://github.com/user-attachments/assets/27bcc287-bf06-4ccc-a31c-c5431a06c86c" /><img width="674" height="755" alt="Captura de pantalla 2026-09-27 225534" src="https://github.com/user-attachments/assets/39f9d79b-5c1c-4dbe-8619-681d2b4bce0e" />



**Figuras 1A y 2A.** Diagrama de bloques del sistema y su instalación en un cordón de la calle. Fuente: US 9,955,636 B2.

| N.° | Parte |
|---|---|
| 102 | Sensor de escurrimiento |
| 104 | Sistema de riego |
| 106 | Controlador |
| 202 | Cordón (borde de la calle) donde se instala el sensor |
| 204 | Jardín residencial |
| 205 | Calle |
| 206 | Salida de agua (aspersor) |

---

## Referencias

[1] A. Chandran y R. R. Brimble (Robert Bosch GmbH y Fiskars Oyj), "System and method for garden monitoring and management," U.S. Patent Appl. 2015/0164009 A1, 18 jun. 2015.

[2] P. J. Woytowitz, J. J. Kremicki y L. D. Porter (Hunter Industries, Inc.), "Irrigation system with soil moisture based seasonal watering adjustment," U.S. Patent 8 660 705 B2, 25 feb. 2014.

[3] B. G. Wherley *et al.* (The Texas A&M University System), "Method and system for reduction of irrigation runoff," U.S. Patent 9 955 636 B2, [completar fecha de concesión].



