# Soporte técnico a conectividad en base al modelo OSI

Este repositorio documenta una metodología estructurada de *troubleshooting* (enfoque *Bottom-Up*) para la resolución de incidentes de redes y telecomunicaciones, aplicando el modelo OSI como estándar técnico para el aislamiento y diagnóstico de fallas.

## Estructura del Repositorio

* **[Guía de Diagnóstico OSI](docs/OSI-Guide.md):** Procedimiento operativo estándar (SOP) para la verificación metódica capa por capa (Capa 1 a Capa 7).
* **Casos de Estudio (Incidentes Reales):**
  * **[Caso #NET-01 (Caída de Core Router y WAN)](cases/case-01-core-router.md):** Resolución de un incidente crítico de afectación corporativa masiva mediante el aislamiento en capas de red y transporte.
  * **[Caso #NET-02 (Microcortes Wi-Fi / Degradación ISP)](cases/case-02-wifi-drops.md):** Diagnóstico diferencial para descartar fallas de red local frente a problemas de transporte en enlaces exteriores.
  * **[Caso #NET-03 (Troubleshooting VPN y Caché DNS)](cases/case-03-vpn-dns.md):** Resolución de fallas de resolución de nombres y reestablecimiento de túneles remotos a nivel de capas superiores.

---
*Dual-language documentation available: [English Version](README.en.md)*
