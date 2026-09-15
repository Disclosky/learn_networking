# NETWORK INVENTORY

## Network Devices

| Device | Role | Connection | IP Address | Notes |
|---|---|---|---|---|
| ISP Gateway | Upstream gateway | Fiber | TBD | Located at neighbor's house |
| Home Router | Local router | Ethernet | TBD | Provides local network access |
| Smart TV | Client/End device | Wi-Fi | TBD | Wireless client |
| Smartphones | Client/End device | Wi-Fi | TBD | Wireless client |
| Laptop | Client/end device | Wi-Fi | TBD | Main workstation |

## Physical Connection
  The home network receives its upstream connection from a neighboring
  network through a Cat5e FTP Ethernet cable.

  The cable connects the upstream network to the home router.

## Cable Information
  - Manufacturer: SPECTRA
  - Category: Cat5e
  - Type: FTP(Foiled twisted pair)
  - Conductor: 24 AWG
  - Pairs: 4 twisted pairs

![ip address assigned to the devices, when the image was taken](network-overview/cisco-packet-tracer/topologyw-lil-bit-ip-config.png)

## Laptop Wireless LAN Configuration
I start with `ipconfig /all` command in cmd and this is what I see:
  ```
  IPv4 Address : 192.168.0.101
  Subnet Mask  : 255.255.255.0
  Gateway      : 192.168.0.1
  DHCP Server  : 192.168.0.1
  DNS          : 1.1.1.1
                 1.0.0.1
  ```
