# Telecommunications and Network Security

A network protocol is a standard set of rules that determine how systems will communicate across networks.

OSI Model TCP/IP Model Application Presentation Application Session ----- ----- Transport Host-to-host ----- ----- Network Internet ----- ----- Data Link Network Access Physical ----- ----- OSI model's goal is to help others develop products that will work well within an open network architectutre. In an open network architecture, various technologies can be easily integrated and interoperability issues are less burdensome.

Encapsulation: a message is constructed at the application layer and then passed down through the protocol stack. Each layer adds its own information to the message. When the message is sent to the destination computer, the encapsulation is reversed by taking the message apart through the same steps as the source computer that encapsulated it.

Open systems are capable of communicating with other open systems because they implement international standard protocols and interfaces.

The application layer includes the protocols that support the applications. Applications send requests to an API, which is the doorway to the supporting protocol.

E.g. SMTP, HTTP, LPD, FTP, Telnet and FTP.

The presentation layer receives information from the application layer protocols and puts it into a format that all computers following the OSI model can understand. This layer provides a common means of representing data in a structure that can be properly processed by the end system. The presentation layer is not concerned with he meaning of data, but with the syntax and format of tha data.

E.g. TIFF, GIF, JPEG.

This layer also handles data compression and encryption.

The session layer is responsible for establishing a connection between the two applications, maintaining it during the transferring of data, and controlling the release of this connection. It provides session restart and recovery if necessary and provides the overall maintenance of the session. When the conversation is over, the path is broken down and all parameters are set back to their original settings. This process is known as dialog management.

Three phases of a session: connection establishment, data transfer, connection release E.g. NFS, SQL, RPC.

Simplex: communication takes place in one direction.

Half-duplex: communication takes place in both directions, but only one application can send information at a time.

Full-duplex: communication takes place in both directions, and both applications can send information at the same time.

The transport layer provides end-to-end data transport services and estabishes the logical connection between two communicating computers. The transport layer receives data from many applications and assembles the data into a stream so that it can be properly transmitted over the network. If data needs to be multiplexed, it happens at this layer.

Protocols that work at the session layer set up connections between applications and protocols that work at the transport layer set up connections between computer systems.

E.g. TCP, UDP, SPX, (SSL).

The network layer inserts information into the packet's header so that it can be properly routed. The protocols at this layer do not ensure the delivery of the packets; they depend on the protocols at the transport layer to catch any problems and resent packets if necessary.

E.g. IP, ICMP, RIP, OSPF, BGP, IGMP The data link layer is where the Network Stack knows what format the data frame must be in to transmit properly over Token Ring, Ethernet, Atm, or Fiber Distributed Interface networks. The data link layer is responsible for proper communication within these technologies and for converting the data into bits for the physical layer.

E.g. SLIP, PPP, RARP, L2F, L2TP, FDDI, ISDN The physical layer converts bits into voltage for transmission. This layer controls synchronization, data rates, line noise and medium access.

E.g. HSSI, X.21, EIA/TIA-232, EIA/TIA-449 TCP is a reliable and connection-oriented protocol.

UDP is a best-effort and connectionless-oriented protocol.

Connection-oriented communication performs handshaking, sets up a virtual circuit, and verifies that each packet reaches the destination.

Connectionless-oriented communication just puts the packets on the wire.

IP is a connectionless protocol that provides the addressing and routing capabilities for each package of data. It is the mechanism that enables the network to read IP addresses and implement proper routing functions.

When a TCP or UDP message is formed, a source and destination port are contained within the header informaton along with the source and destination address; this makes up a socket.

TCP Handshake A ------- SYN ------> B A <--- SYN/ACK --- B A ------- ACK ------> B TCP and UDP differ in terms of the following Reliability Connection Packet sequencing Congestion controls Usage Speed and overhead Layer TCP UDP Application Message Message Transport Segment Packet Network Datagram Datagram Data Link Frame Frame Analog tranmission signals are continuously varying electromagnetic waves that can be carried over air, water, twisted-pair, coaxial, or fiber optic cable.

Modulation of a signal differs in amplitude and frequency.

Digital signals represent binary digits as electrical pulses.

Local loop or last mile refers to the analog communication going over copper wiring from a residential house or business to the telephone company's central office.

Asynchronous communication is used when the two devices are not synchronized in any way. Systems that usually transfer large amounts of data will be developed and configured with synchronous communication mechanisms.

Synchronous communication takes place between two devices that are synchronized, usually via a clocking mechanism. Systems that transfer small amounts of data are developed with asynchronous means.

Baseband is a transmission method that is accomplished by applying direct current to a cable.

Baseband uses the entire cable for its transmission, whereas broadband divides the cable into channels so that different types of data can be transmitted at the same time.

Broadband, in general, provides data transmission rates higher than 56kbps, which is what a standard dial-up connection line provides.

Leased lines (T1, T3), ISDN, ATM, Digital Subscriber Line (DSL), broadband wireless and CATV are examples of broadband communications.

