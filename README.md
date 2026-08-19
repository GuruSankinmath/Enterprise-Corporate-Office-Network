# Enterprise Corporate Office Network

A Cisco Packet Tracer-based enterprise network designed and implemented to simulate a corporate office environment using a Layer-3 core and access-layer architecture.

## Network Topology

The topology includes an Internet/Cloud connection, ISP router, edge router, Layer-3 core switch, two access switches, two servers, and end-user PCs.

![Enterprise Corporate Office Network Architecture](topology/enterprise-network-architecture.png)

## Project Objectives

- Segment the corporate network using VLANs.
- Provide Inter-VLAN communication through the Layer-3 core switch.
- Use 802.1Q trunking between the core and access layer.
- Use LACP EtherChannel to aggregate multiple physical links.
- Provide centralized DHCP services.
- Use DHCP Relay so clients in different VLANs can obtain IP addresses from the DHCP server.
- Prepare the network for centralized DNS and NTP services.
- Provide a structured foundation for ACL, NAT/PAT, SSH, and STP configuration.
- Test and troubleshoot the network using Cisco Packet Tracer and Cisco IOS commands.

## Network Devices

| Device | Quantity |
|---|---:|
| Cloud-PT | 1 |
| Routers | 2 |
| Layer-3 Core Switch | 1 |
| Access Switches | 2 |
| Servers | 2 |
| PCs | 12 |

## VLAN and IP Addressing Plan

| VLAN | Purpose | Network | Gateway |
|---:|---|---|---|
| 10 | HR | 192.168.10.0/24 | 192.168.10.1 |
| 20 | Finance | 192.168.20.0/24 | 192.168.20.1 |
| 30 | IT | 192.168.30.0/24 | 192.168.30.1 |
| 40 | Sales | 192.168.40.0/24 | 192.168.40.1 |
| 50 | Guest | 192.168.50.0/24 | 192.168.50.1 |
| 60 | Management | 192.168.60.0/24 | 192.168.60.1 |
| 70 | Server Services | 192.168.70.0/24 | 192.168.70.1 |
| 80 | Application Server | 192.168.80.0/24 | 192.168.80.1 |
| 99 | Native/Management | 192.168.99.0/24 | 192.168.99.1 |

## Server Configuration

| Server | Role | VLAN | IP Address |
|---|---|---:|---|
| Server 1 | DHCP / DNS / NTP | 70 | 192.168.70.10 |
| Server 2 | File / Web / Application | 80 | 192.168.80.10 |

## Technologies Configured

The following items have been configured in the current Packet Tracer project:

- VLANs
- 802.1Q Trunking
- Inter-VLAN Routing using SVIs
- LACP EtherChannel
- Centralized DHCP
- DHCP Relay

## Technologies Pending Final Configuration / Verification

The following should be added to the implemented list only after they are actually configured and verified in the Packet Tracer file:

- DNS
- NTP
- ACL
- NAT/PAT
- SSH
- STP
- Final end-to-end verification

## Key Features

- Department-wise network segmentation using VLANs
- Layer-3 switching for Inter-VLAN communication
- Centralized DHCP with DHCP Relay
- LACP EtherChannel for link aggregation
- Dedicated server VLANs
- Enterprise-style hierarchical network design

## Testing and Verification

Useful Cisco IOS verification commands:

```text
show vlan brief
show interfaces trunk
show etherchannel summary
show ip interface brief
show ip route
show running-config
show ip dhcp binding
```

Basic connectivity testing:

```text
ping <destination-ip>
traceroute <destination-ip>
```

## Project Structure

```text
enterprise-corporate-office-network/
├── README.md
├── topology/
│   └── enterprise-network-architecture.png
├── packet-tracer/
│   └── Enterprise_Corporate_Office_Network.pkt
├── configs/
│   ├── Core-Switch.txt
│   ├── Access-Switch-1.txt
│   ├── Access-Switch-2.txt
│   ├── Edge-Router.txt
│   └── ISP-Router.txt
├── addressing/
│   └── ip-addressing-table.md
└── verification/
    └── verification-commands.md
```

## Project Outcome

This project demonstrates practical networking skills in VLAN segmentation, Layer-3 switching, 802.1Q trunking, LACP EtherChannel, centralized DHCP, DHCP Relay, network troubleshooting, and Cisco Packet Tracer-based implementation.

> Note: Only claim a technology as implemented after it has been configured and successfully verified in the Packet Tracer project.
