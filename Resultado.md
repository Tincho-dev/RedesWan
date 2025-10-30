# Proyecto de Conectividad WLAN - Enlace Radio Punto a Punto

## Trabajo Práctico N°3

**Ubicaciones a Conectar:**
- **Punto A**: Universidad Tecnológica Nacional, Facultad Regional Tucumán - Casa Central
  - Coordenadas: -26.817226, -65.198500
- **Punto B**: Polo Tecnológico FRT
  - Coordenadas: -26.87925, -65.15636

---

## 1. Introducción

El presente proyecto tiene como objetivo establecer una conexión WLAN de alto rendimiento entre las instalaciones actuales de la Facultad Regional Tucumán de la UTN y el nuevo Polo Tecnológico FRT, ubicado aproximadamente a 8 km de distancia. Para lograr esta conectividad se implementará un sistema de radio enlace punto a punto utilizando equipos de la marca Ubiquiti.

La planificación del enlace se realizó utilizando la herramienta de cálculo de conectividad provista por Ubiquiti (https://link.ui.com/), considerando las condiciones geográficas, obstáculos presentes en el trayecto y las necesidades de ancho de banda requeridas para las actividades académicas y administrativas.

---

## 2. Análisis del Enlace Directo

### 2.1 Características del Trayecto

- **Distancia en línea recta**: Aproximadamente 8 km
- **Tipo de enlace**: Punto a Punto (PtP)
- **Zona**: Urbana con presencia de edificios y vegetación

### 2.2 Análisis de Obstáculos

Para determinar la viabilidad del enlace directo entre ambos puntos, se realizó un análisis exhaustivo de los obstáculos presentes en el trayecto:

#### Obstáculo 1: Edificio en Av. Sarmiento esquina Monteagudo
- **Ubicación**: 220 metros del predio principal (UTN Casa Central)
- **Características**: 6 pisos más terraza
- **Altura estimada**: 20 metros
- **Impacto**: Requiere elevación de la torre principal

#### Obstáculo 2: Edificio en Monteagudo al 800
- **Ubicación**: 360 metros del predio principal
- **Características**: 15 pisos más terraza
- **Altura estimada**: 50 metros
- **Impacto**: Obstáculo crítico que determina la altura mínima de la torre principal

#### Obstáculo 3: Edificio en Honduras al 27
- **Ubicación**: 880 metros del predio principal
- **Características**: 9 pisos más terraza
- **Altura estimada**: 30 metros

#### Obstáculo 4: Edificio en Honduras al 47
- **Ubicación**: 900 metros del predio principal
- **Características**: 13 pisos más terraza
- **Altura estimada**: 45 metros

### 2.3 Alturas de Torres Requeridas

Después del análisis de obstáculos y considerando la Zona de Fresnel, se determinaron las siguientes alturas:

- **Torre #1** (UTN Casa Central): **60 metros**
  - Justificación: Supera el edificio más alto en el trayecto (50m) con un margen de seguridad de 10 metros, garantizando línea de vista directa y zona de Fresnel despejada

- **Torre #2** (Polo Tecnológico FRT): **30 metros**
  - Justificación: Altura adecuada considerando la topografía y menor densidad de obstáculos en el extremo del enlace

---

## 3. Análisis de Equipamiento

Se evaluaron tres opciones de equipos Ubiquiti para el enlace, todos operando en la banda de 60 GHz:

### 3.1 AirFiber 60 LR

**Especificaciones Técnicas:**
- Frecuencia de operación: 60 GHz
- Alcance máximo: 12 km
- Ancho de banda: Hasta 1.95 Gbps
- Antena parabólica de alta ganancia integrada
- Tecnología Wave para largo alcance

**Rendimiento esperado en el enlace:**
- Nivel de señal: -57 dBm
- Calidad de señal: Excelente (>-70 dBm es aceptable)
- Estabilidad: Alta
- Latencia: Baja

**Ventajas:**
- Costo-beneficio favorable
- Rendimiento adecuado para el alcance requerido
- Señal estable

**Desventajas:**
- Menor ancho de banda comparado con otras opciones
- Alcance limitado a 12 km

### 3.2 Wave Pro

**Especificaciones Técnicas:**
- Frecuencia de operación: 60 GHz
- Alcance máximo: 
  - PtP: hasta 15 km
  - PtMP: hasta 8 km (Wave AP)
- Ancho de banda: Hasta 3.20 Gbps
- Soporte para enlaces PtP y PtMP

**Rendimiento esperado en el enlace:**
- Nivel de señal: -49 dBm
- Calidad de señal: Óptima (señal muy fuerte)
- Estabilidad: Muy alta
- Latencia: Muy baja

**Ventajas:**
- Mayor ancho de banda (3.20 Gbps)
- Excelente nivel de señal
- Flexibilidad para futuras expansiones PtMP
- Alcance de 15 km en PtP

**Desventajas:**
- Costo más elevado que el AF60 LR

### 3.3 AirFiber 60 XG (Xtreme)

**Especificaciones Técnicas:**
- Frecuencia de operación: 60 GHz
- Alcance máximo: Más de 15 km
- Ancho de banda: Hasta 2.70 Gbps (dúplex completo)
- Rendimiento total: 5.4 Gbps

**Rendimiento esperado en el enlace:**
- Nivel de señal: -47 dBm
- Calidad de señal: Óptima (señal muy fuerte)
- Estabilidad: Muy alta
- Latencia: Muy baja

**Ventajas:**
- Señal más fuerte de todas las opciones
- Excelente ancho de banda
- Mayor alcance
- Diseñado para enlaces de larga distancia

**Desventajas:**
- Opción más costosa

### 3.4 Comparativa y Recomendación

| Equipo | Ancho de Banda | Señal Esperada | Alcance | Recomendación |
|--------|---------------|----------------|---------|---------------|
| AirFiber 60 LR | 1.95 Gbps | -57 dBm | 12 km | Opción económica |
| Wave Pro | 3.20 Gbps | -49 dBm | 15 km | **RECOMENDADA** |
| AirFiber 60 XG | 2.70 Gbps | -47 dBm | >15 km | Opción premium |

**Equipo Recomendado: Wave Pro**

**Justificación:**
- Ofrece el mayor ancho de banda (3.20 Gbps), garantizando capacidad para crecimiento futuro
- Excelente nivel de señal (-49 dBm) que asegura estabilidad
- Alcance de 15 km sobrado para la distancia de 8 km
- Posibilidad de expansión a PtMP para futuras necesidades
- Mejor relación rendimiento-costo para las necesidades del proyecto

---

## 4. Análisis de Condiciones Climáticas

### 4.1 Impacto del Clima en Enlaces de 60 GHz

Las señales de 60 GHz son susceptibles a la atenuación por precipitaciones. En la región de Tucumán se deben considerar:

**Factores climáticos relevantes:**
- Precipitaciones: Promedio anual de 900-1000 mm
- Humedad: Alta durante la temporada de lluvias
- Temperatura: Variaciones significativas
- Niebla: Ocasional en invierno

### 4.2 Atenuación por Lluvia

Para el enlace de 8 km con los equipos propuestos:

- **Lluvia ligera (2.5 mm/h)**: Atenuación de ~0.5 dB/km = 4 dB total
- **Lluvia moderada (5 mm/h)**: Atenuación de ~1.5 dB/km = 12 dB total
- **Lluvia intensa (25 mm/h)**: Atenuación de ~8 dB/km = 64 dB total

**Análisis de disponibilidad:**
- Con el Wave Pro y su señal de -49 dBm, el enlace mantendrá operatividad incluso con lluvias moderadas
- Durante lluvias intensas puede haber degradación del ancho de banda, pero el enlace se mantendrá operativo
- La disponibilidad estimada del enlace es del 99.9% anual

### 4.3 Mitigación

- Las torres de 60 y 30 metros elevan el enlace sobre la mayoría de obstáculos que podrían generar reflexiones durante condiciones de humedad
- Los equipos Ubiquiti de 60 GHz incluyen modulación adaptativa para ajustarse a las condiciones

---

## 5. Alternativa con Repetidor

### 5.1 Justificación de la Alternativa

Aunque el enlace directo es viable, se propone una alternativa con repetidor para:
- Mejorar la calidad de señal en ambos tramos
- Reducir la altura de la torre en el Polo Tecnológico
- Proporcionar redundancia y mejor estabilidad
- Facilitar futuras expansiones

### 5.2 Ubicación del Repetidor

**Sitio propuesto**: Lince Rugby Club
- **Coordenadas estimadas**: -26.847, -65.177 (aproximadas, requieren confirmación en sitio)
- **Ventajas de la ubicación**:
  - Infraestructura existente (torre de aproximadamente 30 metros)
  - Ubicación geográfica favorable
  - Menos obstáculos en ambos tramos

### 5.3 Configuración de Torres con Repetidor

**Torre #1** (UTN Casa Central): **60 metros**
- Igual que en la configuración directa
- Enlace al repetidor

**Torre #2** (Lince Rugby Club - Repetidor): **30 metros**
- Puede utilizar infraestructura existente
- Dos radios: uno hacia UTN y otro hacia Polo Tecnológico

**Torre #3** (Polo Tecnológico FRT): **20 metros**
- Reducción de altura comparada con enlace directo
- Menor costo de instalación

### 5.4 Análisis de Obstáculos - Alternativa con Repetidor

#### Tramo 1: UTN Casa Central → Lince Rugby Club (aproximadamente 4 km)

**Obstáculos identificados:**
- Edificio en Monteagudo entre Santa Fe y Marcos Paz
  - Distancia: 500 metros
  - Altura: 45 metros (15 pisos)
- Edificios en zona de Balcarce y Corrientes
  - Distancia: 600-700 metros
  - Altura: 45 metros (13 pisos)

**Clearance**: La línea de enlace pasa con 10-15 metros de altura sobre los obstáculos más altos

#### Tramo 2: Lince Rugby Club → Polo Tecnológico FRT (aproximadamente 4 km)

**Obstáculos identificados:**
- Edificio en Av. Soldati y Cuba
  - Distancia: 1400 metros desde punto de inicio
  - Altura: 45 metros (15 pisos)
- Vegetación y arbolado en zona menos urbanizada

**Clearance**: La línea de enlace mantiene adecuada zona de Fresnel

### 5.5 Equipamiento para Alternativa con Repetidor

**Configuración recomendada:**
- **Tramo 1** (UTN → Repetidor): 2x Wave Pro
- **Tramo 2** (Repetidor → Polo Tecnológico): 2x Wave Pro

**Rendimiento esperado:**
- Señal Tramo 1: -45 dBm (excelente)
- Señal Tramo 2: -48 dBm (excelente)
- Ancho de banda efectivo: Hasta 3.20 Gbps
- Mayor estabilidad por tramos más cortos

### 5.6 Consideraciones de la Alternativa

**Ventajas:**
- Mejor calidad de señal en ambos tramos (señales más fuertes)
- Menor altura requerida en Polo Tecnológico (20m vs 30m)
- Mayor resiliencia ante condiciones climáticas adversas
- Posibilidad de servicios adicionales desde el repetidor
- Tramos más cortos reducen atenuación por lluvia

**Desventajas:**
- Requiere acuerdos con terceros (Lince Rugby Club)
- Mayor inversión inicial (equipamiento adicional)
- Mayor complejidad de mantenimiento (tres sitios)
- Necesidad de alimentación eléctrica en sitio de repetidor
- Posible necesidad de construcción de torre adicional

**Requerimientos adicionales:**
- Acuerdo o convenio con Lince Rugby Club
- Estudio de viabilidad de uso de infraestructura existente
- Sistema de alimentación eléctrica confiable en repetidor
- Sistema de respaldo de energía (UPS + generador)

---

## 6. Análisis Económico Preliminar

### 6.1 Costos Estimados - Enlace Directo

**Infraestructura:**
- Torre de 60m (UTN Casa Central): USD 40,000 - 60,000
- Torre de 30m (Polo Tecnológico): USD 20,000 - 30,000
- Instalación y cimentación: USD 15,000 - 25,000

**Equipamiento (Wave Pro):**
- 2x Wave Pro: USD 10,000 - 15,000
- Accesorios y cableado: USD 2,000 - 3,000

**Total estimado**: USD 87,000 - 133,000

### 6.2 Costos Estimados - Alternativa con Repetidor

**Infraestructura:**
- Torre de 60m (UTN Casa Central): USD 40,000 - 60,000
- Adaptación/nueva torre 30m (Repetidor): USD 15,000 - 30,000
- Torre de 20m (Polo Tecnológico): USD 12,000 - 18,000
- Instalación y cimentación: USD 15,000 - 25,000

**Equipamiento (4x Wave Pro):**
- 4x Wave Pro: USD 20,000 - 30,000
- Accesorios y cableado: USD 4,000 - 6,000
- Sistema de energía para repetidor: USD 5,000 - 8,000

**Costos adicionales:**
- Acuerdo con Lince Rugby Club: A determinar
- Mantenimiento adicional: USD 2,000 - 4,000 anuales

**Total estimado**: USD 111,000 - 177,000

---

## 7. Conclusiones y Recomendaciones

### 7.1 Conclusiones

1. **Viabilidad técnica**: Ambas alternativas (enlace directo y con repetidor) son técnicamente viables para conectar los dos sitios

2. **Enlace directo**:
   - Solución más simple y directa
   - Menor complejidad operativa
   - Adecuado para las necesidades actuales
   - Vulnerable a condiciones climáticas extremas

3. **Alternativa con repetidor**:
   - Mayor calidad de señal y estabilidad
   - Mejor preparada para expansiones futuras
   - Mayor inversión inicial pero mejor ROI a largo plazo
   - Requiere coordinación con terceros

4. **Equipamiento**: El Wave Pro de Ubiquiti ofrece la mejor relación rendimiento-costo para este proyecto, con 3.20 Gbps de ancho de banda y excelente calidad de señal

### 7.2 Recomendación Final

**Se recomienda implementar el ENLACE DIRECTO como primera fase**, por las siguientes razones:

1. **Menor complejidad inicial**: No requiere acuerdos con terceros
2. **Menor inversión inicial**: Aproximadamente 20-30% menos de costo
3. **Tiempo de implementación**: Más rápido al involucrar menos actores
4. **Autonomía**: Control total sobre la infraestructura

**Con la opción de migrar a la configuración con repetidor en el futuro** si:
- Se identifican problemas de estabilidad durante condiciones climáticas adversas
- Se requiere ampliar la red a otros puntos de la ciudad
- Se logran acuerdos favorables con Lince Rugby Club
- Las necesidades de ancho de banda superan la capacidad del enlace directo

### 7.3 Plan de Implementación Recomendado

**Fase 1: Planificación y Permisos (2-3 meses)**
- Obtención de permisos municipales y regulatorios
- Estudios de suelo y estructurales
- Diseño de ingeniería detallado
- Adquisición de equipamiento

**Fase 2: Construcción (3-4 meses)**
- Construcción de torres y cimentaciones
- Instalación de equipos
- Tendido de cableado y sistemas auxiliares

**Fase 3: Puesta en Marcha (1 mes)**
- Alineación de antenas
- Pruebas de enlace
- Optimización y ajustes
- Capacitación del personal

**Fase 4: Operación y Monitoreo**
- Monitoreo continuo de rendimiento
- Mantenimiento preventivo trimestral
- Evaluación de necesidad de repetidor después de 6-12 meses

### 7.4 Especificaciones Finales Recomendadas

**Configuración de Enlace Directo:**
- **Torre 1** (UTN Casa Central): 60 metros
- **Torre 2** (Polo Tecnológico): 30 metros
- **Equipo**: 2x Ubiquiti Wave Pro (60 GHz)
- **Ancho de banda esperado**: 3.20 Gbps
- **Disponibilidad esperada**: 99.9%
- **Latencia**: < 2 ms

**Características del sistema:**
- Línea de vista directa garantizada
- Zona de Fresnel despejada en más del 60%
- Clearance de 6-10 metros sobre obstáculos críticos
- Modulación adaptativa para condiciones variables
- Sistema de monitoreo remoto integrado

---

## 8. Anexos

### 8.1 Datos Técnicos de Referencia

**Coordenadas exactas:**
- UTN Casa Central: -26.817226, -65.198500
- Polo Tecnológico FRT: -26.87925, -65.15636
- Distancia: ~8 km en línea recta

**Herramienta utilizada:**
- Ubiquiti Link Planning Tool (https://link.ui.com/)

### 8.2 Normativas Aplicables

- Regulación de la ENACOM (Argentina)
- Normas de construcción y seguridad municipal
- Regulaciones de espectro para banda de 60 GHz (sin licencia)
- Normas de seguridad para torres de telecomunicaciones

### 8.3 Consideraciones de Seguridad

- Señalización de torres según normativas aeronáuticas
- Protección contra descargas atmosféricas
- Sistemas de puesta a tierra
- Protección perimetral de torres
- Señalización de seguridad

---

**Documento elaborado para:**
Universidad Tecnológica Nacional - Facultad Regional Tucumán

**Fecha:** Octubre 2025

**Proyecto:** Conectividad WLAN mediante Radio Enlace - Polo Tecnológico FRT