Four main reasons to have a network are:

- to allow communication between computers

- to share information

- to share resources

- to provide central administration The physical arrangement of computers and devices is called a network topology.

A ring topology has a series of devices connected by unidirectional transmission links. These links form a closed loop and do not connect to a central system, as in a star topology.

In a simple bus topology, a single cable runs the entire length of the network. Nodes are attached to the network through drop points on this cable. Data communications transmit the length of the medium and each packet transmitted has the capability of being lookd at by all nodes.

The linear bus topology has a single cable with nodes attached.

A tree topology has branches from the single cable, and each branch can contain many nodes.

In a star topology, all nodes connect to a central device such as a switch. Each node has a dedicated link to the central device.

In a mesh topology, all systems and resources are connected to each other in a way that provides multiple paths to all the nodes on the network.

A full mesh topology has ever node directly connected to every other node, which provides a great degree of redundancy.

In a partial mesh topology, ever node is not directly connected and each may be used to connect full mesh networks.

When two distinct LANs are connected by a router, the result is an internetwork, not a larger LAN. Each distinct LAN has its own addressing scheme, broadcast domain and communication mechanisms. If two LANs are connected by a different data link layer technology, such as frame relay or X.25, we are looking at a WAN.

Ethernet Type Cabling Type Speed 10Base2, ThinNet Coaxial 10Mbps 10Base5, ThickNet Coaxial 10Mbps 10Base-T UTP 10Mbps 100Base-TX, Fast Ethernet UTP 100Mbps 1000Base-T, Gigabit Ethernet UTP 1000Mbps LAN Implementation IEEE Standard Characteristics Ethernet 802.3 – Shared media – all devices must take turns using the same media and detect collisions – Uses broadcast and collision domains – Uses CMSA/CD access method – Can use coaxial or twister-pair media – Transmission speeds of 10Mbps-1Gbps Token Ring 802.5 – All devices connect to a central MAU – Token-passing media access method – Transmission speeds of 4-16Mbps – Uses an active monitor and beaconing FDDI (Fiber Distributed Data Interface) 802.8 – Token-passing media access method – Dual counter-rotating rings for fault tolerance – Transmission speeds of 100Mbps – Operates over long distances at high speeds and is therefore used as backbones – CDDI works over UTP Ethernet, Token Ring and FDDI are data link layer technologies. The data link layer is actually made up of a Media Access Control (MAC) layer and a Logical Link Control (LLC) layer. These technologies live at the MAC layer and have to interface to the LLC layer.

The bandwidth of a cable indicates the highest frequency range that it uses.

The data rate is the actual data throughput of a cable after compression and encoding have been used.

Coaxial cable has a copper core that is surrounded by a shielding layer and grounding wire. Coaxial cable is more resistant to electromagnetic interference (EMI), provides a higher bandwidth and longer cable lengths can be used compared to twister-pair cabling.

50-ohm cable is used for digital signaling 75-ohm cable is used for high-speed digital signaling and analog signaling.

Twisted-pair cabling has insulated copper wires that are surrounded by an outer protective jacket. Twisted-pair cabling is cheaper and easier to work with. Two-wire pairs within twister-pair cables form a balanced circuit because they both have the same amplitude, just with different phases.

If the cable has an outer foil shielding, it is referred to as shielded twisted pair (STP), which adds protection from radio frequency interference.

If the cable does not have this extra outer shielding, it is called unshielded twisted pair (UTP).

Twisting of wires protects the signals from radio frequency and electromagnetic interference, as well as crosstalk.

Fiber-optic cables use a type of glass that carries light waves, which represent the data that is being transmitted.

UTP Categories range from Cat 1 to Cat 7, with Cat1 providing the lowest speed and quality and Cat7 providingthe highest.

Noise on a line is caused by surrounding devices or characteristics of the wiring's environment.

Attenuation is the loss of signal strength as it travels. The longer the cable, the more attenuation will be introduced, and the signal that is carrying data will deteriorate. The effects of attenuation increase with higher frequencies.

Crosstalk occurs when electrical signals of one wire spill over to another wire.

Plenum space refers to areas where burning cables are capable of producing hazardous gases and such areas mst meet a specific fire rating to ensure that it will not produce and release harmful chemicals in case of a fire.

Nonplenum cables usually have a polyvinyl chloride (PVC) jacket covering Unicast tranmission occurs when a packet is sent from one source computer to one destination computer.

Multicast transmission occurs when a packet is sent from one source computer to several specific computers.

Broadcast transmission occurs when a packet is sent from one source computer to all computers on a certain network segment.

An MTU (maximum transmission unit) is a parameter that indicates how much data a frame can carry on a specific network.

A token is a 24-bit control frame used to control which computers communicate at what intervals. The token is passed from computer to computer, and only the computer that has the token can actually put frames onto the wire.Token-passing methods do not cause collisions because only one computer can communicate at a time. Only the originator of the message can remove the message from the token.

