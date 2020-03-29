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

    R0$ show ip route
    
    Codes: R - RIP
           O - OSPF
           S - Stactic
           U - Per User Static Route
           B - BGP
           i - IS-IS
           * - Candidate Default
           D - EIGRP
           
      R 192.168.2.0/24 [120/2] via 192.168.3.1 00:00:00. Serial0
      |          |       | |           |                      |
      V          |       | |           V                      |
      source of routing info           Next Hop Router        V
                 |       | |                                  Output of interface
                 V       | V
                 Mask    V metrics
                         Distance of Route

(to be continued)
