#  How a Firewall Filters Traffic

A **firewall** is a security system that monitors and controls incoming and outgoing network traffic based on predefined rules. It acts like a security guard that decides whether data packets should be allowed in or out of a computer or network.

---

##  Basic Working of a Firewall

### 1. Packet Inspection

When data (in the form of packets) tries to enter or leave a system, the firewall inspects it.

### 2. Rule Matching

The firewall checks if the packet matches any existing **allow** or **block** rules:

*  If it matches an **allow rule**, the packet is permitted.
*  If it matches a **block rule**, the packet is dropped.
*  If it doesn’t match any rule, the firewall may block it by default (depending on its configuration).

### 3. Direction-Based Filtering

* **Inbound Rules**: Control traffic coming *into* the system.
* **Outbound Rules**: Control traffic *leaving* the system.

### 4. Filtering Criteria

Firewalls filter traffic based on:

* Port numbers (e.g., TCP 139, 80, 443)
* IP addresses (source or destination)
* Protocols (TCP, UDP, ICMP)
* Applications or services
* Network profiles (Private, Public, Domain)

---

##  Windows Firewall Behavior

When **Windows Firewall** is enabled:

* It blocks unsolicited **inbound traffic** by default.
* Outbound traffic is usually allowed unless blocked explicitly.
* Users can add **allow or block rules** to override the default behavior.

---

## Practical Example

*  When Windows Firewall is **disabled**, services like SMB on port 139 are visible to scans (e.g., Nmap shows them as `open`).
*  When Windows Firewall is **enabled**, these ports appear as `filtered`, meaning the firewall is silently dropping packets.
*  If a user adds an **allow rule** for port 139, it will show as `open` again in external scans.

---

##  Why It Matters

Firewalls are essential for:

* Blocking unauthorized access
* Reducing the system’s attack surface
* Enforcing security policies
* Protecting services from being exposed unnecessarily
