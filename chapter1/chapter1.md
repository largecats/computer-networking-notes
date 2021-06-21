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
- Uses existing telephone line (twisted-pair copper wire).
- Frequency-division multiplexing: Uses different frequency than telephone signal channel to transmit digital signals (a telephone call and an internet connection can share the DSL link at the same time).

**Cable.** Internet access from the same cable TV company that provides cable TV.
- Uses Optical fiber, coaxial cable.
- Uses cable modem.
- Shared broadcast medium.

**FTTH (fiber to the home).** Optical fiber path from the central office (CO) directly to the home.
- Optical distribution from CO to home.
- Direct fiber: One fiber from CO for each home.
- Split fiber: Many homes share fiber from CO, which then splits into different fiber.
    - Active optical network (switched Ethernet)
    - Passive optical network

**Dial-Up.** A home modem connects to ISP modem over a phone line.
- Same model as DSL.
- Very slow.

**Satellite link.**

#### Enterprise (and Home) Access

**Local area network (LAN).** Used to connect an end system to the edge router.

**Ethernet.** Most prevalent LAN access technology.
- Users use twisted-pair copper wire to connect to Ethernet switch, which is connected to a router, which connects to the ISP.

**Wireless LAN.** Wireless connection to LAN.
- Users transmit/receive packets to/from an access point connected into the enterprise’s network (using wired Ethernet).

**WiFi.** A Wireless LAN access based on certain IEEE technology.

#### Wide-Area Wireless Access

**3G/4G.** Third/fourth-generation packet-switched wide-area wireless access at > 1Mbps.

**LTE.** Long-term evolution, over 10Mbps.

### Physical Media

**Guided media.** Bit sent by propagating electromagnetic waves or optical pulses across a solid medium.
- Optic fiber
- Copper wire
- Coaxial cable

**Unguided media.** Bit sent by waves propagating in the atmosphere and outer space.
- Wireless LAN
- Digital satellite channel

| Meida                    | Composition                      | Usage                 |
|--------------------------|----------------------------------|-----------------------|
| Twisted-pair copper wire |Two copper wires twisted to reduce electrical interference from other wires                                | Telephone network, LAN |
| Coaxial cable            | Two concentric copper conductors | Cable TV              |
Fiber optics                          |                    Conduct light pulses, each pulse is a bit|                       
| Terrestrial radio channels | Electromagnetic spectrum | Short distance: Wireless keyboards, local-area: LAN, Wide-area: Cellular access 
| Satellite radio channels | Links earth-based microwave ground stations | Geostationary satellites, Low-earth orbiting satellites |

## Network Core

### Packet Switching

**Store-and-forward transmission.** The packet switch must receive the entire packet before it starts transmitting.

**Output queue.** A packet switch link’s output buffer which stores packets that the router is about to send into that link.

**Queuing delay.** Time a packet spends waiting in the output buffer before being transmitted.

**Packet loss.** When an output queue is full, the arriving packet or one of the already-queued packet would be dropped.

**IP address.** An end system’s address in the internet.
$
- Included in the packet’s header.
- Hierarchical, like postal address.

**Forwarding table.** Router maps destination addresses to its outbound links.
- Set by routing protocols automatically.

### Circuit Switching

Need to reserve resources for communication.
- Telephone networks
- Wasteful, but more stable

**Frequency-division multiplexing (FDM).** Frequency spectrum of a link is divided up among circuits. Each circuit gets a frequency band.

**Time-division multiplexing (TDM).** Time is divided into revolving frames of fixed duration. Each frame is divided into fixed number of slots. Each circuit gets a time slot in each frame.
- E.g., 8000 frames/second, each slot has 8 bits, then transmission rate is 8000*8=64kbps.

## Network of Networks

**Access ISP.** Connect end systems into the Internet.
- Wired or wireless
- DSL, cable, FTTH, Wi-Fi, cellular.
- Telephone/cable company, university, company

**Points of presence.** A group of routers in the provider’s network where customer ISPs can connect into the provider ISP.

**Multi-home.** One access ISP connects with multiple regional/tier 1 ISPs.

**Peer.** A pair of nearby ISPs at the same level of hierarchy directly connect their networks.

**Internet Exchange Point (IXP).** A meeting point where multiple ISPs can peer together.

**Content-provider networks.** Like Google.
- May have own private networks.

### Packet-Switched Network

#### Delay

**Nodal processing delay.** Time required to examine the packet’s header and determine where to direct the packet.
- Microseconds

**Queuing delay.** Time the packet spends waiting to be transmitted onto the link.
- Related to the traffic arriving at the queue.
- Can vary from packet to packet. Usually characterized statistically, e.g., average queuing delay.

**Transmission delay.** Time required to push all the packet’s bits into the link.
- Number of bits in packet / link transmission rate.
- Microseconds to milliseconds.

**Propagation delay.** Time required to propagate from the beginning of the link to the next router.
- Depends on the link’s physical medium.
- Distance between the two routers / propagation speed (close to the speed of light).
- Milliseconds.


#### Packet loss

#### Throughput


