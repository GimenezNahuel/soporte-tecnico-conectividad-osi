# Case #NET-03: VPN Connectivity Troubleshooting & DNS Cache Flushing

* **Incident ID:** NET17933846326061
* **Severity:** High (Inability to access internal corporate resources)
* **Reported by:** Ivana Petrova | Engineering Department (Remote)

## 1. Diagnosis & Inspection (OSI Model)
* **Layers 1 to 3 (Physical, Data Link & Network):** Internet connectivity is fully operational on the remote workstation.
* **Layers 5 to 7 (Session, Application / DNS & VPN):** When attempting to bring up the corporate VPN tunnel (IKEv2/IPSec), the client fails to connect because stale or corrupted DNS entries (`vpn.corp.local`) are blocking the tunnel routing.

## 2. Corrective Action & Resolution
1. Remote support session is established on the user's workstation.
2. The local DNS resolver cache is cleared via the system terminal by executing:
   `ipconfig /flushdns`
3. The VPN client connection is re-attempted, verifying proper tunnel establishment and access to internal shares.

## 3. Validation & Closure
* Connectivity and access to services hosted on the corporate network are successfully verified.
* Resolution notes are logged into the ticketing system and the incident is closed.
