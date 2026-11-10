# Caso #NET-03: Troubleshooting de Conectividad VPN y Resolución de Nombres (DNS)

* **ID de Incidente:** NET17933846326061
* **Severidad:** Alto (Imposibilidad de acceder a recursos internos corporativos)
* **Reportado por:** Ivana Petrova | Departamento de Ingeniería (Remoto)

## 1. Diagnóstico e Inspección (Modelo OSI)
* **Capas 1 a 3 (Física, Enlace y Red Local):** Conectividad a internet operativa en el equipo remoto.
* **Capas 5 a 7 (Sesión y Aplicación / DNS & VPN):** Al intentar levantar el túnel VPN corporativo (IKEv2/IPSec), el cliente arroja error de conexión debido a entradas DNS obsoletas o corruptas (`vpn.corp.local`) que bloquean la resolución del túnel.

## 2. Acción Correctiva y Resolución
1. Se realiza soporte remoto a la estación de trabajo asignada.
2. Se ejecuta la depuración y limpieza de la caché de resolución de nombres en la terminal del sistema ejecutando:
   `ipconfig /flushdns`
3. Se reintenta la conexión del cliente VPN, validando el correcto establecimiento del túnel y el acceso a los recursos internos.

## 3. Validación y Cierre
* Se comprueba la navegación y el acceso a los servicios alojados en la red corporativa.
* Se registran las notas técnicas en la ticketera y se cierra el incidente.
