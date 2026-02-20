# CISCO CLI COMMANDS REVIEWER

## 1. ROUTER / SWITCH MODE & NAVIGATION

| Commands | Description |
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

| Commands | Description |
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

> [!NOTE]
> Goodluck to me :D - CodeAkyra
