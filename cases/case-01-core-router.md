# Caso #NET-01: Resolución de Falla en Core Router y Enlace WAN

* **ID de Incidente:** NET17933846094810[cite: 4]
* **Severidad:** Crítico (Afectación total de conectividad corporativa / Sin acceso a correo ni SaaS)[cite: 4]
* **Reportado por:** Victoria Hayes | Departamento Legal[cite: 4]

## 1. Diagnóstico e Inspección (Modelo OSI)
* **Capas 1 y 2 (Física y Enlace Local):** Se descarta una falla local en los puestos de trabajo o switches de acceso, ya que se encuentran operativos y `EN LÍNEA`[cite: 7].
* **Capas 3 y 4 (Red, Transporte y WAN):** Desde la sala de servidores se detecta que el enrutador principal (**Core Router - 10.0.0.1**) presenta un error de estado (Caído) y el enlace exterior (**Metro ISP**) se encuentra degradado[cite: 7].

## 2. Acción Correctiva y Resolución
1. Se aplica un ciclo de energía (reinicio físico/lógico) sobre el Core Router (`10.0.0.1`)[cite: 7].
2. Se valida el restablecimiento de las tablas de enrutamiento y la conectividad general del proveedor externo.

## 3. Validación y Cierre
* Se confirma mediante chat corporativo con la usuaria la estabilidad de la red y la navegación normal.
* Se procede al cierre del ticket en el sistema ITSM cumpliendo con las métricas de SLA[cite: 3, 4].
