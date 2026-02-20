# CISCO CLI COMMANDS REVIEWER

## 1. ROUTER / SWITCH MODE & NAVIGATION

| Command | Description |
| -------- | ----------- |
| `enable` / `en` | Enter privileged EXEC mode (Router#) |
| `configure terminal` / `conf t` | Enter Global Configuration mode (Router(config)#) |
| `interface g0/0` / `int g0/0` | Enter interface config mode |
| `exit` | Go back one level |
| `end` / `Ctrl + Z` | Return directly to Privileged EXEC |
| `do show...` / `do sh...` | Run show commands from config mode |
| `no [command]` | Negate / remove a command |
| `?` | Context-sensitive help |
| `Tab Key` | Auto-complete a command |

## 2. ESSENTIAL SHOW COMMANDS

| Command | Description |
| -------- | ----------- |
| `show running-config` / `sh run` | View current active configuration |
| `show ip interface brief` / `sh ip in br` | Quick overview of all interfaces and their IP/status |
| `show interfaces` / `sh int` | Detailed interface stats (errors, duplex, speed) |
| `show ip route` / `sh ip ro` | View the routing table |
| `show ip protocols` / `sh ip pro` | View routing protocol details (OSPF, RIP, etc.) |
| `show ip ospf neighbor` / `sh ip ospf nei` | OSPF neighbor relationship |
| `show ip ospf interface` / `sh ip ospf int` | OSPF cost, DR/BDR, hello/dead timers per interface |
| `show vlan brief` / `sh vlan br` | List all VLANs and assigned ports |
| `show interfaces trunk` / `sh int trunk` | Show trunk ports and allowed VLANs |
| `show etherchannel summary` / `sh eth sum` | EtherChannel status and protocol (LACP/PAgP) |
| `show port-security` / `sh port-sec` | Port security status on all interfaces |
| `show port-security interface g0/0` / `sh port-sec int g0/0` | Port security on specific interface |
| `show ip nat translation` / `sh ip nat trans` | Active NAT/PAT translation |
| `show ip nat statistics` / `sh ip nat stat` | NAT hit/miss counters |
| `show access-lists` / `sh acc` | View all ACLs and match counters |
| `show ip dhcp pool` / `sh ip dhcp pool` | DHCP pool info |
| `show ip dhcp binding` / `sh ip dhcp bind` | Active DHCP leases |
| `show ntp status` / `sh ntp stat` | NTP sync status |
| `show ntp associations` / `sh ntp ass` | NTP server associations |
| `show version` / `sh ver` | IOS version, uptime, hardware info |
| `show mac address-table` / `sh mac add` | MAC table entries |
| `show spanning-tree` / `sh span` | STP port states and root bridge info |
| `sh cdp neighbors detail` / `sh cdp neig det` | Discover directly connected Cisco devices |
| `sh lldp neighbors detail` / `sh lldp neig det` | Vendor-neutral alternative to Cisco's proprietary CDP, used to discover directly connected network devices |

> [!TIP]
> Remember to use the "`do`" keyword when executing privileged EXEC commands from configuration mode.

## 3. BASIC DEVICE SETUP
### 3.1 HOSTNAME & PASSWORDS

| Command | Description |
| ------- | ----------- |
| `hostname R1` | Set device hostname |
| `enable secret C1sc0123` | Set encrypted privileged EXEC password |
| `service password-encryption` | Encrypt all plaintext passwords in running-config |
| `no ip domain-lookup` | Stop router trying to DNS-resolve mistyped commands |
| `banner motd #Unauthorized Access Prohibited#` | Set login warning banner |
| `line console 0` | Enter console line config |
| > `password C1sc0123` | Set console password |
| > `login` | Enable password check on console |
| > `exec-timeout 5 0` | Auto-logout after 5 mins idle |

### 3.2 CONFIGURING INTERFACES

| Command | Description |
| ------- | ----------- |
| `interface g0/0` | Select interface |
| > `ip address 192.168.1.1 255.255.255.0` | Assign IP Address |
| > `no shutdown` | enable the interface (interfaces are shutdown by default on routers) |
| > `description Link to SW1` | Add description label |
| > `duplex full` | Set duplex (auto/half/full) |
| > `speed 100` | Set speed in Mbps |
| `interface l0` | Create/enter loopback interface |
| > `ip address 1.1.1.1 255.255.255.255` | Assign loopback IP (/32 typical) |
> [!TIP]
> Always end with "`no shutdown`", router interfaces are administratively down by default.

### 3.3 SSH CONFIGURATION

| Command | Description |
| ------- | ----------- |
| `ip domain-name cisco.com` | Required for RSA key generation |
| `crypto key generate rsa general-key modulus 2048` | Generate RSA keys for SSH |
| `ip ssh version 2` | Force SSH version 2 only |
| `username admin privilege 15 secret C1sc0123` | Create local user with max privilege |
| `line vty 0 4` | Enter VTY lines |
| > `transport input ssh` | Allow SSH only |
| > `login local` | Authenticate using local databse |

> [!NOTE]
> Goodluck to me :D - CodeAkyra
