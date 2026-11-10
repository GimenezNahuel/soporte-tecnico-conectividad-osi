# Caso #NET-02: Microcortes e Intermitencia Wi-Fi por Degradación en Enlace WAN

* **ID de Incidente:** NET17942563635270[cite: 4, 5]
* **Severidad:** Crítico (Cortes recurrentes en videollamadas corporativas)[cite: 4, 5]
* **Reportado por:** Rachel Green | Departamento de Ventas[cite: 4, 5]

## 1. Diagnóstico e Inspección (Modelo OSI)
* **Capas 1 y 2 (Física y Enlace Local / Wi-Fi):** Se verifica el estado de la infraestructura local. Los switches de acceso (`Floor 1`, `Floor 2`, `Floor 3`) y el Core Router se encuentran estables y `EN LÍNEA`, descartando fallas en el AP local[cite: 5].
* **Capas 3 y 4 (Red, Transporte y Proveedor):** Se identifica que el servicio **Metro ISP (External)** se encuentra en estado `DEGRADADO` con intermitencia exterior[cite: 6, 7]. La pérdida de paquetes en el transporte afectaba las sesiones de la aplicación de videollamada, generando el falso síntoma de "falla de Wi-Fi"[cite: 4, 5].

## 2. Acción Correctiva y Resolución
1. Se emite una notificación proactiva en el canal de la empresa (`Company GC`) informando la afectación del proveedor exterior[cite: 7].
2. Se realiza monitoreo técnico hasta que el ISP normaliza el servicio por completo (`SIN INTERRUPCIONES ACTUALES`).

## 3. Validación y Cierre
* Se contacta a la usuaria (`Rachel Green`) para validar que la conexión y las llamadas operan de forma estable.
* Se registran las notas de resolución en la ticketera y se cierra el caso bajo métricas de SLA[cite: 3, 4].
