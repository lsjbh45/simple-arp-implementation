# Simple ARP Program Implementation

Implementation of Simple ARP Program in order for using Ethernet directly from the Application Layer

Excercise for using the Socket API of the Data Link Layer for the Linux Operating System

Lab assignment of 2020-2R "Data Communications" class

## Backgrounds

- When an IP module wants to send an IP packet via Data Link Layer SAP(Service Access Point), it needs the destination MAC Address of the next hop node of the IP packet.
- The IP module get the destination address by the ARP module.
  - The ARP module maintains an ARP cache.
  - From this cache, IP layer can get destination MAC Address of next hop toward destination IP of the IP packet.
  - When the cache lookup missed, the ARP module performs the Address Resolution Procedure.

## Goals

- Implementation of Simple ARP Program:
  - The application on the VM1 send an ARP request
  - The application on the VM2 receives the request and sends a ARP reply
  - The application on the VM1 sends a data packet to the application the VM2
- Specifications
  - The application must use the `PF_PACKET` socket for all communication
  - The application may use any unused ethertype
    - Defined use 0xFFFE for ARP request and reply and 0xFFFD for the data packet
  - The application may use two sockets
    - One socket with `ETH_P_ALL` is enough to exchange all packets of the application.

## [Implementation](code.c)

## [Report](report.md)
