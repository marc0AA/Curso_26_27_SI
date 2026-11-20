# Puzzle de componentes · Pieza 09: Fuente de alimentación (PSU)

**Grupo:** Marco Ariza · Antonio Montero  
**Presentación:** [Fuente de alimentación (Genially)](https://view.genially.com/6aec404e6807e230394f80cf)
## Resumen

*Fuente de alimentación (Power Man) del equipo del taller UT2, extraída de la caja. Foto propia.*

### 1. Qué es y cómo funciona

La **fuente de alimentación** convierte la **corriente alterna (AC)** de la red (230 V, 50 Hz) en **corriente continua (DC)** de bajo voltaje: **rectifica, transforma, estabiliza y protege**. Es una fuente **conmutada (SMPS)**:

**Filtro EMI → rectificador + condensador → PFC activo → troceador + transformador de alta frecuencia → rectificación y filtro → salidas DC**, con un **control PWM** que mantiene estable la salida.

El **PFC activo** (*Power Factor Correction*) **mejora el factor de potencia**: aprovecha mejor la corriente que toma de la red. El transformador reduce la tensión y **aísla** la salida de la red.

### 2. Raíles y colores

- **+12 V (amarillo):** CPU, GPU, ventiladores y motor de los discos. Es el que **más potencia** da.
- **+5 V (rojo):** lógica de SSD/HDD y USB. **+3,3 V (naranja):** memoria y placa.
- **+5VSB (morado):** placa en espera (*standby*). **−12 V (azul):** casi sin uso. **Masa (negro).**
- Tolerancia: **±5 %** en +12 V y +5 V, y ±10 % en −12 V.

### 3. Magnitudes y medidas

- **Voltio (V):** tensión de cada raíl. **Amperio (A):** corriente máxima de un raíl. **Vatio (W):** potencia, P = V · I (62,5 A × 12 V = **750 W**).
- **Eficiencia (%):** η = P_salida / P_entrada · 100, medida con carga conocida y vatímetro en la entrada. Con η = 90 % y 500 W de salida, la entrada es 500 / 0,9 ≈ **556 W**; el resto se pierde en calor.
- **Rizado (mV):** ondulación residual sobre la DC, medida con osciloscopio. **Ruido (dB(A)):** con sonómetro. **Hold-up (ms):** tiempo que mantiene la salida ante un microcorte.

### 4. Tipos y evolución

- **Formato:** ATX, SFX, TFX, Flex ATX. **Cableado:** no modular, semimodular o modular.
- **AT** (interruptor mecánico) → **ATX 1995** (apagado por software y +5VSB) → **ATX12V** (conector de +12 V de 4 pines para la CPU y, desde la v2.0, 24 pines en la placa) → **ATX 3.0 (2022)**, con el conector 12VHPWR → **ATX 3.1 (2023)**, con el 12V-2x6.

### 5. Eficiencia: 80 PLUS

De menor a mayor: **Estándar < Bronze < Silver < Gold < Platinum < Titanium**. Cada nivel exige más eficiencia a la misma carga (20 %, 50 % y 100 %). Ejemplo **Gold (115 V): 87 %, 90 % y 87 %**, es decir, rinde más a media carga. **Cybenetics** valora además el ruido.

### 6. Claves y seguridad

- **Fuentes modulares: usa solo los cables de tu fuente.** Los conectores del lado de la fuente pueden encajar, pero cada marca o modelo puede asignar los 12 V y la masa a patillas distintas, y un cable ajeno puede dañar la fuente y los componentes.
- Averías típicas: condensadores hinchados, ventilador bloqueado, fusible quemado y apagados bajo carga.
- Dentro hay **tensión peligrosa** aunque esté desenchufada: no se abre.

## Preguntas tipo test

**1. ¿Qué raíl suministra la mayor parte de la potencia en una fuente ATX moderna?**

- a) +3,3 V
- b) +5 V
- c) +12 V ✅
- d) −12 V

*Explicación:* el raíl de +12 V alimenta a los componentes que más consumen (CPU, GPU y ventiladores), por eso concentra la mayor parte de la potencia. Los raíles de +5 V y +3,3 V se reservan para lógica, memoria y USB, y el de −12 V casi no se usa.

**2. ¿Qué función tiene la etapa PFC activa?**

- a) Refrigerar el transformador
- b) Mejorar el factor de potencia ✅
- c) Convertir DC en AC
- d) Detectar cortocircuitos en la salida

*Explicación:* el PFC (*Power Factor Correction*) hace que la fuente aproveche mejor la corriente que toma de la red, lo que mejora el factor de potencia. No refrigera ni protege: esas funciones son del ventilador y de los circuitos de protección.

**3. Una fuente entrega 500 W y consume 556 W de la red. ¿Cuál es su eficiencia aproximada?**

- a) 80 %
- b) 85 %
- c) 90 % ✅
- d) 95 %

*Explicación:* η = P_salida / P_entrada · 100 = 500 / 556 · 100 ≈ 89,9 %, es decir, alrededor del 90 %. Los 56 W de diferencia se pierden en forma de calor.

