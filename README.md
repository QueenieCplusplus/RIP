# RIP

Routing Information Protocol

* cmd:

> show ip route

* config:

> Mask, Prefix Format

> Basic

> its metrics & timer

* GW:

> Candidate Default Routes & GW of Last Resort

* routing table:

> its Content & Update Process

> Unicast Routing Updates

* so on:

> LB

> NBMA

------------------------------------------------------------------------
# Show IP Route

the cmd is used to display the routing table of cisco router. And this routing table only contains static and connected routes, so the output of show ip route cmd is simple.

There are 3 sources of routing information:

* Static
* Dynamic
* Connected

And the "Gateway at last resort is not set" denotes the default router that the router shall use if it receive a datagram destined for an IP addr for which it does not have any route.

    R0$ show ip route
    
    
        Codes: R - RIP
               O - OSPF
               S - Stactic
               U - Per User Static Route
               B - BGP
               i - IS-IS
               * - Candidate Default
               D - EIGRP
           
        Gateway at last resort is not set
           
          R 192.168.2.0/24 [120/2] via 192.168.3.1 00:00:00. Serial0
          |          |       | |           |                      |
          V          |       | |           V                      |
          source of routing info           Next Hop Router        V
                     |       | |                                  Output of interface
                     V       | V
                     Mask    V metrics
                             Distance of Route
                         

(to be continued)
