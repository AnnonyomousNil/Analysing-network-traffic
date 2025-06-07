# Analysing-network-traffic
**TASK 5** 
Capturing Network Traffic Using Wireshark

Network traffic analysis is a critical practice for cybersecurity detection and network administration. This guide demonstrates Wireshark usage for monitoring and troubleshooting.

## Key Benefits
- **Threat Detection**: Identify malicious activity patterns
- **Troubleshooting**: Diagnose connectivity issues
- **Protocol Analysis**: Verify communication standards
- **Performance Optimization**: Plan network capacity

## Installation

### Windows
Official installation guide:  
[Wireshark Windows Documentation](https://www.wireshark.org/docs/wsug_html_chunked/ChBuildInstallWinInstall.html)

### Linux (Debian-based)
1. Install package:

```bash
sudo apt install wireshark
```

2. Add user to wireshark group:

```bash
sudo usermod -aG wireshark $(whoami)
```

3. Launch application:
```bash
wireshark
```

---

## Traffic Capture Tutorial

1. **Start Session**
- Select active interface. In my case it was `wlan0` for WiFi
- Click Start button (shark fin icon)

2. **Generate Traffic**
- Basic test:
  ```
  ping example.com
  ```
- Web traffic: Visit websites in browser

3. **Analyze Packets**
- Common protocol filters:
  - `http`: Web requests
  - `dns`: Domain resolution
  - `tcp`: Connection-oriented traffic
  - `arp`: Address resolution

4. **Export Results**
- File → Export Packet Dissections → As PCAP

---

## Protocol Reference
| Protocol | Purpose                          | Port  |
|----------|----------------------------------|-------|
| HTTP     | Web page transfer                | 80    |
| HTTPS    | Secure web transfer              | 443   |
| DNS      | Domain name resolution           | 53    |
| SSH      | Secure remote access             | 22    |

> **Note**: Requires admin/root privileges for interface access
