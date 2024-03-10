# Software Defined Networking (SDN)
### Part 1

# What led us to SDN?

Software Defined Networking (SDN) were created to **make computer networks more programmable**.

Computer Networks are difficult/complex for 2 reasons:

- Diversity of equiptment on networks
- Proprietary technologies for equiptment on said networks

### Diversity of Equiptment

Routers, Switches, Middleboxes: Firewalls, Network Address Translators (NATs), 
Server Load Balancers, Intrusion Detection Systems (IDSs), etc.

Each equiptment may implement separate protocls in order to interact with. Very complex.

### Proproetary Technologies

Routers and Switches tend to run software that is closed source and proprietary.

Configuration interaces vary/differ between vendors. Sometimes they differ from the same vendor.
It is hard to manage these devices in a central mannar.

### Complexity

These characteristics of networks made things complex, slow for innovation, and increased 
operating costs of networks.

**SDN offers a new way to redesign networks to make them more manageable**. It employs a simple idea: 
***separation of tasks*** 

In programming, this can be seen as making modular functions/libraries. Easy to manage individually, 
when combined able to build/design/solve complex problems.

SDN divides the netwrok into two planes: 

- Control Plane
- Data Plane

Separation is used to simplify management and increase innovation speed.

# Quiz 1


### Question 1
The main reason why SDNs were created was because of the increase of internet users. 
  
- True
- False

### Answer 
- False

### Question 2
SDNs divide the network in two planes: control plane and data plane, to ease management and speed up innovation. 

- True
- False

### Answer
- True

---

# History of SDN

The history can be broken into 3 phases:

1. Active Networks
2. Control and Data plan Separation
3. OpenFlow API and Network Operating Systems

## Active Networks

Took place during mid 1990's to early 2000's, the internet grew at a rapid pace during this time. From 
infancy to adolescence.

Researchers were keen on testing new ideas to improve network services. Although these ideas required
standardization of new protocols from the **Internet Engineering Task Force** (IETF).

Active Networking aimed to open up network control. Initially an API was envisioned to expose 
resources/network nodes and supported customization of functionalities for subsets of packets
passing through the network nodes.

The simplicity of the networking core was successful for the internet's success.

in the 1990's networking was primarily IP or ATM (Asynchronous Transfer Mode). Active networking 
became one of the first clean slate approaches to network architecture.

1. Capsule Model
    - Carried in-band data packets
2. programmable Router/Switch Model
    - Established out-of-band mechanisms

Carrying code in data packets brings new data-play functionalities across networks.
Able to use caching to make code distribution more efficient.

### Technology Push

- Reduction in computation cost 
- Advancement in programming languages
    - Platform portability (java), code execution safety and VM tech protect 
    an active node in the instance of bad program/processes
- Advances in rapid code compilation and formal methods.
- Funding from agencies like DARPA (US Defense Advanced Research Projects Agency)

### Use Pull

- Network service provider frustration concerning the long timeline to develop new network services
- Third part interests add value by implementing control at a more individualistic nature.
    - Able to meet dynamic network needs
- Researchers interest in having a network that would support large-scale experimentation
- Unified control over Middleboxes

**Active Networks in the 1990's had similar pull reasons as SDNs now!!!**

1. Programmable functions in the network to lower the barrier of innovation 
    - Early SDN focussed on **Control-Plane**
    - Active Networks focussed on the programmability of **Data-Plane**

2. Network virtualisation and the ability to demultiplex to software programs on packet 
headers
    - Active networking created a framework that described a platform that would support 
    experimentation with different programming models.
    - This lead to network virtualisation

3. The vision of a unified architecture for Middlebox orchestration
    - Unified control over middleboxes never fully came to fruition in the era of Active Networking
    - Network Function Virtualization (NFV) took a lot of influence from Active Networks

### Downfall of Active Networking

One of the largest downfalls of Active Networking is that it was **too ambitions**
Required end users to write Java code, far removed from average IT/Sys/Network Admin. 
Not trusted to be network safe in a lot of cases.

Network architecture has an emphasis on performance and security. Hard for widespread adoption.

## Control and Data Plane Separation

2001 - 2007 

Steady increase in traffic volumes and in turn: network reliability, predictability and performance.
Network Admin were looking for better network management functions like
- control over paths to deliver traffic (traffic engineering)

Researchers began development of short term approaches deploying existing protocols

### Technology Push

- Higher link speeds in backbone networks led vendors implement **packet forwarding directly in hardware**
separating it from the **control-plane software**.
- Internet Service Providers (ISPs) found it hard to meet the demands for greater reliability
and new services (like VPNs)
- Servers had substantially more memory an processing power than just 1-2 years ago
    - A single server could store all routing states and compute all routing decisions for a large ISP 
    network
- Open source routing software lowered the barrier to creating prototype implementation of centralized 
routing controllers

#### Pushes Inspired 2 Innovations

1. Open interface between control and data planes
2. Logically centralized control of the network

#### Different from Active Networking in 3 Ways

1. Focused on spurring innovation by and for networking admins rather than end users and Researchers
2. Emphasised programmability in the control domain rather than data domain
3. Worked towards network wide visibility and control rather than device level configurations

### Use Pulls 

- Selecting between network paths based on the current traffic load 
- Minimizing distributions during planned routing changes
- Redirecting/dropping suspected attack traffic 
- Allowing customer networks more control over traffic flow 
- Offering value added services for VPN customers 
