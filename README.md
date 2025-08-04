# nmap-scan
# What is Nmap?

[Nmap](https://nmap.org/) (Network Mapper) is a powerful open-source tool used for network discovery and security auditing. It allows users to:

- Detect hosts and services on a network.
- Identify open ports and running services.
- Perform OS detection, version detection, and more.
- Audit network security posture.

System administrators and cybersecurity professionals commonly use Nmap to assess the vulnerability of their systems and networks.
# What are Open Ports?
Open ports are network ports on a host that are configured to accept incoming connections. Each port corresponds to a specific service or application, for example:

- **Port 22 – SSH (Secure Shell)
- **Port 80 – HTTP (Web traffic)
- **Port 443 – HTTPS (Secure web traffic)

An open port means the service is accessible, which can be normal (e.g., for a web server) or a potential security risk if unintentionally exposed.
# What is a TCP SYN Scan?

A TCP SYN scan (also known as a "half-open scan") is the default and most popular scan type in Nmap. It works by:

1. Sending a SYN packet to a target port.
2. If the port is open, the target replies with a SYN-ACK.
3. Nmap then sends a RST (reset) to avoid completing the handshake.
4. If the port is closed, the target responds with a RST.
5. If no response or a filtered response occurs, the port is likely filtered (blocked by a firewall).
# Nmap command used:
nmap -sS -p- 192.168.1.1
# Output Summary:
PORT     STATE SERVICE
22/tcp   open  ssh
80/tcp   open  http
443/tcp  open  https
3306/tcp open  mysql
