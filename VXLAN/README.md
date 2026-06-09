# VXLAN Notes

1. Users in VLAN 10 cannot communicate across two switches
Topology
PC1 -- SW1 ===== SW2 -- PC2
      VLAN10   VLAN10
What will you check?

✔ VLAN 10 exists on both switches

show vlan brief

✔ Ports are assigned to VLAN 10

✔ Trunk is up

show interfaces trunk

✔ VLAN 10 is allowed on trunk

✔ STP is not blocking the path

✔ MAC addresses are being learned

Interview Answer

"I would verify VLAN existence, access-port assignment, trunk status, allowed VLANs, and spanning-tree status."

🔥 2. Native VLAN Mismatch on Trunk
Scenario

SW1:

switchport trunk native vlan 10

SW2:

switchport trunk native vlan 20
What happens?

✔ Untagged traffic enters wrong VLAN

✔ VLAN leakage

✔ Possible STP issues

✔ CDP warning:

Native VLAN mismatch detected
Interview Answer

"A native VLAN mismatch causes untagged traffic to be placed into different VLANs on each side of the trunk, leading to connectivity and security issues."

🔥 3. New VLAN Created But Users Have No Connectivity
Scenario

VLAN 30 was created yesterday.

Users still cannot communicate.

Checks

✔ Is VLAN created?

✔ Are ports assigned?

✔ Is VLAN 30 allowed on trunks?

✔ Is the SVI up (if using Layer 3 switch)?

show ip interface brief
Interview Answer

"The most common issue is that the VLAN exists locally but has not been allowed across trunk links."

🔥 4. VLAN Traffic Not Crossing Trunk
Scenario

VLAN 50 works on Switch A but not on Switch B.

Common Cause
switchport trunk allowed vlan 10,20,30

VLAN 50 missing from allowed list.

Verification
show interfaces trunk
Interview Answer

"I would verify that the VLAN is included in the allowed VLAN list on all trunk links."

🔥 5. Hosts in Different VLANs Cannot Communicate
Scenario

PC1 → VLAN 10

PC2 → VLAN 20

Same switch.

Why?

Because VLANs are separate broadcast domains.

Need:

✔ Inter-VLAN routing

Examples:

Layer 3 Switch SVI
Router-on-a-Stick
Interview Answer

"Communication between VLANs requires a Layer 3 device because VLANs are isolated Layer 2 domains."

🔥 6. One Side Trunk, Other Side Access
Scenario

SW1:

switchport mode trunk

SW2:

switchport mode access
Symptoms

✔ VLAN mismatch

✔ Some traffic works unexpectedly

✔ Connectivity issues

Verification
show interfaces switchport
Interview Answer

"I would verify both ends of the link are configured consistently as either trunk or access."

🔥 7. After Adding a New Switch, Some VLANs Stop Working
Scenario

A new switch is inserted between two existing switches.

Checks

✔ Trunk configured?

✔ VLANs allowed?

✔ VTP issue?

✔ STP blocking?

✔ Native VLAN mismatch?

Commands
show interfaces trunk
show vlan brief
show spanning-tree
show vtp status
Interview Answer

"I would first verify trunking and VLAN propagation, then check spanning-tree and VTP consistency."

🎯 Interview Cheat Sheet
Scenario	Most Likely Cause
Same VLAN across switches not working	Trunk/VLAN allowed issue
Native VLAN mismatch	Untagged traffic problem
New VLAN not working	Not allowed on trunk
Different VLANs can't communicate	Missing L3 routing
One side trunk, one side access	Port mode mismatch
VLAN works locally only	Trunk issue
VLAN stopped after new switch added	Trunk/VTP/STP issue

These 7 scenarios cover roughly 80% of VLAN troubleshooting questions asked in network engineer interviews.