CSMA/CD – carrier sense multiple access with collision detection. Nodes monitor the tranmission activity or the carrier activity on the wire so that they can determine when would be the best time to transmit data.

CSMA/CA – carrier sense multiple access with collision avoidance. This is an access method in which each computer signals its intent to transmit data before it actually does so.

Contention means that nodes have to compete for the same shared medium.

Random collision timer executed by stattions to force a delay before attempting to transmit data is known as back-off algorithm.

Overalll, carrier-sensing access methods are faster than token-passing access methods, but the former have the problem of collisions.

A collision occurs on Ethernet networks when two computers transmit data at the same time.

A collision domain is a group of computers that are contending, or competing, for the same shared communication medium.

[Insert detail about how switches, routers, bridges and hubs create collision and broadcast domains.] Address Resolution Protocol (ARP) maps the hardware address (MAC address) and associated IP address and stores it in its table for a predefined amont of time.

ARP table poisoning is a type of masquerading attack.

ARP: broadcast IP and find MAC.

Reverse ARP (RARP) maps a broadcast hardware address to an IP address using a RARP server. Diskless workstations have just enough code to boot up and broadcast for an IP address.

BOOTP was created after RARP to enhance functionality that RARP provides for diskless workstations.

RARP: broadcast MAC and find IP.

Internet Control Message Protocol (ICMP) is basically IP's messenger protocol. ICMP delivers messages, reports errors, replies to certain requests, reports routing information and is used to test connectivity and troubleshoot problems on IP networks.

Ping: ICMP ECHO REQUEST ----> <---- ICMP REPLY A repeater repeats and amplifies electrical signals between cable segments. Repeaters work at the physical layer and are add-on devices for extending a network connection over a greater distance.

A hub is a multiport repeater.

A bridge is a LAN device used to connect LAN segments. It works at the data link layer and therefore works with MAC addresses.

Broadcast storms are caused by bridges that forward all broadcast packets and overwhelm the network, thereby degrading network bandwidth and performance.

Local bridge connects two or more LAN segments within a local area.

Remote bridge connects two or more LAN segments over a WAN using telecommunications links.

Translation bridges are needed if the two LANs being connected are different types and use different standards and protocols.

Functions of a bridge:

- segments a large network into smaller, more controllable pieces

- uses filtering based on MAC addresses

- joins different types of network links while retaining the same broadcast domain

- isolates collision domains within the same broadcast domain

- can take place locally within a LAN or remotely to connect two distant LANs

- can translate between protocol types Routers work at the network layer and filter packets based on IP addresses.

Bridges work at the data link layer and filter frames based on MAC addresses.

Routers will not usually pass broadcast information.

Bridgers will pass broadcast information.

When transparent bridging is used, a bridge starts to learn about the network's environment as soon as it is powered on and as the network changes.

When source routing is used, the packets contain the necessary information within them to tell the bridge where they should go. The packets hold the forwarding information so that they can find their way to their destination without needing bridges and routers dictate their paths.

External devices and border routers should not accept packets with source routing information within their headers.

What happens inside a router when it receives a packet?

- Frame received on one of the interfaces of a router. Router strips off header information to view routing data.

- Router retrieves destination IP network address from datagram; it does not care about the host portion of the IP address.

- Router looks at its routing table to see which router port matches the requested destination IP network address.

- If the router does not have the information, it sends out an ICMP error message to the sending computer.

- If the router does have a route for the destination, it decrements the Time to Live (TTL) value and sees whether the MTU is different for the destination network. If the destination network requires a smaller MTU, the router fragments the datagram.

- Router changes header information in the frame so the frame can go to the correct next router or its destination.

- Router then sends the frame to its output queue for the necessary interface.

Bridge Router reads header information, but does not alter it creates a new header for each frame builds forwarding tables based on MAC addresses builds routing tables based on IP addresses uses the same network address for all ports assigns a different network address per port filters traffic based on MAC addresses filters traffic based on IP addresses forwards broadcast packets does not forward broadcast packets forwards traffic if destination is unknown does not forward traffic if destination is unknown Routing environments are based on autonomous systems (ASs). An AS is an individual network that is managed by a specific authority and implements its own internal routing.

Internal routing protocols e.g. OSPF and RIP External routing protocols e.g. BGP A switch is a multiport connection device that provides connections for individual computers or other hubs and switches. Any device connected to one port can communicate with a device connected to another port with its own virtual private link. Each port on a switch provides a dedicated bandwith to the device attached to it.

Switches operate at the data link layer.

Multilayered switches perform most advanced tasks and activities within an application-specific integrated circuit (ASIC).

Virtual LANs (VLANs) enable administrators to separate and group computers logically based on resource requirments, security, or business needs instead of the standard physical location of the systems.

A gateway is a general term for software running on a device that connects two different environments and acts as a translator for them or somehow restricts their interactions.

A private branch exchange (PBX) can interface with several types of devices and provides a number of telephone services). PBXs use digital switching devices that can control analog and digital signals.

