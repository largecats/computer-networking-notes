# Homework Problems and Questions

## Chapter 1 Review Questions

### Section 1.1

1. A host is an end system.

Laptops, smartphones, tablets, TVs, game consoles, home appliances, watches, eye glasses, cars.

Yes.

2. "Protocol is commonly described as a set of international courtesy rules. These well-established and time-honored rules have made it easier for nations and people to live and work together. Part of protocol has always been the acknowledgment of the hierarchical standing of all present. Protocol rules are based on the principles of civility."
   
3. "It’s important that everyone agree on what each and every protocol does, so that people can create systems and products that interoperate." - p31

### Section 1.2

4. Home access: DSL (digital subscriber line), cable, FTTH (fiber to the home), dial-up.

   Enterprise access: LAN (local area network), ethernet, wireless LAN, WiFi.

   Wide-area wireless access: 4G.

5. Shared (p42). 

   No.

   "A *network collision* occurs when more than one device attempts to send a *packet* on a *network* segment at the same time" - [Wikipedia](https://en.wikipedia.org/wiki/Collision_domain). E.g., in upstream channel of HFC, multiple homes may send packets to the head end simultaneously, so collisions are possible in the upstream channel. But in downstream channel, all packets come from a single source (head end), so collision is not possible in a downstream HFC channel.

6. 

7. 100Mbps, 1Gbps, 10Gbps.

8. Twisted-pair copper wire.

   **Or fibre optic links.**

9. Dial-up: 56 kbps, dedicated.

   HFC: Downstream <= 42.8 Mbps, upstream <= 30.7 Mbps, shared.

   DSL: Downstream 12 Mbps and upstream 1.8 Mbps, or downstream 55 Mbps and upstream 15 Mbps, dedicated.

   FTTH: 20Mbps, dedicated.

10. WiFi: Local area network (LAN) access, user transmits/receives packets within tens of meters from an access point connected into the enterprise’s network (using wired Ethernet).

    3G/4G: Wide-area wireless access, user transmits/receives packets within tens of kilometers from base station operated by cellular network provider.

### Section 1.3

11. $\frac{L}{R_1} + \frac{L}{R_2}$.

    At time $0$: Sending host starts transmitting.

    At time $\frac{L}{R_1}$: Packet switch receives entire packet and starts transmitting.

    At time $\frac{L}{R_2}$: Receiving host receives entire packet.

12. More stable as resources such as bandwidth are reserved for the duration of the communication, no unpredictable end-to-end delays.

    **FDM requires sophisticated analog hardware to shift signal into appropriate frequency bands.**

13. 
    
    1. Two. Even if each user is active only 20% of the time, 1Mpbs bandwidth must be reserved at all times.

    2. If two or fewer users transmit at the same time, the required bandwidth is <= 2Mbps. Since the available bandwidth of the shared link is 2Mbps, there will be no queuing delay before the link.
      
       If three users transmit at the same time, the required bandwidth is 3Mbps, which is more than the available bandwidth of 2Mbps., so there will be queuing delay.

    3. $0.2$.
    
    4. $0.2^3 = 0.008.$ The queue grows when all three users are transmitting.
   
14. To reduce payments to provider ISP.

    IXP is a meeting point where multiple ISPs can peer together, so it probably charges each ISP a fee lower than the cost to connect to a provider ISP.

15. "The Google data centers are all interconnected via Google’s private TCP/IP network, which spans the entire globe but is nevertheless separate from the public Internet. Importantly, the Google private network only carries traffic to/from Google servers." - p60.

    Save money and have more control.

### Section 1.4

16. Processing delay: Constant.

    Queuing delay: Variable, depends on traffic arriving at the link.

    Transmission delay: Constant, depends on the transmission rate and the number of bits inside the packet, which is fixed for a given packet.

    Propagation delay: Constant, depends on the link medium and the distance between two routers.

17. 

18. 
    $$
    \begin{align*}
    \text{Propagation delay} = \frac{2500 \cdot 10^3\text{m}}{2.5\cdot 10^8 \text{m/sec}} = 0.01\text{sec}.
    \end{align*}
    $$
     In general:
    $$
    \frac{d}{s} \text{sec}
    $$
    

    No. Propagation delay only depends on propagation speed and distance.

19. 

    1. 
       $$
       \min\{R_1, R_2, R_3\} = 500 \text{kbps}.
       $$
       
    2. $$
       \frac{4 \cdot 10^6 \text{byte} \cdot 8\text{bit/byte}}{500\cdot 10^3\text{bit/sec}} = 64\text{sec}.
       $$
    
     3. $100$ kbps.
$$
       \frac{4 \cdot 10^6 \text{byte} \cdot 8\text{bit/byte}}{100\cdot 10^3\text{bit/sec}} = 320\text{sec}.
$$

20. End system A creates packets by breaking the file into chunks and adding end system B's IP address to each chunk's header.

    The router uses a portion of the destination IP address to determine which link to forward the packet onto.

    The destination IP address is hierarchical, just like postal address.

21.  

### Section 1.5

22. **Error control, flow control, segmentation and reassembly, multiplexing, and connection setup**.

    Yes.

23. Application: Host application end points.

    Transport: Transfer application-layer messages between application endpoints.

    Network: Transfer transport-layer segments between hosts.

    Link: Transfer network-layer datagrams between nodes.

    Physical: Transfer individual bits in link-layer frame between nodes.

24. Application-layer message: Packets that one application end point wants to send to another end point.

    Transport-layer segment: Encapsulates application-layer message with transport-layer header.

    Network-layer datagram: Encapsulates transport-layer segment with a network-layer header.

    Link-layer frame: Encapsulates network-layer datagram with a link-layer header.

25. Network, link, and physical.

    Link and physical.

    Application, transport, network, link, and physical.

### Section 1.6

26. Virus requires user interaction to infect the device, while worm does not.

27. Botnet is created when an infected host spreads the virus to other hosts through network.

    In a DDoS attack, attacker can issue command to all compromised devices in the botnet to send messages to the target host in order to flood it.

28. Pretend to be Bob to Alice or vice versa.

    Modify messages being sent.

    Drop messages being sent.

## Problems

1. 

2. At time $N\frac{L}{R}$, packet $1$ arrives at destination, packet $2$ is at router $N-1$.

   At time $(N+1)\frac{L}{R}$, packet $2$ arrives at destination, packet $3$ is at router $N-1$.

   ...

   At time $(N+P-1)\frac{L}{R}$, packet $P$ arrives at destination.

   So total end-to-end delay for sending $P$ packets across $N$ links is
   $$
   (N+P-1)\frac{L}{R}.
   $$

3. 

   1. Circuit-switched network.

      1. The application has long running sessions with predictable bandwidth requirement, so it can benefit from the stable connection that circuit-switched network provides.
      2. The application does not have frequent idle periods. so bandwidth can be reserved without much waste.

   2. No.

      In the worst case, all applications transmit data at the same time. But since each link has more bandwidth than the sum of all applications' data rates, no congestion will occur.

4. 

   1. $4\cdot 4 = 16.$

   2. A -> B -> C: 4 connections.

      A -> D -> C: 4 connections.

      8 in total.

   3. Yes.

      Between A and C:

      * A -> B -> C: 2 connections.
      * A -> D -> C: 2 connections.

      Between B and D:

      * B -> C -> D: 2 connections.
      * B -> A -> D: 2 connections.

5. 

   1. Tollbooths are $150/2 = 75$km apart. Each tollbooth services at the rate of 12 sec/car.

      End-to-end delay from one tollbooth to the next is:
      $$
      \begin{align*}
      \text{Trasmission delay} + \text{Propagation delay} &= 10 \cdot 12\text{sec/car} + \frac{75\text{km}}{100\text{km/hour}}\\
      &= 2\text{min} + 45\text{min}\\
      &= 47\text{min}.
      \end{align*}
      $$
      There are two such travels, so the delay from the front of the first tollbooth to the front of the third tollbooth is $47\cdot 2 = 94$min.

      At the third tollbooth, the cars require another $2$min to be processed.

      So the delay from the front of the first tollbooth to after the third tollbooth is $96$min.

   2. 
      $$
      (8\cdot 12\text{sec/car} + 45\text{min})\cdot 2 + 8\cdot 12\text{sec/car} = 94.8\text{min}.
      $$

6. 

   1. 
      $$
      d_{\text{prop}} = \frac{m}{s}\text{sec}.
      $$
      
   2. 
      $$
      d_{\text{trans}} = \frac{L}{R} \text{sec}.
      $$
      
   3. 
      $$
      \left(\frac{L}{R} + \frac{m}{s}\right) \text{sec}
      $$
      
   4. At the beginning of the link, just leaving host A.
   
   5. In the link.
   
   6. At host B.
   
   7. 
      $$
      \begin{align*}
      &&d_{\text{prop}} &= d_{\text{trans}}\\
      &\Rightarrow &\frac{m}{2.5\cdot 10^8} &= \frac{120}{56\cdot 10^3} \\
      &\Rightarrow &m &\approx 536\text{km}.
      \end{align*}
      $$
   
7. Time it takes to generate a $56$-byte packet from analog (all bits in the packet need to be generated before it can be transmitted):
   $$
   \frac{56\text{byte}\cdot 8\text{bit/byte}}{64\cdot 10^3 \text{bit/sec}} = 7\text{msec}.
   $$
   

   Transmission delay:
   $$
   \frac{56\text{byte}\cdot 8\text{bit/byte}}{2\cdot 10^6\text{bit/sec}} = 0.224\text{msec}.
   $$
   So total time elapsed is:
   $$
   7 + 0.224 + 10 = 17.224\text{msec}.
   $$
   
8. 

   1. 
      $$
      \frac{3\cdot 10^6}{150\cdot 10^3} = 20.
      $$
      
   2. $0.1$.
   
   3. 
      $$
      {120 \choose n} 0.1^n \cdot (1-0.1)^{120-n}.
      $$
      
   4. 
      $$
      1 - \sum_{k=0}^{20}{120\choose k}0.1^k\cdot 0.9^{120-k}.
      $$
   
9. 

   1. $$
      N = \frac{1\cdot 10^9}{100\cdot 10^3} = 1000.
      $$

   2. $$
      \sum_{n=N+1}^M {M\choose n} p^n\cdot (1-p)^{M-n}
      $$

10. $$
    2\cdot d_{proc} + \sum_{i=1}^3\frac{L}{R_i} + \frac{d_i}{s_i}
    $$

    $$
    2\cdot 3\text{msec} + \left(3\cdot \frac{1500\text{byte}\cdot 8\text{bit/byte}}{2\cdot 10^6\text{bit/sec}} + \frac{(5000 + 4000 + 1000)\text{km}\cdot 10^3\text{m/km}}{2.5\cdot 10^8\text{m/sec}}\right) \cdot 1000\text{msec/sec} = 64\text{msec}.
    $$

11. $$
    \frac{L}{R} + \sum_{i=1}^3\frac{d_i}{s_i}
    $$

12. $$
    \frac{4.5\cdot 1500\text{byte}\cdot 8\text{bit/byte}}{2\cdot 10^6\text{bit/sec}} = 27\text{msec}.
    $$

    $$
    \frac{nL+(L-x)}{R}
    $$

13. 

    1. $$
       \frac{1}{N} \sum_{k=1}^{N-1} \frac{kL}{R} = \frac{N(N-1)L}{2NR} = \frac{(N-1)L}{2R}.
       $$

    2. Same as above.

14. 

    1. $$
       \frac{IL}{R(1-I)} + \frac{L}{R} = \frac{1}{1-I}\cdot \frac{L}{R} = \frac{1}{1-La/R}\cdot \frac{L}{R} = \frac{L}{R-La} = \frac{L/R}{1-aL/R}.
       $$

    2. With $x=\frac{L}{R}$, total delay is $\frac{x}{1-ax}$. Approaches infinity as $x$ approaches $\frac{1}{a}$.

15. Note that
    $$
    \frac{L\text{bit}}{R\text{bit/sec}} = \text{Time it takes to transmit a packet} = \frac{1\text{packet}}{\mu\text{packet/sec}}.
    $$
    
    $$
    \frac{L/R}{1-I} = \frac{L/R}{1-aL/R} = \frac{1/\mu}{1-a/\mu} = \frac{\mu}{\mu-a}.
    $$

16. $$
    a = \frac{N}{d} = \frac{(10+1)\text{packet}}{0.01\text{sec}+1/100\text{sec}} = \frac{11\text{packet}}{0.02\text{sec}} = 550\text{packet/sec}.
    $$

17. 
    
    1. Suppose there are $N$ nodes.
    
    $$
    d_{\text{end-end}} = \sum_{n=1}^N d_{n_{proc}} + d_{n_{trans}} + d_{n_{prop}},
    $$
    ​		where $d_{n_{trans}} = L/R_n$.
    
    2. 
       $$
       d_{\text{end-end}} = \sum_{n=1}^N d_{n_{proc}} + d_{n_{trans}} + d_{n_{prop}} + d_{n_{queue}}.
       $$
    
18. 

19. 

20. $$
    \min\{R_s, R_c, R/M\}.
    $$

21. If can only use one path, the maximum throughput is the maximum of the minimum link among all $M$ paths.
    $$
    \max\{\min\{R_{nm} | n=1,\ldots,N\} | m=1,\ldots,M \}
    $$
    If can use all $M$ paths, the maximum throughput is the sum of all paths' throughputs.
    $$
    \sum_{m=1}^M \min\{R_{nm}|n=1,\ldots,N\}
    $$
    
22. Probability that a packet is received is $(1-p)^N$.

    Probability that a packet is not received is $1 - (1-p)^N$, so average number of re-transmission is $1/(1-(1-p)^N)$.

23. 

    1. $L/R_s$ since the second packet queued at the first link.

    2. Yes, the second packet will queue at the second link if the time it takes for second packet to arrive at the second link is less than the time it takes for the first packet to be transmitted by the second link, i.e.:
       $$
       \frac{L}{R_s} + \frac{L}{R_s} + d_{prop} < \frac{L}{R_s} + d_{prop} + \frac{L}{R_c}
       $$
       This is the same as $R_c < R_s$, so if $R_c<R_s$. the second packet must queue at the second link.
       $$
       \begin{align*}
       \frac{L}{R_s} + \frac{L}{R_s} + d_{prop} + T &> \frac{L}{R_s} + d_{prop} + \frac{L}{R_c}\\
       \frac{L}{R_s} + T &> \frac{L}{R_c}\\
       T &> \frac{L}{R_c} - \frac{L}{R_s}.
       \end{align*}
       $$

24. FedEx. Using the link will take:
    $$
    \frac{40\cdot 10^{12}\text{byte}\cdot 8\text{bit/byte}}{100\cdot 10^6\text{bit/sec}} = 3.2\cdot 10^6\text{sec} \approx 37\text{days}.
    $$
    
25. 

    1. $$
       R\cdot d_{prop} = 2\cdot 10^6\text{bit/sec} \cdot \frac{20000\cdot 10^3\text{m}}{2.5\cdot 10^8\text{m/sec}} = 1.6\cdot 10^5\text{bit}.
       $$

    2. The number of bits in the link can be calculated as a "band area" where the width is the number of bits transmitted per second (bandwidth), and the length is the length of time a bit can stay in the link. This is exactly the bandwidth-delay product.

    3. Maximum number of bits that can be in the link at any given time.

    4. The width of a bit is the length of link / the number of bits in the link:
       $$
       \frac{20000\cdot 10^3\text{m}}{1.6\cdot 10^5\text{bit}} = 125\text{m/bit}
       $$
       Longer than a football field.

    5. $$
       \frac{m}{R\cdot m/s} = \frac{s}{R}.
       $$

26. $$
    \frac{s}{R} = m \Rightarrow R = \frac{s}{m} = \frac{2.5\cdot 10^8\text{m/sec}}{20000\cdot 10^3\text{m}} = 12.5\text{bps}.
    $$

27. 

    1. 

    $$
    R\cdot d_{prop} = 10^9\text{bit/sec} \cdot \frac{20000\cdot 10^3\text{m}}{2.5\cdot 10^8\text{m/sec}} = 8\cdot 10^7\text{bit}.
    $$

    2. $800000$ bits (minimum of maximum number of bits that can be in the link and the total number of bits)

    3. $$
       \frac{20000\cdot 10^3\text{m}}{800000\text{bit}} = 25\text{m/bit}.
       $$

28. 

    1. 

    $$
    d_{trans} + d_{prop} = \frac{800000\text{bit}}{2\cdot 10^6\text{bit/sec}} + \frac{20000\cdot 10^3\text{m}}{2.5\cdot 10^8\text{m/sec}} = 0.48\text{sec}.
    $$

    2. $$
       20\cdot \left(\frac{40000\text{bit}}{2\cdot 10^6\text{bit/sec}} + \frac{20000\cdot 10^3\text{m}}{2.5\cdot 10^8\text{m/sec}}\right) = 2\text{sec}.
       $$

    3. It takes longer to break down a file into segments and send them because each segment adds its propagation delay.

29. 

    1. According to p48, geostationary satellites are 36000km above earth. So propagation delay is
       $$
       \frac{36000\cdot 10^3\text{m}}{2.4\cdot 10^8\text{m/sec}} = 0.15\text{sec}.
       $$

    2. $$
       10\cdot 10^6\text{bit/sec} \cdot 0.15\text{sec} = 1.5\cdot 10^6\text{bit}.
       $$

    3. The image need to take 1min to be transmitted:
       $$
       10\cdot 10^6\text{bit/sec}\cdot 60\text{sec} = 6\cdot 10^8\text{bit}.
       $$

30.  

31.  

    1. Time it takes for the message to reach the first packet switch is
       $$
       \frac{8\cdot 10^6\text{bit}}{2\cdot 10^6\text{bit/sec}} = 4\text{sec}.
       $$
       Time it takes for the message to reach the destination is $4\cdot 3 = 12\text{sec}$ (source to first packet switch, first packet switch to second packet switch, second packet switch to destination - each takes $4$ seconds).

    2. Time it takes for the first packet to reach the first switch is
       $$
       \frac{10000\text{bit}}{2\cdot 10^6\text{bit/sec}} = 0.005\text{sec}.
       $$
       Time it takes for the second packet to reach the first switch is $0.005\text{sec}\cdot 2 = 0.01\text{sec}$.

    3. Total delay of sending $P$ packets across $N$ links:
       $$
       (N+P-1)\frac{L}{R} = (3+800-1)\frac{10000\text{bit}}{2\cdot 10^6\text{bit/sec}} = 4.01\text{sec}.
       $$
       This is much less than the $12$sec delay without segmentation.
       
    4. **Without message segmentation:**

       1. **if bit errors are not tolerated, if there is a single bit error, the whole message has to be retransmitted (rather than a single packet).  **
       2. **huge packets (containing HD videos, for example) are sent into the network. Routers have to accommodate these huge packets. Smaller packets have to queue behind enormous packets and suffer unfair delays.**
    
    5. **Drawbacks of message segmentation:**
       1. **Packets have to be put in sequence at the destination.**
       2. **Message segmentation results in many smaller packets. Since header size is usually the same for all packets regardless of their size, with message segmentation the total amount of header bytes is more.**
    
32.  

33. Delay of moving $N$ packets across $P$ links is
    $$
    (N+P-1)\frac{L}{R} = \left(3+\frac{F}{S}-1\right)\cdot \left(\frac{80+S}{R}\right) = \left(\frac{F}{S}+2\right)\cdot \frac{80+S}{R}.
    $$

34. **The circuit-switched telephone networks and the Internet are connected together at "gateways". When a Skype user (connected to the Internet) calls an ordinary telephone, a circuit is established between a gateway and the telephone user over the circuit switched network. The skype user's voice is sent in packets over the Internet to the gateway. At the gateway, the voice signal is reconstructed and then sent over the circuit. In the other direction, the voice signal is sent over the circuit switched network to the gateway. The gateway packetizes the voice signal and sends the voice packets to the Skype user.**



