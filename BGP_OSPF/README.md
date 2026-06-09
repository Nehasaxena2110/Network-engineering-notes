1. BGP Neighbor Not Coming Up

Two routers are configured as BGP neighbors, but the session remains in Idle state.

👉 What would you check first?

🔥 2. Route Not Being Advertised

You configured a network statement in BGP, but the prefix is not appearing on the peer router.

👉 Why might BGP not advertise the route?

🔥 3. Multiple ISPs

A company is connected to ISP-A and ISP-B.

👉 How would you make ISP-A the preferred outbound path while keeping ISP-B as backup?

🔥 4. eBGP Multihop

Two BGP routers are not directly connected and there is one router in between.

👉 What configuration is required to establish BGP neighborship?

🔥 5. Route Selection

Router learns the same prefix from two BGP peers.

One path:

Local Preference = 200

Second path:

Local Preference = 100

👉 Which path will be selected and why?

🔥 6. BGP Flapping

BGP session goes up and down every few minutes.

👉 What troubleshooting steps would you perform?

🔥 7. Route Received But Not Installed

You can see the route in:

show ip bgp

but not in:

show ip route

👉 Why?

🔥 8. AS Path Manipulation

Your company wants inbound traffic to prefer ISP-A instead of ISP-B.

👉 Which BGP attribute can be manipulated to influence inbound traffic?

🔥 9. Loop Prevention

Why doesn't BGP create routing loops between autonomous systems?

👉 What mechanism prevents loops?

🔥 🔟 Data Center VXLAN EVPN Scenario

Two VTEPs are exchanging MAC/IP routes using BGP EVPN.

Suddenly hosts in one VXLAN segment cannot reach hosts on another leaf.

👉 What BGP-related checks would you perform?

🎯 Bonus "Oracle / Data Center" Questions
Q11

Difference between:

iBGP
eBGP
Q12

Why do we need Route Reflectors?

Q13

What is the purpose of Next-Hop-Self?

Q14

Why is full-mesh iBGP not scalable?

Q15

What is the order of BGP best-path selection?

🔥 The 5 Most Important BGP Topics to Master
Neighbor Formation
Route Advertisement
Best Path Selection
Attributes (Weight, Local Pref, AS Path, MED)
eBGP vs iBGP
1. OSPF Neighbor Not Forming

Two routers are directly connected but are stuck in INIT or EXSTART state.

👉 What would you check?

🔥 2. OSPF Route Missing

Routers are neighbors and adjacency is FULL.

However, a remote network is not appearing in the routing table.

👉 What could be the reason?

🔥 3. DR/BDR Election

On a broadcast network with 10 routers, a newly added router has the highest priority.

👉 Will it automatically become the DR?

🔥 4. Area Mismatch

Two routers are connected and can ping each other.

OSPF neighbors are not forming.

👉 What OSPF parameter mismatch would you check first?

🔥 5. MTU Mismatch

OSPF neighbors are stuck in EXSTART/EXCHANGE.

👉 What Layer 3 issue could cause this?

🔥 6. Network Type Mismatch

One side is configured as Broadcast and the other as Point-to-Point.

👉 What impact could this have on OSPF?

🔥 7. OSPF Path Selection

A router learns two OSPF paths to the same destination:

Path A Cost = 20
Path B Cost = 40

👉 Which path will be selected?

🔥 8. Equal-Cost Paths

OSPF learns two routes to the same network:

Both Cost = 10

👉 What will OSPF do?

🔥 9. Backbone Area Issue

A company has:

Area 1 ---- Area 2

but no Area 0.

👉 What design issue exists?

🔥 🔟 OSPF Flapping

OSPF adjacency goes up and down every few minutes.

👉 What would you troubleshoot?

🎯 Bonus Data Center / Senior-Level Questions
Q11

Why is Area 0 mandatory in OSPF?

Q12

Difference between:

Internal Route
Inter-Area Route
External Route
Q13

When would you use a Stub Area?

Q14

What is a Totally Stubby Area?

Q15

What is an NSSA Area?

🔥 Top OSPF Neighbor States (Interview Favorite)
Down
Init
2-Way
ExStart
Exchange
Loading
Full

Common question:
👉 "Neighbor stuck in EXSTART. What do you check?"

🔥 Top OSPF Commands
show ip ospf neighbor
show ip ospf interface
show ip ospf database
show ip route ospf
show ip protocols
🎯 The 5 Most Important OSPF Topics
Neighbor Formation Process
DR/BDR Election
Area Design (Area 0, Stub, NSSA)
Cost & Path Selection
OSPF Troubleshooting (MTU, Area, Hello/Dead, Authentication)






