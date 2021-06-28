# Chapter 1 Review Questions

## Section 1.1

1. **What is the difference between a host and an end system? List several different types of end
   systems. Is a Web server an end system?**

   A host is an end system.

   Laptops, smartphones, tablets, TVs, game consoles, home appliances, watches, eye glasses, cars.

   Yes.

2. **The word protocol is often used to describe diplomatic relations. How does Wikipedia
   describe diplomatic protocol?**

   "Protocol is commonly described as a set of international courtesy rules. These well-established and time-honored rules have made it easier for nations and people to live and work together. Part of protocol has always been the acknowledgment of the hierarchical standing of all present. Protocol rules are based on the principles of civility."

3. **Why are standards important for protocols?  **

   "It’s important that everyone agree on what each and every protocol does, so that people can create systems and products that interoperate." - p31

## Section 1.2

4. **List six access technologies. Classify each one as home access, enterprise access, or widearea wireless access. **

   Home access: DSL (digital subscriber line), cable, FTTH (fiber to the home), dial-up.

   Enterprise access: LAN (local area network), ethernet, wireless LAN, WiFi.

   Wide-area wireless access: 4G.

5. **Is HFC transmission rate dedicated or shared among users? Are collisions possible in a downstream HFC channel? Why or why not?**

   Shared (p42). 

   No.

   "A *network collision* occurs when more than one device attempts to send a *packet* on a *network* segment at the same time" - [Wikipedia](https://en.wikipedia.org/wiki/Collision_domain). E.g., in upstream channel of HFC, multiple homes may send packets to the head end simultaneously, so collisions are possible in the upstream channel. But in downstream channel, all packets come from a single source (head end), so collision is not possible in a downstream HFC channel.

6. **List the available residential access technologies in your city. For each type of access, provide the advertised downstream rate, upstream rate, and monthly price.**

7. **What is the transmission rate of Ethernet LANs?**

   100Mbps, 1Gbps, 10Gbps.

8. **What are some of the physical media that Ethernet can run over?**

   Twisted-pair copper wire.

   **Or fibre optic links.**

9. **Dial-up modems, HFC, DSL and FTTH are all used for residential access. For each of these access technologies, provide a range of transmission rates and comment on whether the transmission rate is shared or dedicated.**

   Dial-up: 56 kbps, dedicated.

   HFC: Downstream <= 42.8 Mbps, upstream <= 30.7 Mbps, shared.

   DSL: Downstream 12 Mbps and upstream 1.8 Mbps, or downstream 55 Mbps and upstream 15 Mbps, dedicated.

   FTTH: 20Mbps, dedicated.

10. **Describe the most popular wireless Internet access technologies today.­ Compare and contrast them.**

    WiFi: Local area network (LAN) access, user transmits/receives packets within tens of meters from an access point connected into the enterprise’s network (using wired Ethernet).

    3G/4G: Wide-area wireless access, user transmits/receives packets within tens of kilometers from base station operated by cellular network provider.

## Section 1.3

11. **Suppose there is exactly one packet switch between a sending host and a receiving host. The transmission rates between the sending host and the switch and between the switch and the receiving host are $R_1$ and $R_2$, respectively. Assuming that the switch uses store-and-forward packet switching, what is the total end-to-end delay to send a packet of length $L$? (Ignore queuing, propagation delay, and processing delay.)**

    $\frac{L}{R_1} + \frac{L}{R_2}$.

    At time $0$: Sending host starts transmitting.

    At time $\frac{L}{R_1}$: Packet switch receives entire packet and starts transmitting.

    At time $\frac{L}{R_2}$: Receiving host receives entire packet.

12. **What advantage does a circuit-switched network have over a packet-switched network? What advantages does TDM have over FDM in a circuit-switched network?**

    More stable as resources such as bandwidth are reserved for the duration of the communication, no unpredictable end-to-end delays.

    **FDM requires sophisticated analog hardware to shift signal into appropriate frequency bands.**

13. **Suppose users share a 2 Mbps link. Also suppose each user transmits continuously at 1
    Mbps when transmitting, but each user transmits only 20 percent of the time. (See the
    discussion of statistical multiplexing in Section 1.3 .)**

    1. **When circuit switching is used, how many users can be supported?**

       Two. Even if each user is active only 20% of the time, 1Mpbs bandwidth must be reserved at all times.

    2. **For the remainder of this problem, suppose packet switching is used. Why will there be
       essentially no queuing delay before the link if two or fewer users transmit at the same
       time? Why will there be a queuing delay if three users transmit at the same time?**

       If two or fewer users transmit at the same time, the required bandwidth is <= 2Mbps. Since the available bandwidth of the shared link is 2Mbps, there will be no queuing delay before the link.

       If three users transmit at the same time, the required bandwidth is 3Mbps, which is more than the available bandwidth of 2Mbps., so there will be queuing delay.

    3. **Find the probability that a given user is transmitting.**

       $0.2$.

    4. **Suppose now there are three users. Find the probability that at any given time, all three
       users are transmitting simultaneously. Find the fraction of time during which the queue
       grows.**

       $0.2^3 = 0.008.$

       The queue grows when all three users are transmitting.

14. **Why will two ISPs at the same level of the hierarchy often peer with each other? How does an IXP earn money?**

    













