# What the OSI model is:
Open Systems Interconnection (OSI) model
The OSI model is a conceptual framework that is used to describe how a network functions. In plain English,
 the OSI model helped standardize the way computer systems send information to each other.

## layer: 
A layer is a way of categorizing and grouping functionality and behavior on and of a network.

Each layer abstracts lower level functionality away until by the time you get to the highest layer. All the details and inner workings of all the other layers are hidden from the end user.
The problems that can happen at each of the 7 layers:
## layer1
Defunct cables, for example damaged wires or broken connectors
Broken hardware network devices, for example damaged circuits
Stuff being unplugged (...we’ve all been there)
## layer2
All the problems that can occur on Layer 1
Unsuccessful connections (sessions) between two nodes
Sessions that are successfully established but intermittently fail
Frame collisions
## layer3
All the problems that can crop up on previous layers 
Faulty or non-functional router or other node
IP address is incorrectly configured
## layer4
All the problems that can crop up on previous layers 
Blocked ports - check your Access Control Lists (ACL) & firewalls
Quality of Service (QoS) settings. QoS is a feature of routers/switches that can prioritize traffic,
and they can really muck things up.
## layer5
Servers are unavailable
Servers are incorrectly configured, for example Apache or PHP configs
Session failure - disconnect, timeout, and so on.
## layer6
Non-existent or corrupted drivers
Incorrect OS user access level
## layer7
All issues on previous layers
Incorrectly configured software applications
User error

# The difference between TCP/IP model and the OSI model:
In the OSI model, layers are organized from the most tangible and most physical,
to less tangible and less physical but closer to the end user.

TCP explicitly establishes a connection with the destination node and requires a handshake
between the source and destination nodes when data is transmitted. The handshake confirms that data was received.
If the destination node does not receive all of the data, TCP will ask for a retry.

TCP also ensures that packets are delivered or reassembled in the correct order.

# Socket.IO

Socket.IO is a library that enables low-latency, bidirectional and event-based communication between a client and a server.
Socket.IO is NOT a WebSocket implementation.

Although Socket.IO indeed uses WebSocket for transport when possible, it adds additional metadata to each packet.
That is why a WebSocket client will not be able to successfully connect to a Socket.IO server,
and a Socket.IO client will not be able to connect to a plain WebSocket server either.
