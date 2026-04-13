# Informe de Infraestructura de Red WiFi Corporativa

## 1. Introducción

La red inalámbrica corporativa se ha diseñado sobre el ecosistema UniFi de Ubiquiti, con 9 puntos de acceso U6 Pro gestionados centralizadamente. El objetivo es garantizar cobertura completa, sin interferencias y con alta disponibilidad en todas las zonas del edificio.

---

## 2. Equipamiento

### Dream Router 7 (DR-7) — Núcleo de gestión

1. Actúa como router, firewall
2. Elimina la necesidad de servidor dedicado para la gestión de la red.

### Switch Pro Max 24 PoE — Distribución

24 puertos PoE que alimentan eléctricamente todos los APs a través del propio cable de red, sin fuentes de alimentación adicionales. Desde aquí parten todos los enlaces al edificio.

### 9× UniFi U6 Pro — Puntos de acceso

WiFi 6 (802.11ax), doble banda (2,4 / 5 GHz).

## 3. Cableado

Desde el Switch situado en el Rack pasamos el cableados por las paredes hasta llegar a los AP.

---

## 4. Gestión de Interferencias y Potencia

### Ajuste de potencia por AP

Cada U6 Pro se configura para que la cobertura quede contenida en su propia estancia.

---

## 5. Cobertura Conseguida

El mapa de calor generado con UniFi Design Center muestra cobertura óptima:

### Mapa de Calor 2.4GHz:
![img](img/2.4_ghz_mapadecalor.png)

### Mapa de Calor 5GHz:
![img](img/5_ghz_mapadecalor.png)

---

## 6. Conclusión

Con nuestra infraestructura realizada: DR-7 (Router) + Switch 24 PoE + 9× U6 Pro (Acces Points), proporciona cobertura WiFi completa y gestionada centralizadamente. La clave del rendimiento óptimo reside en el ajuste correcto de la potencia de cada AP para que no se solapen y salgan de su estancia fijada y la planificación manual de canales, evitando interferencias y garantizando conectividad estable en todo el edificio.