**4. ¿Cuál es el orden correcto de certificaciones 80 PLUS de menor a mayor eficiencia?**

- a) Gold, Silver, Bronze, Platinum
- b) Bronze, Silver, Gold, Platinum ✅
- c) Silver, Bronze, Platinum, Gold
- d) Platinum, Gold, Silver, Bronze

*Explicación:* los niveles van de menor a mayor eficiencia así: Estándar, Bronze, Silver, Gold, Platinum y Titanium. Cada nivel exige un porcentaje mayor que el anterior para las mismas cargas (20 %, 50 % y 100 %).

**5. ¿Qué error es más peligroso al instalar una fuente modular?**

- a) Dejar un cable sin usar
- b) Usar cables de otra fuente modular, aunque encajen ✅
- c) Usar menos conectores de los disponibles
- d) Montarla con el ventilador hacia abajo

*Explicación:* los conectores del lado de la fuente pueden ser idénticos entre modelos y marcas, pero la asignación de patillas (12 V y masa) no tiene por qué serlo. Un cable ajeno puede encajar y poner 12 V donde va masa, y dañar la fuente y los componentes. Las otras opciones son inofensivas: no hace falta usar todos los cables ni todos los conectores.

## Uso de IA

- **Herramienta y fecha:** Claude (Anthropic), 20/11/2026.
- **Para qué la usamos:** Claude nos ayudó a preparar el resumen y la presentación en Genially, a revisar el resumen para que cubra todo lo necesario para responder el test y lo que explicamos en la presentación, y a buscar fuentes con las que contrastar los datos.
- **Qué comprobamos y resultado:**
  - La tabla de eficiencias 80 PLUS (115 V) coincide con las fuentes: **confirmada**.
  - Los colores de los cables de los raíles coinciden con lo recomendado por ATX: **confirmada**.
  - Que los cables de fuentes modulares no son intercambiables aunque encajen: **confirmada** por NZXT y ASUS.
  - Que ATX12V trajo el conector de 4 pines para la CPU y la versión 2.0 el de 24 pines: **confirmada**.
  - Nuestro resumen decía que ATX 3.1 era de 2024, pero fue lanzado en septiembre de 2023: **corregida**.
  - Decía ±5 % para el raíl de +3,3 V, pero ATX 2.1 indica ±4 %: **corregida** (en el resumen solo damos la tolerancia de +12 V y +5 V).
  - Que la fuente debe tener un 20–30 % de margen era una regla orientativa que no pudimos contrastar, y la hemos sustituido por lo que sí aparece en las tablas: la eficiencia es mayor a media carga.

## Fuentes

- Tom's Hardware, *What do 80 PLUS levels mean?*: <https://www.tomshardware.com/news/what-80-plus-levels-mean,36721.html>
- Hardware Secrets, *Understanding the 80 Plus certification*: <https://hardwaresecrets.com/understanding-the-80-plus-certification/3/>
- PC Gamer, *Cybenetics ratings* (eficiencia y ruido): <https://pcgamer.com/hardware/power-supplies/corsair-ditches-80-plus-for-psus-here-are-the-cybenetics-ratings-itll-use-instead>
- AnandTech, *XPG Core Reactor II VE 850W (ATX 3.1)*, fechas de ATX 3.0 y 3.1 y conector 12V-2x6: <https://www.anandtech.com/show/21367/the-xpg-core-reactor-ii-ve-850w-atx-31-psu-review/2>
- XPG Knowledge Hub, *ATX 3.1 and 12V-2x6 power supply standard* (ATX de Intel, 1995; 12VHPWR de 600 W; picos del 200 %): <https://www.xpg.com/lb/knowledgehub/power-supply-unit/95>
- O'Reilly, *PC Hardware in a Nutshell*, tolerancias de los raíles ATX 2.1: <https://www.oreilly.com/library/view/pc-hardware-in/059600513X/ch26s02s01.html>
- O'Reilly, *PC Hardware in a Nutshell*, conector de +12 V de 4 pines de ATX12V: <https://www.oreilly.com/library/view/pc-hardware-in/059600513X/ch26s03s05.html>
- Tom's Hardware, *ATX12V 2.0* (conector de 24 pines): <https://www.tomshardware.com/reviews/performance,946-2.html>
- SpeedGuide, *Wire color coding of ATX power supplies*: <https://speedguide.net/faq_in_q.php?qid=401>
- NZXT, *Why modular cables are not interchangeable*: <https://nzxt.com/blogs/news/psu-cable-compatibility>
- ASUS, *PSU modular cable connection guide*: <https://www.asus.com/us/support/faq/1056866/>
- Corsair, *ATX 3.0 vs ATX 3.1* (definición de hold-up): <https://www.corsair.com/kr/no/explorer/diy-builder/power-supply-units/atx-30-vs-atx-31-whats-the-difference/>
- Presentación del grupo en Genially: <https://view.genially.com/6aec404e6807e230394f80cf>
- Fotos propias del taller UT2 (carpeta `imagenes/`).
