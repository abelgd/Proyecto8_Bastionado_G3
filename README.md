# Proyecto 8: Seguridad en conexiones invisibles

## Fundamentación teórica

### Los routers domésticos

Los routers domésticos son un tipo de dispositivo que hay que evitar a toda costa en entornos profesionales. Están pensados para facilitar la conexión, tanto por cable como inalámbrica (sobre todo inalámbrica) a clientes particulares. 

Sin embargo, replican muchas de las medidas de seguridad que podemos aplicar en un entorno empresarial desde una interfaz de gestión bastante simple. Por lo tanto, se pueden realizar muchas pruebas útiles con este tipo de dispositivos. 

Además, son utilizados en un entorno empresarial por muchas **PYMEs** que no tienen un presupuesto demasiado alto y cuyos riesgos no compensan la adquisición de dispositivos más potentes.

Comienza leyendo con atención esta [web sobre seguridad en routers domésticos](https://routersecurity.org/checklist.php). Ofrece información muy completa e interesante sobre los elementos a tener en cuenta al tratar de configurar la mayor seguridad posible. 

Una frase clave que aparece es:

> “El mayor experto del mundo solo puede hacer un router seguro tanto como lo permita su firmware”.

Esto quiere decir que **la elección del dispositivo es crítica**, ya que no todos permiten aplicar todas las medidas necesarias.

---

### Seguridad WiFi en redes empresariales

Cuando tenemos una red WiFi empresarial, normalmente formada por uno o más puntos de acceso (en función del tamaño de la misma y sus requisitos), éstos se configuran desde un **controlador central** que los administra.

En el mercado actualmente existen varias marcas destacadas: **Aruba, Cisco, Ubiquiti**, entre otras.

Una parte del proyecto la vamos a realizar sobre **Ubiquiti**, por los siguientes motivos:

- Permiten probar su software de gestión de forma gratuita.  
- Es el único distribuidor de los mencionados que no tiene cuotas mensuales obligatorias para usar los dispositivos adquiridos.  
- Gracias a su equilibrio entre **calidad y precio**, se está convirtiendo en una de las soluciones más utilizadas en el entorno empresarial.

---

## Objetivos del proyecto

- Configurar medidas de seguridad en un router doméstico.  
- Diseñar y securizar una infraestructura de red inalámbrica empresarial.

---

## Descripción del proyecto

### Parte 1

En [este enlace](https://routersecurity.org/resources.php) puedes encontrar un listado de las páginas web en las que los fabricantes de routers publican sus avisos de seguridad. 

En el siguiente apartado, tienes un listado de **emuladores web de diferentes consolas de gestión de varios dispositivos**. Elige uno de ellos y realiza una de las siguientes opciones:

- Elaborar una **guía de hardening** de ese modelo en el formato que prefieras (PDF, CodeLab, web, Documento de Google, etc).  
- Buscar una **guía de seguridad** de ese modelo previamente realizada y hacer un **anexo crítico** en el que:
  - Cuestiones alguna de las medidas propuestas, o  
  - Añadas otras nuevas.  

De nuevo, eres libre de elegir el formato.

---

### Parte 2

1. [Crea una cuenta](https://account.ui.com/) en **Ubiquiti**.  
2. [Descarga](https://ui.com/download) e **instala el software de UniFi Controller**.  

Este es el mismo software que se usa para gestionar este tipo de redes. Normalmente:
- Se instala en un **servidor**, o  
- Se adquiere un dispositivo **CloudKey**, que viene con el software preinstalado y facilita el acceso remoto al mismo.

---

### Diseño de la infraestructura WiFi

Comenzaremos diseñando y creando la **infraestructura física** de nuestra red WiFi. Esto lo consensuaremos en equipo, decidiendo cómo lo haríamos en una empresa real. 

Para ello debemos definir:

- Cuántos **APs** (Access Points) vamos a necesitar.  
- **Dónde** los vamos a colocar.

Esto se puede hacer desde la web [design.ui.com](https://design.ui.com/).

En esta página se puede:
- **Simular físicamente** una red.  
- Elaborar automáticamente el **presupuesto del material necesario** para la instalación.

**Limitación:** no permite definir la configuración de los puntos de acceso para delimitar su potencia y ver cómo influye en el mapa de calor de la cobertura.  

Sin embargo, podemos **asumir posteriormente** que se ajustará la potencia de cada AP para que la señal **no escape de las paredes** del área asignada, considerando el **material de dichas paredes**.

---

### Entregables

- Elaborar una **propuesta de instalación** en un plano a elección del grupo.  
- Exportar los **mapas de calor** de las coberturas de **2.4 GHz** y **5 GHz**.

---

### Aseguramiento de la instalación WiFi UniFi

Para finalizar el proyecto, se realizará un estudio sobre **cómo asegurar al máximo una instalación WiFi de UniFi**.  

El resultado se reflejará en un **repositorio grupal de GitHub**, donde se publicarán las guías de configuración.

**Indicaciones:**
- Cada integrante elaborará **al menos una guía**.  
- Las guías se crearán con la extensión de Chrome [Tango](https://www.tango.us/).  
- Después se enlazarán en el repositorio de forma ordenada.  
- No se deben incluir configuraciones que requieran **acceso directo a los parámetros de un punto de acceso concreto**.

---

## Recursos de interés

- [Router Security Checklist](https://routersecurity.org/checklist.php)  
- [Router Security Resources](https://routersecurity.org/resources.php)  
- [Ubiquiti Account](https://account.ui.com/)  
- [Ubiquiti Downloads](https://ui.com/download)  
- [Ubiquiti Network Designer (design.ui.com)](https://design.ui.com/)  
- [Tango — Chrome Extension](https://www.tango.us/)

---
