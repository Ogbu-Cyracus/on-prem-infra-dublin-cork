                                                                                     # 𝐨𝐧-𝐩𝐫𝐞𝐦-𝐢𝐧𝐟𝐫𝐚-𝐝𝐮𝐛𝐥𝐢𝐧-𝐜𝐨𝐫𝐤
----------------------------------------------------------------------------------------------------------------------------------------------------------------
While preparing for my CompTIA Network+ certification, I decided to simulate and build a multi-site enterprise IT infrastructure in EVE-NG. This project gave me real hands-on experience in switching, routing, and core IT services — and most importantly, helped me understand what’s really happening in Layer 2 (switching) and Layer 3 (routing) of the OSI model.

                 🔧 What I built & learned:

Two Sites (Dublin & Cork) connected via OSPF routing
-----------------------------------------------------
DHCP Design:
-----------
   -- Dublin → DHCP from the Domain Controller using relay (ip-helper) on the L3 gateway
   -- Cork → DHCP handled locally via the router with helper addresses
This setup helped me truly understand how DHCP works across VLANs & sites

DNS Setup:
-----------
  -- Created A records (fileserver, webserver) → to allow users to connect by names, not IPs
  -- Configured Reverse Lookup Zones for IP → hostname mapping
  -- Added CNAMEs for user-friendly aliases (e.g., files, www, intranet)

File Services & GPOs:
--------------------
  -- Instead of multiple drives, I created one partition with departmental folders
  -- Secured them using Active Directory groups + NTFS permissions → ensuring least privilege
  -- Used Group Policy Objects (GPO) to automatically map departmental drives at login (F:, I:, H:)

                             🔑 Key Takeaways:
----------------------------------------------------
  -- VLAN segmentation and inter-VLAN routing improved my understanding of traffic flow & security
  -- OSPF routing gave me a real-world view of multi-site connectivity
  -- DHCP, DNS, and GPOs are the backbone of enterprise networks — now I’ve seen them work together

                              🛡️ Next Step:
I’ll be implementing security policies using my FortiGate firewall and AD hardening. Securing on-prem first is essential — because even as organizations move to the cloud, a weak on-prem environment exposes everything connected to it.
