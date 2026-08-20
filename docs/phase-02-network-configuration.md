## Phase 02 – OPNsense Three-Zone Network Configuration

### Network Configuration

| Interface | Device | Network | IP |
|---|---|---|---|
| WAN | em0 | VMnet8 | 192.168.10.134/24 |
| LAN | em1 | VMnet9 | 192.168.200.1/24 |
| DMZ | em2 | VMnet10 | 192.168.100.1/24 |

### DHCP

- LAN DHCP: 192.168.200.100 – 192.168.200.200
- DMZ DHCP: 192.168.100.100 – 192.168.100.200

### Connectivity Validation

- LAN → OPNsense: Successful
- WAN → Internet: Successful
- LAN → Internet: Successful
- LAN → DNS: Successful
- DMZ → OPNsense: Successful from firewall side
- DMZ → Internet: Successful
- DMZ → DNS: Successful


### Screenshots

1. [OPNsense Web GUI Dashboard](screenshots/phase-02/04-opnsense-web-gui-dashboard.png)

2. [OPNsense WAN, LAN and DMZ Interface Assignment](screenshots/phase-02/05-interface-assignments-wan-lan-dmz.png)

3. [OPNsense Interface Overview](screenshots/phase-02/06-interface-overview.png)

4. [Dnsmasq DHCP Ranges – LAN and DMZ](screenshots/phase-02/07-dnsmasq-dhcp-ranges.png)

5. [LAN Connectivity Test](screenshots/phase-02/08-lan-connectivity-ping.png)

6. [WAN Internet Connectivity Test](screenshots/phase-02/09-wan-internet-connectivity.png)

7. [LAN Internet and DNS Test](screenshots/phase-02/10-lan-internet-dns-test.png)

8. [OPNsense DMZ to Ubuntu Connectivity](screenshots/phase-02/11-opnsense-dmz-to-ubuntu.png)

9. [DMZ Internet and DNS Connectivity](screenshots/phase-02/12-dmz-internet-dns-test.png)