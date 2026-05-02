- sniffing the wire, tapping the network, tapping into the wire
# Living Promiscuously
# Sniffing Around Hubs
- visibility window
# Sniffing in a Switched Environment
1. Port Mirroring: theorically work, not reliable enough in real world
2. Hubbing Out: works, but can reduce target from full-duplex to half-duplex
3. Using a Tap(Test Access Point): high volume traffic > choose nonaggregated tap (with fail-open capability)
4. ARP Cache Poisoning: be aware of high volume ('Cain&Abel' < 'bettercap')
5. Direct Install
- bonus: **asymmetric routing**
# Sniffing in a Routed Envrironment
# Sniffer Placement in Practice
## Network Map
- Automated Discovery Tool: Auvik, Domotz, SolarWinds NTM, Nmap
- Lucidchart, Draw.io(diagrams.net)
- Lucidchart AI, Whimsical, specialized AI Diagram Makers, Mermaid.js Code | EX:
```
"Create a network diagram with one Cisco router connected to a 24-port switch. The switch connects to three VLANs: Management (10.0.1.0/24), Finance (10.0.2.0/24), and Guest (192.168.1.0/24). Include a firewall between the router and the Internet."
```