Firewalls are used to restrict access to one network from another network.

A demilitarized zone (DMZ) is a network segment that is located between the protected and the unprotected networks. The DMZ provides a buffer zone between the dangerous Internet and the goodies within the internal network that the company is trying toprotect.

Packet filtering is a security method of controlling what data can flow into and out of a network. Packet filtering takes place using ACLs, which are developed and applied to a device.

Pros:

- scaleable

- provides high performance

- application independent Cons:

- does not look into the packet past the header information

- low security relative to other options

- does not keep track of the state of a connection Stateful filtering/inspection remembers and keeps track of what packets went where until each particular connection is closed. Stateful firewalls maintain state tables to keep track of connections.

Characteristics of Stateful Inspection:

- firewall maintains a state table that tracks each and every communication channel

- frames are analyzed at all communication layers

- provides a high degree of security and does not introduce the performance hit that proxy firewalls introduce

- scaleable and transparent to users

- provides data for tracking connectionless protocols such as UDP and ICMP

- state and context of the data within the packets are stored and updated continuously

- considered a third generation firewall Regular packet filtering compares incoming packets to rules defined in its ACLs.

When stateful packet filtering receives a packet, it first looks in its state table to see whether a connection has already been established and whether this data was requested. If there was no previous connection and the state table holds no information about the packet, the packet is compared to the device's ACLs.

A proxy stands between a trusted and untrusted network and makes the connection, each way, on behalf of the source. A proxy firewall breaks the communication channel: there is no direction connection to internal computers. Packets are repackaged to contain the source address of the proxy server, not the host system on the internal network.

Pros and cons of proxy firewalls:

Pros:

- looks at information within a packet, possibly all the way up to the application layer

- provides better security than packet filtering

- breaks the connection between trusted and untrusted systems Cons:

- some proxy firewalls are limited to what applications it can support

- degrades traffic performance

- application-based proxy firewalls can have scalability issues

- breaks client/server model, which is good for security but at times bad for functionality A dual-homed firewall has two interfaces: one facing the external network and the other facing the internal network. Characteristics of dual-homed host firewalls:

- single computer with separate network cards connected to each network

- used to divide an internal trusted network from an external untrusted network

- must disable computer's forwarding and routing functionality so the two networks are truly segregated

- users can easily and accidentally enable packet forwarding, which can cause malicious traffic to enter the internal network Application-level proxies inspect the entire packet and make access decisions based on the content of the packet. Characteristics:

- different proxy required for each service allowed

- provides more intricate control than circuit-level proxy firewalls

- reduces network performance A circuit-level proxy creates a circuit between the client computer and the server. It knows the source and destination addresses and makes access decisions based on this type of header information. Characteristics:

- does not require a proxy for each and every service

- does not provide the detailed access control than an application-level proxy firewall provides

- provides security for a wider range of protocols SOCKS is an example of a circuit-level proxy gateway that provides a secure channel between two computers. SOCKS does not provide detailed protocol-specific control. Characteristics:

- circuit-level proxy firewall

- requires clients to be SOCKS-ified with SOCKS client software

- can be resource intensive

- provides authentication and encryption features similar to other VPN protocols, but is not considered a traditional VPN protocol When an internal system needs to communicate to an entity outside of its trusted network, it has to choose a source port, so the receiving system knows how to respond properly. The sender must choose a dynamic port higher than 1024 when it sets up a connection with another entity. The dynamic packet filtering firewall will then create an ACL that allows the external entity to communicate to the internal system via this high port.

A kernel proxy firewall creates dynamic, customized TCP/IP stacks when a packet needs to be evaluated.

The packet is scrutinized at every layer of the stack, not just at the data payload. Kernel proxy firewalls are faster than application layer firewalls because all of the inspection and processing is taking place in the kernel and does not need to be passed up to a higher software layer in the operating system.

The bastion host can be thought of as the “foundation” for the firewall software. It is a locked down system. Any system that resides within the DMZ should be istalled on a bastion host.

A screened host is often a firewall that communicates directly with a perimeter router and the internal network. Traffic that is received from the Internet is first filtered via packet filtering on the outer router.

The traffic that makes it past this phase is sent to the screened-host firewall, which applies more rules to the traffic and drops the denied packets.

A screened-subnet architecture adds another layer of security to the screened-host architecture. In this environment, the firewall is sandiwched between two routers. The external router applies packet filtering to data entering the network and ports the traffic to the firewall. However, instead of the firewall then redirecting the traffic to the internal network, an interior router also filters the traffic.

The default action of any firewall should be to implicitly deny any packets not implicitly allowed.

Any packets entering the network that have a source address of an internal host should be denied. This is a popular attacking trick called masquerading or spoofing.

No trafiic should be allowed to leave a network that does not have an internal source address. Zombies, agents used in distributed DoS attacks, work this way. If packets are leaving a network with different source addresses, these packets are spoofed and the network is most likely being used as an accomplice in a distributed DoS attack.

