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

If you can answer those well, you're already ahead of many interview candidates. 🚀
