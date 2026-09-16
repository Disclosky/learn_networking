# DHCP Lease Test

### Objective
  The objective of this experiment is to observe how a device can have their IP address and other configurations without user manually configure it one by one using DHCP.

### DHCP Configuration

 ???
 

---
### 1. What Happen If I Erase IP Configured In My Laptop?
  By using `ipconfig /release` we can acieve that. It will erase all Network Adapter that configured by DHCP on our device.

  ![0.0.0.0](./img/Screenshot_2026-09-16_070823.png)

  Interestingly the computer will notice that they are connected to a network but don't have an IP address. So our computer will broadcasting  

  



---
### What I learned

  - DHCP provides network configuration to clients.
  - DHCP can provide the client's IP address, subnet mask, default gateway, DNS server, and lease duration.
