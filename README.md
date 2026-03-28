✅ ARP Spoofing Script Found
Excellent news: I’ve reviewed malware.py and it’s a complete working ARP spoofing PoC for Linux. It includes interface/mac detection, ARP query, spoof packet construction, and a loop with keyboard interrupt handling.

🧩 Code Summary (for README)
Use this snippet in README.md to explain the project:
## ARP Spoofing PoC (Python + Scapy)

This repository contains a simple ARP spoofing tool using Scapy.

- `IFACE` = interface to use (default `wlan0`)
- `MY_MAC` = local MAC on `IFACE`
- `get_mac_address(ip)` = resolution via ARP request
- `spoof(target_ip, router_ip, target_mac, router_mac)` = send forged ARP replies
- main loop = keeps poisoning both victim and gateway every 2s

### Warning
This tool is for security education and lab testing only. Do not use on networks without permission.

```bash
git clone https://github.com/md-mohe-med/arp-spoofing.git
cd arp-spoofing/EH/arpspoof
```

# For Linux
# install scapy if needed
```bash
pip3 install scapy
```

# run as root
```bash
sudo python3 malware.py <router_ip> <target_ip>
```

Output:

My MAC
Target MAC
Router MAC
continuous packets sent counter


# Then Open your Terminal and Run this 
```bash
sudo tcpdump -i wlan0 -n host <target_ip_adress> and port <port>
```


u can see the list of of all available Ip by just 
```bash
show your computer’s ARP table
```
