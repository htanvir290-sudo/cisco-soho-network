# SOHO Enterprise Network Architecture (Phase 1)

This project demonstrates a basic Small Office / Home Office (SOHO) network setup configured in Cisco Packet Tracer. It establishes basic Layer 3 connectivity between office workstations, a local file server, and a central gateway router.

## Network Topology

The network consists of:
* 1 Cisco 2911 Router (Gateway)
* 1 Cisco 2960 Switch
* 2 Workstations (HR-PC, Admin-PC)
* 1 Central File Server

## IP Addressing Table

| Device | Interface | IP Address | Subnet Mask | Default Gateway |
| :--- | :--- | :--- | :--- | :--- |
| Main-Office-Router | GigabitEthernet0/0 | 192.168.1.1 | 255.255.255.0 | N/A |
| HR-PC | FastEthernet0 | 192.168.1.10 | 255.255.255.0 | 192.168.1.1 |
| Admin-PC | FastEthernet0 | 192.168.1.11 | 255.255.255.0 | 192.168.1.1 |
| File-Server | FastEthernet0 | 192.168.1.50 | 255.255.255.0 | 192.168.1.1 |

## Configuration & Verification

1. Configured static IP addressing on all end devices.
2. Enabled the `GigabitEthernet0/0` interface on the gateway router and assigned the IP `192.168.1.1`.
3. Verified connectivity using ICMP ping from `HR-PC` (`192.168.1.10`) to `File-Server` (`192.168.1.50`).

## File Contents

* `cisco-soho-network.pkt`: The Cisco Packet Tracer lab environment file.
* `ping-test.png`: Verification screenshot of the successful ICMP ping output.