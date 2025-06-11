### Devices
#### Router
- **Router**: Allows us to route data from one IP subnet to another IP subnet
- OSI layer 3
-  Its primary role is to determine the best path for data to travel from its source to its destination across multiple networks

#### Hub
- Connects Multiple Ethernet devices together, making them act as a single network segement
- OSI layer 1(Phyical Layer)
- Its simple broadcast the packet it recieved into the network

#### Switch
- Switch is more efficient and intelligent device  then Hub
- It connects multiple devices withing the Local Area network and direct traffic only to intendet devices
- Operates at layer 2 (data Link layer)
- It store MAC address of the devices and When it recieves a packet , it simply direct the packet to the destination MAC address, if MAC address is not present in the stored memory , then it simple broadcast that and then learn the address when it replies

#### Firewall
- A firewall is a network security device (hardware or software) that monitors and controls incoming and outgoing network traffic based on predetermined security rules.
- ts primary purpose is to establish a barrier between a trusted internal network and untrusted external networks (like the internet).
- It inspects data packets and decides whether to allow them to pass or block them, based on rules defined by an administrator
- These rules can be based on IP addresses, port numbers, protocols, application types, and even content.
- OSI Layer 3

#### WAP (Wirelesss Access Points)
- A WAP allows wireless devices to connect to a wired network
- OSI layer 2
- converting wireless signals into wired Ethernet signals and vice-versa.

#### Modem 
- A modem (modulator-demodulator) is a device that converts digital signals from a computer into analog signals that can be transmitted over traditional phone lines, coaxial cables, or fiber optic lines, and vice-versa


#### Repeater
- A repeater is a basic network device that regenerates and retransmits network signals
- Its purpose is to extend the range of a network by boosting the signal strength, overcoming attenuation (signal loss over distance).
- Operates at Layer 1 of the OSI model (Physical Layer)

#### Bridge
- A bridge connects two or more network segments and filters traffic between them based on MAC addresses
- It's more intelligent than a repeater but less intelligent than a router.
- Operates at Layer 2 of the OSI model (Data Link Layer)
- It learns MAC addresses and forwards frames only to the segment where the destination MAC address resides.

#### Load Balancer
- Devices help balaning load by distributing it across the server on different nodes
- Protocol Overhead
- Helps Encryption/Decryption
- Fast response using cache
- Content Switiching : Application centric balancing
  
#### Proxy 
- Sits between user and the external network
- Recieves the user request and send the request on behalf of the user
- Useful for caching info , access control, URL filtering , content scanning
- Application may need to know how to use the proxy
- Some proxies are invisible

#### NAS(Network Attached Storage)
- Connect to shared storage devices across the network
- File Level access

#### SAN(Storage Area Network) 
- Looks and feels like local area storage
- Block level access
- Very efficient reading and writing
- Requires lot of bandwidth 
- May uses  an isolated network  and high speed network technology 