When security is a top priority for a company, its firewalls should reassemble framented packets before sending them on to their destination.

Source routing means that the packet decides how it is to get to its destination, not the routers in between the source and destination computer.

A honeypot system is a computer that sits in the screened subnet, or DMZ, with the hopes of luring attackers to it instead of to actual production computers. A lega l honeypot can entice attackers to access the computer and attempt to hack into it, but it cannot entrap them.

A network operating system (NOS) is designed to control network resource access and provide the necessary services to enable a computer to interact with the surrounding network. A NOS is built to work in a client/server model that enables resources, files and applications to be centralized.

Services provided by NOS systems:

- directory services

- internetworking, routing and WAN support

- support for remote dial-up users

- clustering functionality

- strong authentication, authorization, access control and auditing

- file and printing services including backup and replication services

- management and administration tools for remote clients

- software distribution, and software and hardware inventory functionality

- fault tolerance capabalities The Domain Name Service (DNS) is a method of resolving hostnames to IP addresses so that names can be used instead of IP addresses when referencing unique hosts on the Internet.

Within DNS servers, networks are split up into zones. One zone may contain all hostnames for the marketing and accounting departments and another zone may contain administration, research and legal departments.

The DNS server that holds the files for one of these zones is said to be the authoritative name server for that particular zone.

The zone files contain records that map hostnames to IP addresses, which are referred to as resource records.

Primary and secondary DNS provides fault tolerance and redundancy to ensure that users can continue to work if something happens to one of these servers.

The naming scheme of the Internet resembles an inverted tree with the root servers at the top. Lower branches of this tree are divided into top-level domains with second-level domains under it.

A directory service has a hierarchical database of user, computers, printers, resources, and attributes of each. The directory is mainly used for lookup operations, which enable users to track down resources and other users easily to facilitate access. Most directory service databases are buld on the X.500 model and use the Lightweight Directory Access Protocol (LDAP) to access the directory database.

Metadata is data about data. Metadirectories hold top-level information about the directory itself.

An intranet is a “private” network that uses Internet technologies, such as TCP/IP.

Private Address Ranges:

- 10.0.0.0                      Class A network

- 172.16.0.0 – 172.31.255.255   16 contiguous Class B networks

- 192.168.0.0 – 192.168.255.255 256 contiguous Class C networks An extranet extends outside the bounds of the company's network to enable two or more companies to share common information and resources.

Network Address Translation (NAT) enables a network that does not follow the Internet's addressing scheme to communicate over the network. NAT is a gateway that lies between a network and the Internet (or another network) that performs transparent routing and address translation.

Most NAT implementations are stateful, meaning they keep track of a communication between the internal host and an external host until that session is ended.

A metropolitan area network (MAN) is usually a backbone that connects LANs to each other and LANs to WANs, the Internet, and telecommunication and cable networks. A majority of today's MANs are Synchronous Optical Network (SONET) or FDDI rings provided by the telecommunication service providers.

SONET is a standard for telecommunication transmissions over fiber-optic cables. SONET is self-healing i.e. if a break occurs on one of its lines, it can use a backup redundant ring to ensure that transmission continues.

Wide area network (WAN) technologies are used when communication needs to travel over a larger geographical area.

Multiplexing is a method of combining multiple channels of data over a single transmission path.

T1 can multiplex upto 24 voice communication calls which yields 1.544Mbps transmission rate. [24 channels * 8 bits + 1 bit (for control) = 193 bits; 193 bits * 8000 frames per second = 1.544Mbps] T3 lines carry up to 28 T1 lines which yields 44.736Mbps.

ATM encapsulates data in fixed cells and can be used to deliver data over the SONET network. ATM uses a fixed cell size, which provides better performance and a reduced overhead for error handling.

OC-1 frames run at a signaling rate of 51.84Mbps, with a throughput of 44.738Mbps.

Europeans chose to use Synchronous Digital Hierarchy (SDH), which supports E1 lines (2.048Mbps) and E3 lines (34.368Mbps).

A dedictated link is also called a leased line or a point-to-point link.

T-carriers are dedicated lines that can carry voice and data information over trunk lines. T1 and T3 lines are the most commonly used T-carriers and are digital circuits that multiplex several individual channels into a higher-speed channel. These lines perform multiplex functionality through time-division multiplexing (TDM).

Secure WAN (S/WAN) was originally an initiative of RSA Security and is based on VPNs that are created with IPSec.

IPSec is a secure tunneling protocol that provides hard-to-break encryption, the option of encrypting the header information and not just the payload data, and incorporates authentication based off of the public-key technology.

A Channel Service Unit/Data Service Unit (CSU/DSU) is required when digital equipment will be used to connect a LAN network to a WA N network. The CSU/DSU provides a digital interface for Data Terminal Equipment (DTE), such as terminals, multiplexers, or routers, and an interface to the Data Circuit-Terminating Equipment (DCE) device, such as a carrier's switch. The CSU/DSU basically works as a translator and sometimes as a line coordinator.

