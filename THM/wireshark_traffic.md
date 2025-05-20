### ARP Poisoning
```bash
arp.opcode == 1
arp.opcode == 2
arp.dst.hw_mac==00:00:00:00:00:00
arp.duplicate-address-detected or arp.duplicate-address-frame
((arp) && (arp.opcode == 1)) && (arp.src.hw_mac == target-mac-address)
```
### DHCP Analysis
```bash
dhcp or bootp
Request: dhcp.option.dhcp == 3
ACK: dhcp.option.dhcp == 5
NAK: dhcp.option.dhcp == 6
dhcp.option.hostname contains "keyword"
dhcp.option.domain_name contains "keyword"

```
### NetBIOS (NBNS) Analysis
```bash
nbns.name contains "keyword"
```
### Kerberos Analysis
```bash
kerberos
kerberos.CNameString contains "keyword" 
kerberos.CNameString and !(kerberos.CNameString contains "$" )
kerberos.pvno == 5
kerberos.realm contains ".org" 
kerberos.SNameString == "krbtg"
```
