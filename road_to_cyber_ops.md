# CYBERSECURITY REVIEWER

## 1. NETWORKING FUNDAMENTALS (CCNA CORE)
> BATAK KA NA BA SA NETWORKING FUNDAMENTALS? ARALIN MO NA TOH!

### 1.1 OSI MODEL (RECAP)
> THE OSI (Open Systems Interconenction) model is a conceptual framework that standardizes how data travels across a network, divided into 7 layers. Every cybersecurity attack, tool, and defense mechanism maps to one or more of these layers.

| Layer | Name | PDU | Protocol / Device | Attacks | Defenses |
| ----- | ---- | --- | ----------------- | ------- | -------- |
| 7 | `Application` | Data | HTTP, HTTPS, DNS FTP, SMTP, SNMP, SSH | Phishing, XSS, SQLi, DNS poisoning, malware | WAF, App Patching, Input Validation DNSSEC |
| 6 | `Presentation` | Data | SSL/TLS, JPEG, ASCII, MPEG, Base64 | SSL Stripping, weak cipher exploit, cert spoofing | Enfore TLS 1.3, disable weak ciphers, HSTS |
| 5 | `Session` | Data | NetBIOS, RPC, PPTP, SIP, NFS | Session hijacking, session fixation, replay attacks | Session timeouts, secure tokens, ID rotation |
| 4 | `Transport` | Segment | TCP, UDP | SYN flood, port scanning, UDP flood, TCP hijack | Firewalls, SYN cookies, rate limiting, IPS |
| 3 | `Network` | Packet | IP, ICMP, OSPF, BGP, Router | IP Spoofing, ICMP flood, Smurf, BGP hijack | ACLs, ingress/egress filtering, IPSec |
| 2 | `Data Link` | Frame | Ethernet, MAC, ARP, Switch, 802.11, STP | ARP poisoning, MAC flooding, VLAN hopping | DAI, Port Security, 802.1X, DHCP Snooping |
| 1 | `Physical` | Bit | Hubs, Cables, NICs, Fiber, Wi-Fi Radio | Wiretapping, keyloggers, RF jamming | Locked rooms, cable shielding, cameras |

# Layer 7 APPLICATION
The layer users interact with directly. Provides network services to applications, not the apps themselves, but the protocols that let apps communicate.
  - What it does: Provices interfaces for email, web browsing, file transfer, remote access
  - PDU (Protocol Data Unit): Data
  - Key protocols: `HTTP(80), HTTPS(443), FTP(21), SSH(22), SMTP(25), DNS(53), SNMP(161)`

| Attack | How It Works | Example |
| ------ | ------------ | ------- |
| `Phishing` | `Fake pages/emails` trick users into giving credentials | Spoofed bank login page sent via email |
| `SQL Injection` | `Malicious SQL` in input fields manipulates the database | `'OR '1'='1` bypasses login form |
| `XSS` | `Injected JavaScript` runs in victim's browser | Stealing session cookies from other users |
| `DNS Poisoning` | `Corrupt DNS cahce` redirects users to malicious IPs | Redirecting bank.com to a fake phishing site |
| `Command Injection` | `OS commands injected` via application input | `; cat /etc/passwd` appended to a web form |
| `Malware Delivery` | `Malicious files/links` served via HTTP or email | Drive by download, malicious Office macro |
>[!TIP]
> Defenses: WAF, input validation, parameterized queries, DNSSEC, content filtering, antivirus, app patching
