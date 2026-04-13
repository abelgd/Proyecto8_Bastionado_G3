# Informe de Infraestructura de Red WiFi Corporativa

## 1. Introducción

La red inalámbrica corporativa se ha diseñado sobre el ecosistema UniFi de Ubiquiti, con 9 puntos de acceso U6 Pro gestionados centralizadamente. El objetivo es garantizar cobertura completa, sin interferencias y con alta disponibilidad en todas las zonas del edificio.

---

## 2. Equipamiento

### Dream Router 7 (DR-7) — Núcleo de gestión

Actúa como router, firewall, controlador UniFi embebido e IDS/IPS en un único dispositivo. Elimina la necesidad de servidor dedicado para la gestión de la red.

### Switch Pro Max 24 PoE — Distribución

24 puertos PoE que alimentan eléctricamente todos los APs a través del propio cable de red, sin fuentes de alimentación adicionales. Desde aquí parten todos los enlaces al edificio.

### 9× UniFi U6 Pro — Puntos de acceso

WiFi 6 (802.11ax), doble banda (2,4 / 5 GHz), MIMO 4×4 en 5 GHz. Características clave:

- Alto rendimiento en entornos con muchos dispositivos simultáneos
- Alimentación PoE, sin adaptadores independientes
- Gestión centralizada desde el controlador del DR-7

### Ubicación de los puntos de acceso

| AP | Ubicación |
|----|-----------|
| U6 Pro 1 | Zona central del edificio |
| U6 Pro 2 | Zona derecha, planta principal |
| U6 Pro 3 | Zona superior central |
| U6 Pro 4 | Zona superior derecha central |
| U6 Pro 5 | Zona central inferior |
| U6 Pro 6 | Zona superior izquierda |
| U6 Pro 7 | Zona inferior derecha |
| U6 Pro 8 | Zona superior extremo derecho |
| U6 Pro 9 | Zona izquierda central |

---

## 3. Cableado

Topología en estrella con cable Cat6 empotrado desde el rack central hasta cada AP. El backhaul cableado garantiza inmunidad a interferencias RF y aprovisionamiento eléctrico PoE sin instalación eléctrica adicional.

---

## 4. Gestión de Interferencias y Potencia

### Ajuste de potencia por AP

Cada U6 Pro se configura con TX Power manual para que la cobertura quede contenida en su propia estancia. Ruta en el controlador:

`Configuración del AP → Radio → TX Power → Manual`

Se ajusta iterativamente midiendo RSSI real hasta encontrar el equilibrio óptimo.

### Planificación de canales

- **2,4 GHz:** canales 1, 6 y 11 (únicos no solapados)
- **5 GHz:** mayor disponibilidad de canales; planificación manual recomendada

### BSS Coloring (WiFi 6)

Permite que APs vecinos identifiquen su propia red y reduzcan colisiones, mejorando la eficiencia espectral sin necesidad de mayor separación física.

---

## 5. Cobertura Estimada

El mapa de calor generado con UniFi Design Center muestra cobertura óptima (≥ −65 dBm) en la práctica totalidad del interior en ambas bandas. La señal decrece en el exterior, lo que es deseable por seguridad perimetral.

---

## 6. Ventajas de la Solución

| Característica | Beneficio |
|---|---|
| Gestión centralizada (UniFi) | Administración unificada de todos los APs desde un único panel |
| Cableado PoE estructurado | Sin fuentes independientes; instalación limpia y fiable |
| WiFi 6 (802.11ax) | Mayor velocidad, menor latencia, mejor rendimiento con alta densidad |
| Un AP por estancia | Cobertura focalizada sin solapamientos |
| TX Power ajustable por AP | Eliminación de interferencias entre APs vecinos |
| Arquitectura UniFi | Escalable: nuevos APs o switches sin cambiar el núcleo |

---

## 7. Conclusión

La solución DR-7 + Switch 24 PoE + 9× U6 Pro proporciona cobertura WiFi 6 completa y gestionada centralizadamente. La clave del rendimiento óptimo reside en el ajuste correcto de TX Power por AP y la planificación manual de canales, evitando interferencias y garantizando conectividad estable en todo el edificio.