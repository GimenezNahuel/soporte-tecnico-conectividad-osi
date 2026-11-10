# Case #NET-02: Wi-Fi Drops and Intermittency Due to WAN Link Degradation

* **Incident ID:** NET17942563635270[cite: 4, 5]
* **Severity:** Critical (Recurrent drops in corporate video calls)[cite: 4, 5]
* **Reported by:** Rachel Green | Sales Department[cite: 4, 5]

## 1. Diagnosis & Inspection (OSI Model)
* **Layers 1 & 2 (Physical & Local Link / Wi-Fi):** Local infrastructure status is verified. Access switches (`Floor 1`, `Floor 2`, `Floor 3`) and Core Router are stable and `ONLINE`, ruling out local AP issues[cite: 5].
* **Layers 3 & 4 (Network, Transport & Provider):** It is identified that the **Metro ISP (External)** service is `DEGRADED` with external packet loss[cite: 6, 7]. Transport layer drops were disrupting video conferencing application sessions, creating a false symptom of "Wi-Fi failure"[cite: 4, 5].

## 2. Corrective Action & Resolution
1. A proactive notification is posted in the company channel (`Company GC`) informing about the external provider outage[cite: 7].
2. Technical monitoring is performed until the ISP fully normalizes the service (`NO CURRENT INTERRUPTIONS`).

## 3. Validation & Closure
* The user (`Rachel Green`) is contacted to validate that the connection and calls are running smoothly.
* Resolution notes are logged into the ticketing system and the case is closed under SLA metrics[cite: 3, 4].
