---
title: MPN data model
description: The Mobile Private Network \(MPN\) data model extends the Telecom data model to represent both the physical hardware and the virtual network functions that make up a mobile private network, along with the relationships that connect them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-service-ops/telecommunications-service-operations-management/mpn-data-model.html
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-06-25"
reading_time_minutes: 7
breadcrumb: [Telecom data model, Explore, Telecommunications Service Operations Management]
---

# MPN data model

The Mobile Private Network \(MPN\) data model extends the Telecom data model to represent both the physical hardware and the virtual network functions that make up a mobile private network, along with the relationships that connect them.

A mobile private network contains a mix of physical and virtual objects. Physical objects include servers, firewalls, routers, switches, antennas, and radio units. Virtual objects include the network functions that run on those servers, such as the User Plane Function \(UPF\) and the Unified Data Management \(UDM\) function, along with their associated licenses. The MPN data model provides dedicated classes and relationships in the Configuration Management Database \(CMDB\) for these objects so that the physical and virtual components of an MPN can be modeled accurately and consistently. Accurate inventory and relationship data enables faster troubleshooting, supports impact analysis when faults occur, and provides the foundation for automated event and performance monitoring across MPN network elements.

The model spans two domains of the mobile network: the Radio Access Network \(RAN\), which connects user equipment to the network over the air interface, and the Mobile Core, which provides packet routing, session management, authentication, and policy control. The model also defines upper‑layer logical objects that group RAN and Core components into end‑to‑end network service instances and assign them to network sites.

## Physical hardware classes

Physical hardware classes represent the tangible equipment deployed in the RAN and the Mobile Core. The following table describes the physical classes used in the MPN data model.

|Domain|Class|Description|
|------|-----|-----------|
|RAN|Remote Radio Unit|Radio frequency unit, typically mounted close to the antenna, that transmits and receives signals over the air interface.|
|RAN|Antenna|Antenna assembly used to radiate and receive signals to and from user equipment.|
|RAN|Baseband Unit|Equipment that processes baseband signals and connects radio units to the transport network.|
|RAN|Baseband Control and Interface Cards|Cards inside a Baseband Unit that provide control plane processing and interfaces to radio and transport networks.|
|RAN|Server|Compute platform that hosts virtualized 5G Distributed Units \(DUs\) and Centralized Units \(CUs\).|
|RAN|BBU chassis \(`cmdb_ci_chassis`\)|Physical enclosure that houses one or more Baseband Units and their interface cards.|
|RAN|Antenna Tower \(`cmdb_ci_antenna_structure`\)|Physical tower structure that supports one or more antennas and their associated radio units.|
|RAN|Indoor Radio Unit \(IRU\) \(`cmdb_ci_indoor_radio_unit`\)|Radio frequency unit deployed indoors to provide cellular coverage inside buildings.|
|RAN|Radio Dot/ Distributed IRU \(`cmdb_ci_distributed_indoor_radio_unit`\)|Distributed indoor radio unit that extends indoor coverage from a central Indoor Radio Unit.|
|RAN and Core|MPN box/ cabinet \(`cmdb_ci_container_cabinet`\)|Outdoor or indoor cabinet that houses the BBU chassis and other RAN equipment at the cell site.|
|RAN|Cable \(`cmdb_ci_cable`\)|Physical cable connection between MPN hardware components.|
|Core|Firewall|Security appliance that enforces traffic policies at the boundaries of the Mobile Core network.|
|Core|IP Router|Layer 3 device that forwards IP traffic between network segments in the Mobile Core.|
|Core|IP Switch|Layer 2 device that forwards traffic between hosts and routers in the Mobile Core.|
|Core|Time sync source|Timing source that provides accurate clock synchronization to the mobile network. Common sources include GPS receivers and other PTP grandmaster clocks.|
|Core|Server|Compute platform that hosts 4G and 5G virtualized network functions \(VNFs\).|
|RAN and Core|Network Adapter|Physical network interface hardware \(cmdb\_ci\_network\_adapter\) installed in a Server, Router, Switch, or Firewall.|
|RAN and Core|Network Interface|Logical interface \(cmdb\_ci\_network\_interface\) exposed by a Network Adapter and used to terminate IP connectivity.|
|RAN and Core|IP Address|IP address \(cmdb\_ci\_ip\_address\) assigned to a Network Adapter or Network Interface and used for routing traffic across the MPN.|

## Virtual network function classes

Virtual network function classes represent the software components that run on the MPN servers. RAN virtual functions handle radio‑side processing, while Core virtual functions provide subscriber, session, and policy services. The following table describes the virtual classes used in the MPN data model.

