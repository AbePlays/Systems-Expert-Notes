# Availability

Other than Latency & Throughput, when designing a system one should ponder over the availability of the system.

**Availability** is the percentage of system's uptime throughout a year.

In today’s market everything that is below 99% availability is considered bad, hence in the industry, availability is measured in so-called **nines**. 99 % is a two nines availability, 99.99% is a four numbers availability.

**Highly Available** systems are systems with availability 99.999% and higher.

**Service-level agreement (SLA)** is a collection of agreements between a service provider and customer on system’s availability amongst other things. Ex: ‘we guarantee you **this amount** of availability/uptime’.

**Service-level objective (SLO)** is the guarenteed percentage of uptime. Ex: I guarantee that you’ll have x number of errors when you use my service.

> A SLA consists of a number of SLOs.

**Note:** High availability is very difficult to achieve, hence you need to make trade-offs.
For ex: Stripe has payment service which has to be HA, whilst other parts of the whole system like dashboard for businesses to monitor sales are not required to be HA.

## Ways to ensure the system does not fail

* No single points of failure: if one place fails then whole system should not crash.
* Introduce Redundancy.
* Multiplying certain parts of the system.

Ex of single point of failures: Clients -> Server -> DB.
Here the server is a single point of failure, that’s why adding another server is an option. We can add a **load balancer** between the clients and the servers to distribute the requests. But having only one LB introduces a single point of failure. In order to remedy that, we can add multiple of them.

The solution discussed above is an example of **Passive redundancy**.
If some part goes down(say one of the LBs), then another ones will take the work till first is fixed.

**Active redundancy** is when only particular amount of machines(from a group) handles the operations and if one of them fails(or the group of them), other machines in the system are alerted that something is broken and they reconfigure themselves.

![Key Terminologies](ImageRepo/Availability.png?raw=true)
