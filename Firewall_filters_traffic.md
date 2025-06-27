🔥 How a Firewall Filters Traffic
A firewall is a security system that monitors and controls incoming and outgoing network traffic based on predefined rules. It acts like a security guard that decides whether data packets should be allowed in or out of a computer or network.

🧱 Basic Working of a Firewall
Packet Inspection:
When data (in the form of packets) tries to enter or leave a system, the firewall inspects it.

Rule Matching:
The firewall checks if the packet matches any existing allow or block rules.

If it matches an allow rule, the packet is permitted.

If it matches a block rule, the packet is dropped.

If it doesn’t match any rule, the firewall may block it by default (depending on the firewall’s default policy).

Direction-Based Filtering:

Inbound Rules control traffic coming into the system.

Outbound Rules control traffic leaving the system.

Criteria for Filtering:
A firewall can filter traffic based on:

Port number (e.g., TCP 139, 80, 443)

IP address (source or destination)

Protocol (TCP, UDP, ICMP, etc.)

Application or service

Network profile (Private, Public, Domain)

🛡️ Windows Firewall Behavior
In Windows Firewall, when it's enabled:

It blocks unsolicited inbound traffic by default to protect the system.

Outbound traffic is usually allowed unless specifically blocked.

To allow a specific type of connection, you must manually create an inbound allow rule.

You can also block access to certain services by creating inbound block rules.

🧪 Example
When Windows Firewall is disabled, all services (e.g., SMB on port 139) are visible to external scans like Nmap.

When Windows Firewall is enabled, those ports appear as filtered, meaning the firewall is dropping those packets.

If you create an allow rule for port 139, it becomes visible again (open) in a scan.

✅ Why It Matters
Firewalls are essential for:

Preventing unauthorized access

Limiting attack surfaces

Enforcing organization/network security policies

Controlling service exposure in home or corporate environments