|Domain|Class|Description|
|------|-----|-----------|
|RAN|Mobile Cell|Logical representation of a radio cell served by a Baseband Unit and its associated radio units.|
|RAN|vDU \(virtual Distributed Unit\)|5G virtual service that performs lower‑layer baseband processing and connects to one or more radio units.|
|RAN|vCU-CP \(virtual Centralized Unit, Control Plane\)|5G virtual service \(cmdb\_ci\_5g\_cu\_control\_plane\_network\_function\) that performs higher-layer control plane processing and signaling between the RAN and the Mobile Core.|
|RAN|vCU-UP \(virtual Centralized Unit, User Plane\)|5G virtual service \(cmdb\_ci\_5g\_cu\_user\_plane\_network\_function\) that performs higher-layer user plane processing and forwards subscriber traffic to the Mobile Core.|
|Core|4G and 5G VNFs|Virtual services that represent Mobile Core network functions. The 5G Core includes nine functions: AMF \(Access and Mobility Management\), AUSF \(Authentication Server\), SMF \(Session Management\), UPF \(User Plane\), UDM \(Unified Data Management\), PCF \(Policy Control\), NRF \(Network Repository\), NEF \(Network Exposure\), and NSSF \(Network Slice Selection\). The 4G EPC \(Evolved Packet Core\) includes six functions: MME \(Mobility Management Entity\), HSS \(Home Subscriber Server\), PCRF \(Policy and Charging Rules\), AAA \(Authentication, Authorization, and Accounting\), SGW \(Serving Gateway\), and PGW \(Packet Data Network Gateway\).|
|Core|VNF license|License assigned to a specific virtual network function. Tracks entitlement and consumption per VNF.|
|RAN|Virtual Machine|Compute instance \(cmdb\_ci\_vm\_object\) that runs on a RAN Server and hosts a vDU or vCU virtual service.|
|Core|Virtual Machine|Compute instance \(cmdb\_ci\_vm\_object\) that runs on a Core Server and hosts a 4G or 5G VNF.|
|Core|IMS network functions|Shared 3GPP network functions \(cmdb\_ci\_network\_function\_instance\) that provide IP Multimedia Subsystem \(IMS\) services for voice and multimedia sessions across 4G and 5G.|
|Core|MPN O&amp;M functions|Operations and management applications \(cmdb\_ci\_app\) such as ProbeApp and Prometheus that monitor and manage the MPN.|

## MPN-specific classes

The MPN data model introduces custom classes that represent assets and resources unique to mobile private networks, including radio spectrum, network slices, data network names, and SIM provisioning. The following table describes the MPN-specific classes used in the MPN data model.

|Class|Description|
|-----|-----------|
|Spectrum|Frequency band \(u\_mpn\_spectrum\) allocated to the mobile private network and consumed by Mobile Cells for radio transmission.|
|SIM range|Block of subscriber identities \(u\_mpn\_sim\_range\) provisioned to the MPN for allocation to SIM cards.|

## Upper‑layer logical classes

Upper‑layer logical classes group the physical and virtual components of an MPN into end‑to‑end service constructs and assign them to a geographic site. The following table describes the upper‑layer logical classes used in the MPN data model.

|Class|Description|
|-----|-----------|
|Network service instance|End‑to‑end logical service that represents an entire MPN deployment, including its RAN and Mobile Core components.|
|Mobile Core network service instance|Logical service that groups the Mobile Core VNFs, supporting hardware, and licenses that deliver core packet, session, and policy functions.|
|RAN network service instance|Logical service that groups the RAN virtual functions, baseband and radio hardware, and Mobile Cells that deliver radio access.|
|Network Site|Physical or logical location to which the MPN network service instance and its components are assigned.|
|Slice|Logical network slice \(u\_mpn\_slice\) that partitions the MPN to deliver tailored connectivity for specific use cases or tenants.|
|DNN|Data Network Name \(u\_mpn\_slice\_dnn\) that identifies the external data network reachable through a slice.|
|SIM card|Individual subscriber identity module \(cmdb\_ci\_sim\_card\) assigned from a SIM range and consumed by user equipment connecting to a Mobile Cell.|

## Relationships between physical and virtual objects

The MPN data model uses CMDB relationships to express how physical equipment hosts virtual functions, how virtual functions consume each other, and how individual components roll up into network service instances and sites. These relationships make dependencies and connectivity visible in the CMDB and support downstream assurance workflows such as fault management, performance monitoring, and impact analysis.

-   RAN servers *Contain* the Virtual Machines that host the vDU and vCU virtual services.
-   Core servers *Contain* the Virtual Machines that host the 4G and 5G VNFs.
-   Baseband Units *Contain* the Baseband Control and Interface Cards, Remote Radio Units, and Antennas.
-   Mobile Cells are *Provided By* the Baseband Unit and its associated radio units.
-   VNF licenses are *Consumed By* the VNFs they entitle.
-   The MPN RAN network service instance and the MPN Mobile Core network service instance are *Contained By* the MPN network service instance.
-   The MPN network service instance and its components are *Located In* an MPN Network Site.

**Related topics**  


[Configure elastic connectors for MPN alarm collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/set-up-connector-instance-nokia-mpn.md)

[Configure elastic event pull connectors for MPN](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/configure-mpn-connectors-for-events-and-metrics.md)

[MPN Formula Engine processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/nokia-mpn-formula-engine.md)

[Metric-to-CI binding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-service-ops/telecommunications-service-operations-management/metric-to-ci-binding-tsom-sgc.md)