Circuit-switching sets up a virtual connection that acts like a dedicated link between two systems.

Characteristics:

- connection-oriented virtual links

- traffic travels in a predictable and constant manner

- fixed delays

- usually carries voice-oriented data Packet-switching will not set up a dedicated virtual link, and packets from one connection can pass through a number of different individual devices, instead of all of them following one another through the same devices. Examples of packet-switching technologies are the Internet, X.25, and frame relay.

Characteristics:

- packets can use many different dynamic paths to get to the same destination

- traffic is usually bursty in nature

- variable delays

- usually carriers data-oriented data Frame relay is a WAN protocol that operates at the data link layer. It is a WAN solution that uses packet-switching technology that enables multiple companies and networks to share the same WAN media.

Companies that pay more to ensure that a higher level of bandwidth will always be available pay a committed information rate (CIR).

Frame relay connections use two main types of equipment: DTE and DCE. The DTE is usually a customer-owned device, such as a router or switch that provides connectivity between the company's own network and the frame relay network. DCE is the service provider's or telco's device that does the actual data transmission and switching in the frame relay cloud.

Frame relay forwards frames across virtual circuits.

The permanent virtual circuit (PVC) works like a private line for a customer with an agreed-upon bandwidth capability.

The switched virtual circuit (SVC) establishes temporary connections which are torn down once the connections are no longer needed.

X.25, like frame relay, is a switching technology that uses carrier switches to provide connectivity for many different networks. Data is divided into 128 bytes and encapsulated in High-level Data Link Control (HDLC) frames.

Asynchronous Transfer Mode (ATM) is a cell-switching technology. It is a high-speed networking technology used for LAN, WAN and service provider connections. Data is segmented into fixed-size cells of 53 bytes, instead of variable-size packets.

ATM sets up virtual circuits, which act like dedicated paths between the source and destination. These virtual circuits can guarantee bandwidth and QoS, unlike IP. ATM is a good carrier for voice and video transmissions because it promises a bandwidth level and a virtual dedicated path.

Switched Multimegabit Data Service (SMDS) is a high-speed packet-switched technology used to enable customers to extend their LANs across MANs and WANs.

Synchronous Data Link Control (SDLC) protocol is based on networks that use dedicated, leased lines with permanent physical connections. It is used mainly for communication to IBM hosts within a Systems Network Architecture (SNA). It is a bit-oriented , synchronous protocol that has evolved into other communication protocols such as HDLC, Link Access Procedure (LAP) and Link Access Procedure-Balanced (LAPB). SDLC was developed to enable mainframes to communicate with remote locations.

High-Level Data Link Control (HDLC) protocol is also a bit-oriented link layer protocol used for transmission over synchronous lines. HDLC is an extension of SDLC. It provides high throughput because it supports full-duplex transmissions and is used in point-to-point and multipoint connections.

High-Speed Serial Interface (HSSI) is an interface used to connect multiplexers and routers to high-speed communication services such as ATM and frame relay.These interfaces define the electrical and physical interfaces to be used by DTE/DCE devices; thus, it works at the physical layer.

Multiservice access technologies combine several types of communication categories (data, voice and video) over one transmission line.

PSTN – public-switched telephone network Signaling System 7 protocol – helps set up connection, control signaling and tearing down the session Jittering refers to the delay experienced by users when packets holding their voice conversation get queued up somewhere within the network.

H.323 gateways tanslate protocols used on the circuit-based telephone network and the packet-based VoIP network. The gateways also translate the circuits into packets and packets into circuits as required.

Remote access is usually gained by connecting to a network access server (NAS). The NAS acts as a gateway and end point to a PPP session. Then NAS provides authentication and authorization and usually controls a bank of modems.

Wardialing is used by many attackers to identify remote access modems.

Integrated Services Digital Network (ISDN) is a communication protocol that enables data, voice and other types of traffic to travel over a medium, in a digital manner, that was previously used only for analog voice calls.

Basic Rate Interface (BRI) ISDN

- operates over existing copper lines at the local loop and provides digital voice and data channels

- uses two B channels and one D channel with a combined bandwidth of 144Kbps Primary Rate Interface (PRI) ISDN

- has up to 23 B channels and 1 D channel, at 64Kbps per channels

- total bandwidth is equivalent to a T1, which is 1.544Mbps Broadband-ISDN (BISDN)

- this implementation can handle many different types of services at the same time and is mainly used within telecommunication carrier backbones

- when BISDN is used within a backbone, ATM is used to encapsulate data at the data link layer into cells, which travel over a SONET network Analog uses a full channel for communication, but ISDN can break up this channel into multiple channels to provide full-duplex commincation and a higher level of control and error handling.

D channel provides for a quicker call setup and process of making a connection. D channel is an out-of-band communication link between the local loop equipment and the user's terminal. It is out-of-band because the control data is not mixed in with the user communication data.

