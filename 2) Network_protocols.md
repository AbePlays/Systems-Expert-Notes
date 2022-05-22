# Network Protocols

**IP** stands for Internet Protocol. It defines how machines communicate with each other. The modern internet operates using IP.

**IP Packet** is an unit of data that is sent from one machine to another. It is the building block of communication between machines.

IP packet consists of a header and data.

Header contains info about the packet: *source IP address, destination IP address, total size of the packet, version of the IP*

**Data**(payload): The size of an IP Packet is very small(~65KB). Hence multiple IP Packets are sent to deliver the entire data but there is a risk that some of the packets may be lost during the transfer over the network. This is where TCP comes into play. It allows the machine to send multiple IP packets and ensures that they are all delivered.

**TCP** stands for Transmission Control Protocol. It is built on top of IP.
It ensures that packets are:

* sent in an ordered way
* sent in a reliable way
* delivered error free

**TCP header** goes after IP header in that same IP packet.

When machine wants to communicate with one another over TCP (i.e. browser wants to communicate with website server), it:

* Creates connection with destination server via **TCP handshake** by sending a couple of packets.
* After the connection has been established, data can be sent between them.

> One machine can end connection via special command. A connection can end due to time out (no response from one of the sides). But it’s difficult for developers to communicate with TCP w/o any use of robust framework. This is where **HTTP** appears.

**HTTP** stands for Hyper Text Transfer Protocol. It is an abstraction above IP & TCP.
It introduces the idea of machines communicating in Client-Server manner.

## HTTP Verbs Mapping

| HTTP VERB     | CRUD          |
| ------------- | ------------- |
| GET           | READ          |
| POST          | CREATE        |
| PUT, PATCH    | UPDATE        |
| DELETE        | DELETE        |

**Headers** - a collection of key-value pairs which comprises essential metadata about the request.
**Body** - data that is sent in the request(key-value pair also).

A response can have status *code/ headers/ body*

**In a nutshell:** HTTP is the one that allows developers to create business logic and interact with data.

![Key Terminologies](ImageRepo/Network_Protocols_first.png?raw=true)
![Sample request and response structure](ImageRepo/Network_Protocols_second.png?raw=true)
![Express code](ImageRepo/Network_Protocols_third.png?raw=true)
