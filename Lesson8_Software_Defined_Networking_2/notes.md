# Lesson 8 SDN Architecture Part 2
# Revisiting SDN Motivations

### Handling Increasing Complexity and Dynamic Nature of Networks

Implementation of network polies required changes all the way down to individual devices. This was handled 
by each vendor, requiring manual configuration.

There was a lot of overhead managing/maintining these devices. 

Traditional IP networks are far away from automatic response mechanisms to dynamic network environmental
changes.

### Tightly Coupled Architecture

Traditional IP networks had Control Plane and Data Plane bundled together: 
- Control Plane
	- Handles network traffic
- Data Plane
	- Forwards traffic based on control plane decisions

These components are inside the devices and not very accessible. New protocols updated every 10+
years because of the accessiblility.

## Software Defined Networking

Paradigm shift to overcome the limitations of legacy IP networking. 

Begins with separating control logic: control/data planes from eachother. With separation, network 
switches simply forward traffic. Control logic is purley implemented ina logically centralized controller
(or network OS). This allws innovation to occur in areas of the network just by a difference in 
polocy implementation.

Production level SDNs need a physically distributed control plane to achieve performance, reliability, and 
scalability.

Separation of control/data plane was acheived by using a programming interface between the SDN controller 
and the switches. SDN controller control data plane elements via API. Ex: 
- OpenFlow is an API to practice/implement SDN
	- A switch is managed via OpenFlow
	- Has one or more tables for packet handling rules
	- Each rule matches a set of network traffic and performs actions like
		- Dropping
		- Forwarding
		- Modifying
	- OpenFlow can be engineered to implement various technologies like: Firewalls, Switch, Router, Load-
Balancing, etc.

SDN principles allow for a separation of concerns introduced between
- defining network policies
- implementation of hardware
- forwarding table

The separation that allows for networking control problems to be viewed as tractable pieces, 
allowing for newer networking abstractions and simplifying networking management, allowing innovation. 

![Layered view of Networking Functionality](./ImagesLesson8/1.png)


- **Data Plane**
	- Functions and prcoesses that forward data in the form of packets/frames
- **Control Plane**
	- Functions and processes that determine which path to use by using protocols to populate
forwarding tables of data plane elements
- **Management Plane**
	- services that are used to monitor and configure control functionality: SNMP-based tools

If a network policy is defined in the management plane, the control plane enforces the policy and 
the data plane executes the policy by forwarding the data accordingly.

# Quiz 1

### Question 1

In a software defined networking, every device (switch, router, middlebox, etc.) must be able 
to make decisions in the forwarding process.

- True
- False

### Answer

- False

### Question 2

The transition to IPv6 would be faster with a software defined networking paradigm compared to a 
conventional networking paradigm.

- True
- False

### Answer

- True

### Question 3

An OpenFlow switch may also be used for routing.

- True
- False

### Answer

- True

### Question 4

The management plane ___________ a network policy.

- Defines
- Enforces
- Executes
- Ignores

### Answer

- Defines

### Question 5

The control plane ___________ a network policy.

- Defines
- Enforces
- Executes
- Ignores

### Answer 

- Enforces

### Question 6

The data plane ___________ a network policy

- Defines
- Enforces
- Executes
- Ignores

### Answer

- Executes

# SDN Advantages

### Conventional Networks

Tightly coupled data and contorl planes. Making networking components embedded. In order to make updates
or changes, one has to manually updates all control planes on all devices.
	- installing new firmware, version upgrades

To avoid manual updates/installations per device, specialized equiptment was created: Middlebox.
concepts and features like load balancers, IDS, Firewalls were introduced.

Middleboxes were required to carefully placed in network topology, much header to reconfigure afterwards.

### SDN 

SDN decouples control and data places. It isolates itself as an external entity (SDN Controller).
With this, middlebox serices can be viewed as an SDN controller application.
Advantages: 

1. Shared Abstractions
	- middlebox services/functionalities can be programmed easily
	- abstractions controlled by platform and network programming languages, can be shared
2. Consistency of same network infromation
	- all network applications have the same global network information view
	- leading to consistent policy decisions while reusing control plane modules
3. Locality of functionality placement
	- location of middleboxes was strategic and could be a huge constraint during refactor
	- with SDN, middlebox applications can take actions from anywhere in the network
4. Simpler integration
	- integration of networking applications are smoother
	- load balancing and routing applications can be combined sequentally

![SDN Advantages](./ImagesLesson8/2.png)

# Quiz 2

### Question 1

Load balancing is only possible with software defined networking.

- True
- False

### Answer 

- False

### Question 2

In software-defined networking, integrations of networking applications are smoother. 
For example, load balancing and routing applications can be combined sequentially.

Describe a scenario where routing would take precedence over load balancing, and vice versa

### Answer

For example, in a network with high traffic volume and complex routing requirements, 
routing policies may take precedence over load balancing. Conversely, in a network with 
high availability requirements, load balancing may be a higher priority.

### Question 3

In conventional networking, which device can implement an intrusion detection system (IDS)?

- Switches
- Routers
- Middleboxes
- All of the above

### Answer

- Middleboxes

# 