Digital Subscriber Line (DSL) is a type of high-speed connection that provides 6 to 30 times higher bandwidth speeds than ISDN and analog technologies. DSL is a broadband technology that can provide up to 52Mbps transmission speed without replacing the carrier's copper wire.

Symmetric service refers to the fact that traffic flows at the same speed upstream and downstream.

Asymmetric service refers to the fact that downstream speed is much higher than upstream.

Cable modems also provide high speed access to the Internet, through existing cable coaxial and fiber lines. Cable modem provides upstream and downstream conversions.

A virtual private network (VPN) is a secure, private connection through a public network or an otherwise unsecure environment. It is a private connection because the encryption and tunneling protocols are used to ensure the confidentiality and integrity of the data in transit.

Protocols that can be used for VPNs are Point-to-Point Tunneling Protocol (PPTP), IPSec and L2TP.

A tunnel is a virtual path across a network that delivers packets that are encapsulated and possibly encrypted.

Encapsulation is for enabling routing of packets on various network technologies. E.g. NetBEUI packets must be encapsulated within a routable protocol, such as IP.

Encapsulation and encryption: encapsulation remains the same, but encryption is used to protect the data's confidentiality and integrity as it travels through unsafe environments.

Point-to-Point Protocol (PPP) is used to encapsulate messages and transmit them over a serial line. PPP is used to allow TCP/IP and other protocols to be carried across dial-up lines.

PPP encapsulates the data coming from a computer or network and puts the data into the correct format to travel over the telecommunication link.

PPP has replaced Serial Line Internet Protocol (SLIP) and brings the following features:

- PPP implements header and data compression for efficiency and better use of bandwidth

- PPP has error correction

- PPP supports different authentication methods

- PPP can encapsulate protocols other than just IP

- PPP does not require both ends to have an IP address before data transfer can occur PPTP, a Microsoft protocol, has been the de facto industry standard tunneling protocol for years that has allowed remote users to set up a PPP connection to a local ISP and then create a secure VPN to their destination.

PPP payload is encrypted with Microsoft Point-to-Point Encryption (MPPE) protocol using MS-CHAP or EAP-TLS. The keys used in encrypting this data are generated during the authentication process between the user and the authentication server.

Resulting frame is then encapsulated by PPTP with a Generic Routing Encapsulation (GRE) header and IP header. This encapsulation allows the resulting frame to be routable over public networks, such as in the Internet.

PPTP only works over IP --> led to the formation of L2TP.

L2TP provides the functionality of PPTP, but it can work over networks other than just IP, and it provides a higher level of security when combined with IPSec.

L2TP supports TACACS+ and RADIUS whereas PPTP does not.

Password Authentication Protocol (PAP) is an authentication protocol used by remote users to authenticate over PPP lines.

PAP sends credentials in the clear.

Challenge Handshake Authentication Protocol (CHAP) addresses some of the vulnerabilities found in PAP.

It uses a challenge/response mechanism to authenticate the user instead of sending a password.

A sends logon request to B B sends challenge to A A encrypts challenge value with a predefined password and sends to B B also encrypts challenge value with predefined password and compares both encrypted results A's connection is authorized of failed PAP is vulnerable to sniffing as well as man-in-the-middle attacks. CHAP is not vulnerable to man-in-the-middle attacks because it continues challenge/response activity throughout the connection.

Extensible Authentication Protocol (EAP) is also supported by PPP and is a framework to enable many types of authentication techniques to be used during PPP connections.

A single point of failure can bring a lot of potential risk to a network, because if the device fails, a segment or the entire network is negatively affected.

Redundant array of inexpensive disks (RAID) is a technology used for redundancy and performance improvement. It combines several physical disks and aggregates them into logical arrays .When data is saved, it is written across all drives.

When data is written across all drives, the technique of striping is used. This activity divides and writes the data over several drives. The write performance is not affected, but the read performance is increased dramatically because more than one head is retrieving data at the same time.

Parity data can be written to each disk, which works as a backup. If a drive fails, the parity data is used to rebuild a new drive and all the information is restored.

Hot-swapping disks refer to drives that can be replaced while the system is running.

Failure Resistant Disk Systems – protects against loss of data or access due to a disk failure Failure Tolerant Disk Systems – preotects against loss of data access due to failure of any single component and offers continuous data availability Disaster Tolerant Disk Systems – Two or more zones are used to provide access to stored data.

RAID Level Activity Name 0 Data striped over several drives. No redundancy Striping or parity is involved. If one volume fails, the entire volum is unusable. It is used for performance only.

1 Mirroring of drives. Data is written to two drives at Mirroring once. If one drive fails, the other drive has exact same data available.

2 Data striping over all drives at the bit level. Parity Hamming code parity data is created with a hamming code, which identifies any errors. This level specifies the use of up to 39 disks: 32 for storage and 7 for error recovery data. This is not used in production today.

3 Data striping over all drives and parity data held on Byte-level parity one drive. If a drive fails, it can be reconstructed from parity drive.

4 Same as level 3, except data is striped at the block level Block-level parity instead of the byte level.

