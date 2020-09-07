
### Router Forward Tables (Flags)

Router forwarding tables contain 3 bits for flags. These are the U(p), G(ateway) and H(ost) flags. The falgs have the following meanings:
 - U: The route is up. In other words the interface this route egresses from is up and functional.
 - G: This is a gateway route. This means that the network this entry in the routing table is trying to reach is not directly connected to the router. 
      Instead the destination is just the next hop router on the route.
 - H: This is used for routes to specific host. In other words routes to destinations with the /32 suffix (e.g. 10.80.160.1/32)
 
 As an example the flags __UGH__ indicate that the route is up, that we are trying to send a packet to a specific host and that the host is 
 not on a network directly attached to the router and will need to be forwarded to the next hop router.
 
 ### IPv4 braodcasts
 
 There are two types of IPv4 broadcasting. 
  1. __Directed Broadcasting__ is when we want to broadcast a packet to every host on a specific network. 
  2. __Limited Broadcasting__ is when we want to broadcast a packet to every host on the network we are currently on.
  
  A directed broadcast to every host on the network 192.168.4.0/24 would use a destination address of 192.168.4.255.
  A limited broadcast always uses the destination address 255.255.255.255. This will send the packet to every other host on the local network.
