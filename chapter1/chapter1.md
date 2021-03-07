# Chapter 1

[TOC]

## Internet basics

### Components

**Access network.** A type of network that connects subscribers to their immediate service provider.

**Core network.** Connects local providers to one another.

**Host/End systems.** Devices connected to internet.

**Communication link.** Link that connects the hosts.
- Physical media: copper wire, optical fiber, radio spectrum, coaxial cable, etc.
- Transmission rate: bit/sec.

**Packet.** Data segment transferred by end system.
- Header: Bytes added to each segment containing source/destination info.

**Packet switch.** Takes a packet from one of its incoming communication links and forwards to one of its outgoing links.
- Routers: Used in network core.
- Link-layer switches: Used in access networks.

**Route/path.** Sequence of communication links and packet switches traversed by a packet from the sending end system to receiving end system.

**Internet Service Providers (ISP).** Provides network access to end systems.
- Is itself a network of packet switches and communication links.
- Types: Residential ISP, corporate ISP, university ISP, etc.
- Types of access: Cable modem, local area network (LAN), mobile wireless access.
- Each ISP network is managed independently and runs the IP protocol.

### Protocols

**Protocol.** Defines the format and order of messages exchanged between two or more communicating entities, as well as the actions taken on the transmission/receipt of a message or other event.
- All internet activity that involves two or more communicating remote entities is governed by a protocol.
- Different protocols are used in different communication tasks.

**Transmission Control Protocol (TCP).** Controls the sending and receiving of information.

**Internet Protocol (IP).** Specifies the format of the packets sent/received among routers and end systems.

**Hypertext Transfer Protocol (HTTP).** Application layer protocol for distributed, collaborative, hypermedia information systems.

**Simple Mail Transfer Protocol (SMTP).** A communication protocol for electronic mail transmission.

### Services

**Socket interface.** Rules the sending program must follow so that the internet can deliver data to the destination program.

## Network Edge

**Host/End system.** Devices that sit at the edge of the internet, running (hosting) application programs.
- Clients: Desktops, laptops, smartphones, etc.
- Servers: Web servers, email servers, etc.

### Access Networks

**Access networks.** Network that physically connects an end system to the first router (edge router) on a path from the end system to any other distant end system.

#### Home access

**DSL (digital subscriber line).** Internet access from the same telco (telephone company) that provides wired local phone access.
- Uses existing telephone line (twisted-pair copper wire)
- Frequency-division multiplexing: Uses different frequency than telephone signal channel to transmit digital signals (a telephone call and an internet connection can share the DSL link at the same time)

**Cable.** Internet access from the same cable TV company that provides cable TV
- Uses Optical fiber, coaxial cable
- Uses cable modem
- Shared broadcast medium

**FTTH (fiber to the home).** Optical fiber path from the central office (CO) directly to the home
- Optical distribution from CO to home
- Direct fiber: One fiber from CO for each home
- Split fiber: Many homes share fiber from CO, which then splits into different fiber
    - Active optical network (switched Ethernet)
    - Passive optical network

**Dial-Up.** A home modem connects to ISP modem over a phone line
- Same model as DSL
- Very slow

**Satellite link.**

#### Enterprise (and Home) Access

**Local area network (LAN).** Used to connect an end system to the edge router.

**Ethernet.** Most prevalent LAN access technology.
- Users use twisted-pair copper wire to connect to Ethernet switch, which is connected to a router, which connects to the ISP.

**Wireless LAN.** Wireless connection to LAN.
- Users transmit/receive packets to/from an access point connected into the enterprise’s network (using wired Ethernet).

**WiFi.** A Wireless LAN access based on certain IEEE technology.