5 Data is written in disk sector units to all drives. Parity is Interleave parity written to all drives also, which ensures that there is no single point of failure.

6 Similar to level 5 but with added fault tolerance, which is Second parity data (or a second set of parity data written to all drives. double data) 10 Data is simultaneously mirrored and striped across several Striping and mirroring drives and can support multiple drive failures RAID Level 15 is a combination of RAID Level 1 and RAID Level 5, etc.

Hierarchical Storage Management (HSM) provides continuous online backup functionality. It combines hard disk technology with the cheaper and slower optical or tape juke boxes.

In storage area network (SAN), storage systems are connected together to form a single backup network.

Private channels or storage controllers are implemented so hosts can access the different backup devices transparently.

Clustering is a fault-tolerant server technology that is similar to redundant servers, except each server takes part in processing services that are requested. A server cluster is a group of servers that are viewed logically as one server to users and can be managed as a singly logical system. Clustering provides for availability and scalability.

Spread spectrum means that something is distributing individual signals across the allocated frequencies in some fashion. This allowed for more effective use of the available bandwidth, because the sending system can use more than one frequency at a time.

Frequency Hopping Spread Spectrum (FHSS) takes the total amount of bandwidth and splits it into smaller subchannels. The sender and receiver work at one of these channels for a specific amount of time and then move to another channel. The FHSS algorithm determines the frequency to which the signal will hop and the sender and receiver's hop sequence.

Direct Sequence Spread Spectrum (DSSS) takes a different approach by applying sub-bits to a message.

The sub-bits are used by the sending system to generate a different format of the data before it is transmitted. The receiving end uses these bits to reassemble the signal into the original data format. The sub-bits are collectively called a chip and the sequence of how the sub-bits are applied is referred to as chipping code.

Sender combines data with the chipping sequence, new form of information is modulated with a radio carrier signal and it is shifted to the necessary frequency and transmitted.

Receiver demodulates the data from the carrier signal. Receiver has to know the correct chipping sequence to change the received data into its original format.

Sender and receiver must be properly synchronized.

Sub-bits provide error recovery instructions. This is a benefit of DSSS versus FHSS.

FHSS uses only a portion of the total bandwidth available t any one time, while DSSS technology uses all the available bandwidth continously.

DSSS provides more security because the signals are more difficult to detect from background noise without knowing the specific code.

DSSS is less affected than FHSS by fading and the negative effects of jumping from one path to another.

DSSS spreads the signals over a wider frequency band, whereas FHSS uses a narrow band carrier.

DSSS has a higer data throughput than FHSS.

802.11b – 11Mbps in transfer rates and works in the 2.4GHz frequency range. Uses DSSS and is backward compatible with 802.11 implementations.

802.11a – uses OFDM and works in the 5GHz frequency band. Not backward compatible. Provides up to 54Mbps and does not work in the alread y very crowded 2.4GHz spectrum.

802.11e – provided QoS and proper support of multimedia traffic.

802.11f – deals with the conveying of information between the different access points uring roaming.

802.11g – backward compatible of 802.11b and provides 54Mbps but works in the 2.4GHz range.

802.11h – builds upon 802.11a specification to meet requirements of European wireless rules.

802.11j – bringing together many of the different standards and streamlining their development to allow for better interoperability across borders 802.16 – MAN wireless standard, also known as broadband wireless access.

802.15 – this standard deals with a much smaller georgraphical network, which is referred to as a wireless personal area network (WPAN).

Bluetooth – works in 2.4GHz range and provides data transfer rate of 1-20Mbps.

Wireless Application Protocol (WAP) is a market and industry-driven protocol stack. WAP provides a common architecture for wireless devices to be able to communicate over the Internet. It is a set of communication protocols used to standardize the way that wireless devices interface with each other and the Internet.

WAP has its own session and transaction protocols and transport layer security protocol called Wireless Transport Layer Security (WTLS), which is similar to TLS and SSL.

WTLS classes:

- Class 1 = Anonymous authentication: the wireless device and server do not authenticate to each other.

- Class 2 = Server authentication: the server authenticates to the wireless device.

- Class 3 = Two-way client and server authentication: the server and the client wireless device authenticate to each other.

Wireless device ---> WAP over WTLS ---> WAP gateway ---> HTTP over SSL ---> Web server Infrastructure WLAN – APs are used to bridge wireless and wired networks; used to extend an existing wired network.

Ad hoc WLAN – No APs; wireless devices communicate to each other through their wireless NICs instead of going through a centralized NIC.

A channel is a certain frequency within a given frequency band.

SSID – Service Set ID Open System Authentication (OSA) – wireless device does not have to prove to AP that is has a specific cryptographic key to allow for authentication purposes.

Shared Key Authentication (SKA) – utilizes shared keys for authentication; basis for WEP.

AP will send random value to devices Device will encrypt with its cryptographic key and return to AP AP will decrypt and extract the response If response is same as original value, the device is authenticated
