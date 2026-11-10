# Case #NET-01: Core Router and WAN Link Troubleshooting

* **Incident ID:** NET17933846094810[cite: 4]
* **Severity:** Critical (Total corporate connectivity outage / No access to email or SaaS)[cite: 4]
* **Reported by:** Victoria Hayes | Legal Department[cite: 4]

## 1. Diagnosis & Inspection (OSI Model)
* **Layers 1 & 2 (Physical & Local Link):** Local workstation issues and access switches are ruled out, as they are operational and `ONLINE`[cite: 7].
* **Layers 3 & 4 (Network, Transport & WAN):** Server room monitoring reveals that the primary router (**Core Router - 10.0.0.1**) is down (Error) and the external link (**Metro ISP**) is degraded[cite: 7].

## 2. Corrective Action & Resolution
1. A power cycle / service restart is executed on the Core Router (`10.0.0.1`)[cite: 7].
2. Verification of the restoration of routing tables and external provider connectivity.

## 3. Validation & Closure
* Network stability and normal browsing are confirmed via corporate chat with the user.
* The ticket is closed in the ITSM system meeting SLA metrics[cite: 3, 4].
