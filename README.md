# 🌐 [Nombre del Proyecto]

> **Curso Académico:** 20XX/20YY  
> **Fecha de última actualización:** DD/MM/20AA  

---

## 👥 Bloque 1: Gestión, Documentación y Estado del Arte

### 1.1. Equipo de Trabajo y Dedicación
Describe los integrantes del equipo, sus roles principales y el desglose de dedicación/aportación al proyecto (debe reflejarse también en el historial de *commits* del repositorio).

| Nombre y Apellidos | Usuario GitHub | Rol Principal (HW / Firmware / Backend / App / Docs) | Horas estimadas | Tareas principales desarrolladas |
| :--- | :--- | :--- | :---: | :--- |
| Alumno/a 1 | `@usuario1` | ... | XX h | ... |
| Alumno/a 2 | `@usuario2` | ... | XX h | ... |
| Alumno/a 3 | `@usuario3` | ... | XX h | ... |

---

### 1.2. Escenario, Problema e Hipótesis de Solución
- **Escenario de aplicación:** *(Describe de forma narrativa o técnica la situación real, el entorno físico y los actores involucrados).*
- **Resumen ejecutivo (máx. 250 palabras):** *(Describe el problema detectado y vuestra hipótesis de solución mediante computación ubicua).*
- **Vídeo promocional y demostración en funcionamiento:**
  - 🔗 [Enlace al Vídeo Demo (YouTube / Vimeo / Drive)](https://...)

---

### 1.3. Estructura del Repositorio
Para facilitar la evaluación y reproducibilidad del proyecto, este repositorio sigue la siguiente estructura de directorios:

```text
├── recursos/              # Recursos multimedia
│   ├── esquemas/          # Diagramas de bloques, esquemáticos eléctricos y vistas protoboard (.fzz, .pdf, .png)
│   ├── arquitectura/      # Diagramas de arquitectura Mist-Edge-Fog-Cloud, secuencia y flujo de datos
│   └── otra-media/        # Audios, recursos multimedia o datasets de prueba organizados en los subdirectorios que necesites
├── hardware-tests/        # Sketches y logs de pruebas empíricas comparativas de sensores/actuadores descartados y elegidos (1 subdirectorio por cada conjunto de pruebas realizado)
├── sources/               # Código fuente final de los sistemas involucrados (Arduino, ESP32, routers, smartphone... 1 subdirectorio por dispositivo)
│   ├── dispositivo 1/     # Código fuente del dispositivo 1
│   ├── dispositivo 2/     # Código fuente del dispositivo 2
│   └── dispositivo 3/     # Código fuente del dispositivo 3
└── README.md              # Memoria principal del proyecto (este documento)
```

---

### 1.4. Estado del Arte y Comparativa de Soluciones
Analiza productos comerciales, proyectos preferiblemente *open-source* y/o literatura académica/patentes similares. Justifica qué aporta vuestro sistema frente a lo existente. Puedes subir imágenes u otros recursos a `/recursos/otra-media/` y enlazarlos aquí.

| Solución / Proyecto / Artículo | Tipo (Comercial / Académico / Open-Source) | Tecnologías que emplea | Limitaciones detectadas | Ventaja diferencial de nuestra propuesta | Coste aprox. |
| :--- | :---: | :--- | :--- | :--- | :---: |
| [Proyecto/Producto 1](https://...) | Comercial | ... | ... | ... | XX € |
| [Proyecto/Producto 2](https://...) | Open-Source | ... | ... | ... | XX € |
| [Artículo/Patente 3](https://...) | Académico | ... | ... | ... | N/A |
| **[Nuestro Proyecto]** | **Prototipo Ubicuo** | **...** | **...** | **Propuesta de valor única** | **XX €** |

---

## 🔧 Bloque 2: Ingeniería Hardware, Software y Despliegue

### 2.1. Evaluación Comparativa de Sensores, Actuadores y Placas
Detalla todas las alternativas de hardware analizadas para cubrir el escenario.
> 💡 Documenta aquí las pruebas experimentales realizadas en el laboratorio comparando distintos sensores/actuadores antes de elegir el definitivo (precisión, consumo, latencia, fiabilidad).

| Función en el sistema | Alternativas evaluadas | Probado en práctica | Métricas / Observaciones obtenidas en pruebas | Componente finalmente elegido y justificación técnica |
| :--- | :--- | :---: | :--- | :--- |
| Microcontrolador / Nodo | Arduino Uno vs. ESP32 vs. Arduino Nano | Enlaza al subdirectorio de `/hardware-tests/` correspondiente | ... | ... |
| Sensor 1 (p. ej. Posición/Presencia) | Sensor A vs. Sensor B | Enlaza al subdirectorio de `/hardware-tests/` correspondiente | ... | ... |
| Sensor 2 (p. ej. Biométrico/Ambiental) | Sensor C vs. Sensor D | Enlaza al subdirectorio de `/hardware-tests/` correspondiente | ... | ... |
| Actuador / Feedback | Actuador X vs. Actuador Y | Enlaza al subdirectorio de `/hardware-tests/` correspondiente | ... | ... |
| Módulo de Comunicación | BLE vs. WiFi vs. LoRa vs. 4G/GSM | Enlaza al subdirectorio de `/hardware-tests/` correspondiente | ... | ... |

---

### 2.2. Esquemas de Conexiones y Diseño Hardware
Incluye el diagrama de montaje (protoboard) o el esquemático eléctrico formal si lo has llevado a cabo (Fritzing, KiCad, Eagle, etc.). *(Nota: se valora la exactitud lógica y eléctrica, asegúrate de que los pines sean legibles).*

- **Vista de conexionado (Protoboard o Esquemático eléctrico formal):**
  ![Esquema de conexiones hardware del dispositivo 1](recursos/esquemas/dispositivo1.png)
  ![Esquema de conexiones hardware del dispositivo 2](recursos/esquemas/dispositivo2.png)
  ![Esquema de conexiones hardware del dispositivo 3](recursos/esquemas/dispositivo3.png)

---

### 2.3. Desarrollo Software/Hardware Original y Complejidad Técnica
Describe la arquitectura del código desarrollado en `/sources/`.
- **Complejidad de sensórica y periféricos integrados:** *(Explica si utilizas buses I2C/SPI/UART avanzados, interrupciones hardware, timers, filtrado de señal, calibración propia o gestión estricta de memoria. Si elegiste un sensor sencillo tras comprobar que era el más idóneo para el problema, justifícalo aquí).*
- **Componentes software desarrollados desde cero vs. librerías de terceros:**
  - **Desarrollo propio:** ...
  - **Librerías empleadas y adaptaciones realizadas:** ...
  - *(Incluye aquí cualquier detalle adicional que quieras especificar de cara a la evaluación).*

---

### 2.4. Puesta en Marcha y Despliegue *Zero-Config*
Explica cómo se instala, configura y despliega un nodo nuevo en un entorno real, sin necesidad de abrir el IDE ni recompilar el código fuente.
- **Mecanismo de aprovisionamiento implementado:** *(p. ej., portal cautivo WiFiManager, aprovisionamiento seguro por QR/NFC/BLE, persistencia en tarjeta SD/EEPROM/NVS, descubrimiento automático de servicios, actualizaciones OTA).*
- **Guía rápida de reproducción del proyecto:**
  1. Paso 1 (Hardware/Firmware): ...
  2. Paso 2 (Servidor/Servicios): ...
  3. Paso 3 (Aplicación/Cliente): ...

---

## 🧠 Bloque 3: Propiedades *Core UbiCom* (Modelo de Poslad — Smart DEI)

Justifica qué nivel de la escala de **Stefan Poslad (*Core UbiCom Model Properties*, Niveles 1 a 5)** alcanza vuestro sistema en cada dimensión y cómo está implementado en el código. Es una valoración subjetiva del propio grupo hacia su trabajo.

### 3.1. Propiedad *Distributed* — Topología y Coordinación
- **Nivel de Poslad alcanzado:** `[ ] Nivel 1 (Networked)` | `[ ] Nivel 2 (Discoverable)` | `[ ] Nivel 3 (Mobile, Ad hoc)` | `[ ] Nivel 4 (Orchestrated)` | `[ ] Nivel 5 Extra (Choreographed)`
- **Justificación técnica y diagrama de comunicación entre nodos (`/recursos/arquitectura/`):**
  *(Explica cómo se descubren, coordinan e intercambian datos los distintos nodos/dispositivos del sistema y qué ocurre si un nodo pierde conexión temporalmente).*

---

### 3.2. Propiedad *Context-Aware* — Conciencia y Adaptación al Contexto
- **Nivel de Poslad alcanzado:** `[ ] Nivel 1 (Context Sensing)` | `[ ] Nivel 2 (Passive Context-aware)` | `[ ] Nivel 3 (Context-composition)` | `[ ] Nivel 4 (Context Control)` | `[ ] Nivel 5 Extra (Active Context-adaptation)`
- **Variables de contexto primario capturadas y combinadas:**

| Variable de Contexto | ¿Capturada? | Sensor / Fuente de datos que la obtiene | Cómo influye o adapta el comportamiento del sistema |
| :--- | :---: | :--- | :--- |
| **Localización (Dónde)** | Sí / No | ... | ... |
| **Identificación (Quién)** | Sí / No | ... | ... |
| **Tiempo (Cuándo)** | Sí / No | ... | ... |
| **Actividad / Estado (Qué)** | Sí / No | ... | ... |

- **Reglas de control vs. adaptación dinámica:** *(Indica si el sistema ejecuta reglas fijas ante el contexto o si modifica dinámicamente sus propios parámetros de comportamiento de forma continua).*

---

### 3.3. Propiedad *iHCI* — Transparencia de Uso e Interacción Implícita
- **Nivel de Poslad alcanzado:** `[ ] Nivel 1 (eHCI & WIMPS)` | `[ ] Nivel 2 (eHCI & Natural UI)` | `[ ] Nivel 3 (User Profiling)` | `[ ] Nivel 4 (Static, episodic user awareness)` | `[ ] Nivel 5 Extra (Dynamic, sequential user awareness)`
- **Justificación de la invisibilidad y experiencia de usuario (*Calm Technology*):**
  *(Explica cómo el sistema evita percibirse como una computadora tradicional, minimiza la atención consciente requerida por el usuario y emplea interacciones implícitas, voz, gestos, presencia o actuación ambiental).*

---

## ⚡ Bloque 4: Inteligencia, Autonomía y Proactividad

### 4.1. Propiedad *AI* — Nivel de Inteligencia y Razonamiento
- **Nivel de Poslad alcanzado:** `[ ] Nivel 1 (Syntactical Interactions)` | `[ ] Nivel 2 (Semantics & Linguistics)` | `[ ] Nivel 3 (Problem solving & Reasoning)` | `[ ] Nivel 4 (Goals & Plans)` | `[ ] Nivel 5 Extra (Handling Uncertainty)`
- **Algoritmos, reglas o modelos implementados:**
  *(Detalla cómo razona el sistema, cómo planifica objetivos o cómo gestiona datos ruidosos, incompletos o inciertos procedentes de los sensores).*

---

### 4.2. Propiedad *Autonomous* — Autogestión Interna y Resiliencia
- **Nivel de Poslad alcanzado:** `[ ] Nivel 1 (Environment-aware)` | `[ ] Nivel 2 (Self-healing)` | `[ ] Nivel 3 (Self-aware)` | `[ ] Nivel 4 (Adaptive, predictive)` | `[ ] Nivel 5 Extra (Autonomic control)`
- **Mecanismos de autogestión y tolerancia a fallos internos:**
  *(Explica cómo monitoriza el sistema su propio estado interno —batería, conectividad, salud de sensores—, cómo se recupera automáticamente ante fallos y si reacciona al cruzar umbrales o ajusta su operación de forma predictiva antes de degradarse).*

---

### 4.3. Proactividad y Calibración de la Anticipación
- **Nivel de calibración percibido:** `[ ] Nula (reactivo)` | `[ ] Muy excesiva o muy baja` | `[ ] Algo excesiva o algo baja` | `[ ] Ideal (momento oportuno)` | `[ ] Calibración dinámica anti-intrusión (Extra)`
- **Anticipación y mecanismos para evitar intrusividad:**
  *(Explica cómo se anticipa el sistema a las necesidades o deseos del usuario/entorno y qué mecanismos incorpora para evitar falsos positivos, actuaciones repetitivas o saturación —p. ej., histéresis, tiempos de enfriamiento/cooldown, confirmación implícita o aprendizaje de rechazo).*

---

## 🚀 Bloque 5: Arquitectura, Viabilidad y Estándares

### 5.1. Distribución *Mist–Edge–Fog–Cloud* de Cómputo y Almacenamiento
Discute y justifica arquitectónicamente cómo habéis repartido el procesamiento y el almacenamiento de datos entre todos los dispositivos del sistema, buscando que **la computación esté siempre lo más cerca posible del nodo final** y evitando transmitir o almacenar históricos brutos innecesarios en servidores intermedios o en la nube. Analiza también el impacto en **latencia, privacidad y coste de comunicación/almacenamiento**.

![Diagrama Mist-Edge-Fog-Cloud](recursos/arquitectura/mist_edge_fog_cloud.png)

| Capa Arquitectónica | Dispositivo(s) en nuestro proyecto | ¿Qué cómputo / filtrado se realiza aquí? | ¿Qué datos se almacenan localmente (y durante cuánto tiempo)? | ¿Qué datos se transmiten a la capa superior y con qué frecuencia? | Justificación (latencia, privacidad, tráfico y almacenamiento) |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Mist** *(Nodo sensor/actuador extremo)* | p. ej., MCU + Sensores | ... | ... | ... | ... |
| **Edge** *(Pasarela local / Smartphone)* | p. ej., App Android / Gateway BLE | ... | ... | ... | ... |
| **Fog** *(Servidor local / Nodo intermedio)* | p. ej., Raspberry Pi / Broker local | ... | ... | ... | ... |
| **Cloud** *(Nube pública / Backend global)* | p. ej., API REST / Base de datos Cloud | ... | ... | N/A | ... |

---

### 5.2. Coste Hardware del Prototipo, Miniaturización Actual y Proyección a 4 Años

#### A) Presupuesto del Prototipo Funcional (BOM Actual)
*(Una tabla por dispositivo).*

- **Dispositivo 1**

| Componente (Módulo de desarrollo) | Cantidad | Precio Unitario (€) | Subtotal (€) | Enlace / Proveedor |
| :--- | :---: | :---: | :---: | :--- |
| Placa de desarrollo / MCU | 1 | XX,XX € | XX,XX € | ... |
| Sensor / Módulo 1 | 1 | XX,XX € | XX,XX € | ... |
| Actuador / Módulo 2 | 1 | XX,XX € | XX,XX € | ... |
| Alimentación / Batería / Carcasa | 1 | XX,XX € | XX,XX € | ... |
| **TOTAL Dispositivo 1** | | | **XX,XX €** | |

- **Dispositivo 2**

| Componente (Módulo de desarrollo) | Cantidad | Precio Unitario (€) | Subtotal (€) | Enlace / Proveedor |
| :--- | :---: | :---: | :---: | :--- |
| Placa de desarrollo / MCU | 1 | XX,XX € | XX,XX € | ... |
| Sensor / Módulo 1 | 1 | XX,XX € | XX,XX € | ... |
| Actuador / Módulo 2 | 1 | XX,XX € | XX,XX € | ... |
| Alimentación / Batería / Carcasa | 1 | XX,XX € | XX,XX € | ... |
| **TOTAL Dispositivo 2** | | | **XX,XX €** | |

- **Dispositivo 3**

| Componente (Módulo de desarrollo) | Cantidad | Precio Unitario (€) | Subtotal (€) | Enlace / Proveedor |
| :--- | :---: | :---: | :---: | :--- |
| Placa de desarrollo / MCU | 1 | XX,XX € | XX,XX € | ... |
| Sensor / Módulo 1 | 1 | XX,XX € | XX,XX € | ... |
| Actuador / Módulo 2 | 1 | XX,XX € | XX,XX € | ... |
| Alimentación / Batería / Carcasa | 1 | XX,XX € | XX,XX € | ... |
| **TOTAL Dispositivo 3** | | | **XX,XX €** | |

**TOTAL PROTOTIPO: XX,XX €**

#### B) Coste y Tamaño del Producto Final Industrializado (Hoy vs. Proyección a 4 Años)
Analiza cómo se reduciría el tamaño, volumen/peso y coste del dispositivo si se sustituyeran las placas de prototipado por chips comerciales integrados concretos (SoC, SiP, MEMS SMD en PCB propia) hoy, y su evolución estimada a **4 años vista**.

| Métrica / Componente | Prototipo Actual (Placas/Módulos) | Dispositivo Final Hoy (SMD / SoC / PCB propia) | Proyección Dispositivo Final a 4 Años | Justificación de tendencias tecnológicas (SoC/MEMS/Baterías) |
| :--- | :---: | :---: | :---: | :--- |
| **Chips principales equivalentes** | p. ej. Arduino Uno + Módulos | p. ej. ATmega328P-AU / nRF52840 SMD | SoC ultra-integrado / eSIM | ... |
| **Dimensiones ($L \times A \times H$ en $\text{mm}$)** | $\text{XX} \times \text{YY} \times \text{ZZ}\text{ mm}$ | $\text{XX} \times \text{YY} \times \text{ZZ}\text{ mm}$ | $\text{XX} \times \text{YY} \times \text{ZZ}\text{ mm}$ | ... |
| **Volumen aproximado ($\text{mm}^3$ / $\text{cm}^3$) y Peso ($\text{g}$)** | $\text{XX cm}^3$ / $\text{XX g}$ | $\text{XX cm}^3$ / $\text{XX g}$ | $\text{XX cm}^3$ / $\text{XX g}$ | ... |
| **Coste unitario HW estimado (lote 1.000 uds.)** | XX,XX € | XX,XX € | XX,XX € | ... |

**TOTAL PRODUCTO FINAL (4 años vista): XX,XX €**

---

### 5.3. Interoperabilidad, Estándares Abiertos y Extensibilidad
Detalla los protocolos, formatos de intercambio de datos y mecanismos de extensibilidad empleados para evitar soluciones propietarias cerradas.
- **Protocolos de comunicación estándar empleados:** *(p. ej., MQTT, CoAP, HTTP/REST, BLE GATT, Matter, Thread, LoRaWAN).*
- **Formatos de serialización de datos:** *(p. ej., JSON, CBOR, Protobuf, SenML).*
- **Especificación de la API / Árbol de Topics MQTT / Servicios BLE:**
  ```json
  // Ejemplo de payload estándar intercambiado por el sistema
  {
    "device_id": "node-01",
    "timestamp": 1763400000,
    "context": {
      "location": [39.4752, -6.3724],
      "event": "geofence_alert"
    }
  }
  ```
- **Extensibilidad:** *(Explica cómo se puede añadir un nuevo sensor, actuador o nodo de otro fabricante al sistema sin tener que rediseñar la arquitectura central).*

---

## ⚠️ Limitaciones del prototipo
- **Limitaciones actuales del prototipo:** ...

---
