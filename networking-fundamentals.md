# Networking Fundamentals for Cybersecurity

## 1. Introduction

Computer networking allows devices to communicate and exchange data. Cybersecurity professionals study networks to understand traffic, identify suspicious activity, and protect systems from unauthorized access.

## 2. Important Networking Concepts

- **IP address:** Identifies a network interface on an IP network.
- **MAC address:** Identifies a network interface at the data-link layer.
- **Port:** A number used to identify a network service or application endpoint.
- **Protocol:** A set of rules governing communication between devices.
- **Packet:** A formatted unit of data transmitted across a network.
- **Router:** Forwards packets between networks.
- **Firewall:** Applies rules to allow or block network traffic.

## 3. Common Network Protocols

| Protocol | Default Port | Purpose |
|---|---:|---|
| HTTP | 80 | Web communication without transport encryption |
| HTTPS | 443 | Encrypted web communication using TLS |
| DNS | 53 | Resolves domain names to records such as IP addresses |
| SSH | 22 | Secure remote command-line access |
| FTP | 21 | Traditional file transfer; not encrypted by default |
| SMTP | 25 | Email transfer between mail servers |
| DHCP | 67/68 | Automatically assigns network configuration to clients |
| RDP | 3389 | Remote desktop access, commonly on Windows |

*Note: These are default ports. Services can be configured to use different ports.*

## 4. TCP vs UDP

### TCP — Transmission Control Protocol

- Establishes a connection before transferring application data.
- Provides reliable, ordered delivery.
- Retransmits data when required.
- Commonly used for HTTPS, SSH, and email transport.

### UDP — User Datagram Protocol

- Sends datagrams without establishing a TCP-style connection.
- Does not guarantee delivery or ordering.
- Has lower protocol overhead.
- Commonly used for DNS queries, streaming, and real-time communication.

## 5. The OSI Model

The OSI model divides network communication into seven conceptual layers.

| Layer | Name | Example |
|---:|---|---|
| 7 | Application | HTTP, DNS |
| 6 | Presentation | Data representation and encryption concepts |
| 5 | Session | Session management |
| 4 | Transport | TCP, UDP |
| 3 | Network | IP routing |
| 2 | Data Link | Ethernet, MAC addressing |
| 1 | Physical | Cables, radio signals |

**Security relevance:** Understanding the layers helps organize network investigations and identify where a protocol or control operates.

## 6. DNS and HTTP/HTTPS

### DNS

DNS translates domain names into records used by networked systems. Investigators can examine DNS logs to identify unusual domains, unexpected lookups, or possible command-and-control activity.

### HTTP and HTTPS

HTTP is used for web communication. HTTPS protects communication using TLS, helping provide confidentiality and integrity in transit.

**Security lesson:** Encryption protects data in transit, but it does not automatically make a website or destination trustworthy.

## 7. Useful Linux Networking Commands

```bash
ip addr
ip route
ping 127.0.0.1
ss -tuln
```

- `ip addr` — Displays network interface addresses.
- `ip route` — Displays routing information.
- `ping 127.0.0.1` — Tests the local loopback interface.
- `ss -tuln` — Lists listening TCP and UDP sockets without resolving names.

Use these commands on your own system or an authorized lab.

## 8. Network Security Concepts

- **Firewall rules:** Control permitted inbound and outbound traffic.
- **Network segmentation:** Separates systems into different network zones.
- **IDS:** An Intrusion Detection System identifies potentially suspicious activity.
- **IPS:** An Intrusion Prevention System can block detected malicious activity.
- **Packet analysis:** Examines network packets to understand communication and investigate incidents.
- **Least privilege:** Limits access to only what is necessary.

## 9. Safe Practical Exercise

On your own Linux machine, run:

```bash
ip addr
ip route
ping -c 4 127.0.0.1
ss -tuln
```

Record your observations:

- Which network interfaces are present?
- Is a default route configured?
- Does the loopback test succeed?
- Which ports appear to be listening?

Do not assume a listening port is malicious. Identify the associated service and determine whether it is expected.

## 10. Key Takeaways

- IP addresses, ports, and protocols are fundamental to network communication.
- TCP and UDP have different delivery characteristics.
- The OSI model helps organize networking concepts.
- DNS and web traffic can provide useful investigation evidence.
- Network monitoring and packet analysis support threat detection.
- Only scan or test systems when you have permission.

## Learning Progress

**Status:** Networking fundamentals notes drafted.

**Next goal:** Practice the commands in an authorized environment and add your own observations.

---

*Original educational study notes. This document is not a walkthrough of a specific TryHackMe room.*
