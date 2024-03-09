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

### Active Networks

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

      


