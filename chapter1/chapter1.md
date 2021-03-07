# Chapter 1

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

**Transmission Control Protocol (TCP).** Controls the sending and receiving of information.

**Internet Protocol (IP).** Specifies the format of the packets sent/received among routers and end systems.