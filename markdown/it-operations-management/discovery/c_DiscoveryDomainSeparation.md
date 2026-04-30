---
title: Domain Separation and Discovery
description: Domain separation is supported in Discovery. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Domain Separation and Discovery

Domain separation is supported in Discovery. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard

-   Includes all aspects of **Basic** level support.
-   Application properties are domain-aware as needed.
-   Business logic: The service provider \(SP\) creates or modifies processes per customer. The use cases reflect proper use of the application by multiple SP customers in a single instance.
-   The instance owner must configure the minimum viable product \(MVP\) business logic and data parameters per tenant as expected for the specific application.

Sample use case: An Admin must be able to make comments required when a record closes for one tenant, but not for another.

For more information on support levels, see [Application support for domain separation](https://www.servicenow.com/docs/access?context=domain-separated-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

## Domain separation overview



Service Providers \(SPs\) use domain separation to segregate data for each customer. Users in a given domain have visibility only to the data in their own domains or in child domains. SPs typically control the top-level domain, which gives them visibility to data associated with all domains. Given that Discovery domain separation support is considered **Standard** there is no delegated administration to the child domains. The SPs must retain administrative control.

## How domain separation works in Discovery

Multiple domains can be supported by a single MID Server. In releases prior to Kingston, each MID Server could support only a single domain. In newer releases, segregating domains by MID Server is useful when the domain is large, or when the domain's resources are held in a customer's data center rather than the SP's. For Discovery on MID Servers supporting a single domain, the discovered CIs are assigned to the domain of the MID User used to authenticated against the ServiceNow instance. In multi-domain MID Servers, the discovered CIs are assigned to the domain of the user who created the Discovery schedule.

Discovery implements data domain separation through the MID Server by impersonating the MID Server user during sensor processing. Discovery uses the domain, that the MID Server user is in, to determine which domain the discovered data should be put into. Discovery configuration information, including classifiers, identifiers, probes, and sensors, is not domain separated.

Service providers generally use IP-based Discovery. In cases where the SP controls the network addressing, they divide the address space among their customers to ensure that each domain has a distinct IP address space. The SP assigns one or more subnets to a customer or domain and creates Discovery schedules for those subnets.

If the SP is remotely managing their customer's data center, there will often be some overlap between address spaces different customers use. In these cases, the SP can use network address translation \(NAT\) on the IP range and run a Discovery schedule.

Once the CIs are assigned to the correct domain, the visibility and read/write access control are provided by the platform through the domain hierarchy. Schedules are visible to users in their respective domains. Cross-domain schedule visibility is not possible, except for the SP who controls the parent domain and has visibility to all domains.

## Domain separation for MID Server files

You can create versions of these specific MID Server policy records that only a MID Server from the same domain can use. This process separation is supported for records in tables that extend MID Server Synchronized Files \[ecc\_agent\_sync\_file\]:

-   MID Server MIB File \[ecc\_agent\_mib\]
-   MID Server JAR File \[ecc\_agent\_jar\]
-   MID Server Script File \[ecc\_agent\_script\_files\]

By default, all records in these tables are members of the global domain. A user can override the default global domain and create a version of these policies for use in the user's own domain.

**Note:** Attachments on MIB or JAR file records might not appear as they did in a non-domain separated environment. The attachments do not appear because the **Attachments** \[sys\_attachment\] table is data separated. When data is separated between domains, a record in a child domain cannot access records in a parent domain.

See [MID Server domain separation](https://www.servicenow.com/docs/access?context=c_MIDServerDomainSeparation&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for instructions on setting up domain separation through the MID Server.

## Domain-separated tables

Records in all tables that extend the Base Configuration Item \[cmdb\] table can be domain-separated. In addition, records in these tables can also be domain-separated:

-   Serial Number \[cmdb\_serial\_number\]
-   TCP Connection \[cmdb\_tcp\]
-   Fibre Channel Initiator \[cmdb\_fc\_initiator\]
-   Fibre Channel Targets \[cmdb\_fc\_target\]
-   IP Address to DNS Name \[cmdb\_ip\_address\_dns\_name\]
-   Service \[cmdb\_ip\_service\_ci\]
-   KVM Virtual Device \[cmdb\_kvm\_device\]
-   Load Balancer Service VLAN \[cmdb\_lb\_service\_vlan\]
-   Load Balancer VLAN Interface \[cmdb\_lb\_vlan\_interface\]
-   Switch Port \[cmdb\_switch\_port\]

-   **[Configure domain-separated Discovery schedules](../task/configure-domain-separated-discovery-schedules.md)**  
Configuring the "Run as" user in a Discovery schedule directs discovered Configuration Items \(CIs\) to the correct domain and maintains data isolation.

**Parent Topic:**[Configuring Discovery](c_DiscoveryConfiguration.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

[Domain separation recommended practices for service providers](https://www.servicenow.com/docs/access?context=bp-domain-sep-recommended&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)

[Discovery behaviors](c_DiscoveryBehaviors.md)

