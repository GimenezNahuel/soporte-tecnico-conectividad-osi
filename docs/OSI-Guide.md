# Metodología de Troubleshooting de Conectividad basada en el Modelo OSI

Esta guía define el procedimiento operativo estándar (SOP) para el diagnóstico, aislamiento y resolución de incidentes de red en soporte técnico IT. Se aplica un enfoque **Bottom-Up** (desde la Capa 1 hacia las capas superiores), lo que permite validar de forma metódica la infraestructura física antes de escalar hacia fallas de configuración lógicas o aplicaciones.

---

## 1. Capa 1: Física (Medio de Transmisión y Hardware)
* **Objetivo:** Confirmar la integridad del hardware, los cables y la recepción de señal eléctrica u óptica.
* **Puntos de Verificación:**
  * Inspección física de cables UTP/FTP (conectores RJ45 dañados, dobleces excesivos).
  * Verificación de niveles de potencia óptica en enlaces FTTH (Rx/Tx) o niveles de señal RF en conexiones coaxial/HFC.
  * Estado de los LEDs del módem/ONT/Switch: Power, PON/LOS, Link/ACT de los puertos Ethernet.

## 2. Capa 2: Enlace de Datos (Sincronismo y Conmutación L2)
* **Objetivo:** Garantizar la comunicación directa entre interfaces adyacentes y el estado del enlace local.
* **Puntos de Verificación:**
  * Sincronismo del módem

  ## 3. Capa 3: Red (Direccionamiento IP y Enrutamiento)
* **Objetivo:** Comprobar la asignación lógica de IP y la capacidad de enviar paquetes dentro y fuera de la red local.
* **Puntos de Verificación:**
  * Asignación de dirección IP (validación de servidor DHCP vs. dirección APIPA `169.254.x.x`).
  * Prueba de conectividad local a la puerta de enlace predeterminada (`ping <Gateway_IP>`).
  * Verificación de tabla de ruteo local y salida a IP pública externa (`ping 8.8.8.8`).

## 4. Capa 4: Transporte (Pérdida de Paquetes, Latencia y Puertos)
* **Objetivo:** Analizar la calidad de la sesión de comunicación extremo a extremo y la accesibilidad de puertos.
* **Puntos de Verificación:**
  * Traza de ruta (`traceroute` / `tracert`) para identificar saltos con latencia alta o pérdida de paquetes.
  * Evaluación de enlaces WAN del ISP (identificación de degradaciones o saturación externa).
  * Verificación de puertos de servicio TCP/UDP mediante herramientas de terminal (`telnet`, `nc`, `Test-NetConnection`).

## 5. Capas 5, 6 y 7: Sesión, Presentación y Aplicación (Servicios Finales)
* **Objetivo:** Confirmar el funcionamiento correcto de los servicios y aplicaciones consumidos por el usuario final.
* **Puntos de Verificación:**
  * Resolución de nombres mediante DNS (`nslookup`, `dig`) y depuración de caché DNS local (`ipconfig /flushdns`).
  * Validación de protocolos de aplicación (HTTP/HTTPS, peticiones GET/POST en navegadores web).
  * Diagnóstico de servicios específicos como registros SIP/VoIP, clientes VPN (IKEv2/IPSec) o conectividad SaaS.
