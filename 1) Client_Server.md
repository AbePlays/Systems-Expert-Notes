# Client-Server Architecture

**Client - Server**
[Browser] - [Google]

A Client is a machine which sends request to the server. A Server is a machine that responds to the client with the result.

**Note:** A machine can have both roles simultaneously when being a server to the browser, it can be a client to the database.

When you type www.google.com, the browser makes a **DNS** query to find the **IP** address of the aforementioned site.

A **DNS(Domain Name System)** query is a special request that goes to a predetermined list of servers and requests the IP address of the desired site.

An **IP** address is a unique identifier provied to a machine.

After the browser has received the response with the **IP** address, it sends an **HTTP** request to this **IP** address. It sends a bunch of bytes (characters) in packets with the source address of the request (IP address of your browser/computer).

Servers are machines which listen to requests from other machines on **ports**. So, the client has to specify which port it wants to communicate on.
However, there are predefined ports which some protocols have:

- HTTP: 80
- HTTPS: 443
- DNS: 53
- Secure Shell: 22

After a server has received a request, using the data sent along the request, it understands what client has requested and responds back with the result.

**IP address** is an address of a system in the Network.
**Port** is an address of the service within the System.
So IP address + Port defines address of a particular service on a particular system.

![Key Terminologies](ImageRepo/Client_Server_first.png?raw=true)
