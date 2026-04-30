---
title: Software asset connections
description: Use third-party discovery sources to discover the installed software data that you can integrate with the Software Asset Management application.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# Software asset connections

Use third-party discovery sources to discover the installed software data that you can integrate with the Software Asset Management application.

The discovery process is an integral part of the Software Asset Management application. The discovery process consists of discovering where the installed software in your organization is installed, who the owner of the device is, and where it's located. The discovered information is then merged into a common configuration management database such as the CMDB application.

The CMDB application enables other business applications to use the discovered information to support various business needs.

![Third-party discovery sources](../image/third-party-sources.png "Discovery with Software Asset Management")

ServiceNow platform's identification and reconciliation engine \(IRE\) framework enables all third-party data integrations with the CMDB application.

IRE provides a centralized framework where you can perform reconciliations and de-duplication of the data when multiple sources are ingesting data at the same time. IRE uses identification rules, reconciliation rules, and IRE data source rules to process the incoming data and then inserts the data into the corresponding CMDB tables. You can extend these rules to insert the data into tables that extend the CMDB core tables such as the Software Asset Management tables. There are two types of identification rules for IRE:

-   Independent: If the **Independent** check box is selected on a CI identifier, it means that the CI is not dependent on any other CI.
-   Dependent: If the **Independent** check box is not selected on a CI identifier, it implies that this CI is dependent on other CIs.

For more information on IRE, see [Identification and Reconciliation Engine](https://www.servicenow.com/docs/access?context=ire&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

You should have already configured loading the CIs in the ServiceNow instance. For each CI in your environment, the Hardware \[cmdb\_ci\_hardware\] table has a corresponding CI identifier rule. When the third-party discovery application runs, the software is identified on CIs. The third-party application constructs a payload and sends the payload via the IRE REST API endpoint to the ServiceNow instance to insert or update data into the Software Asset Management tables.

A [generic payload](../reference/payload-details.md) is used for creating installed software records. For Oracle, VMware, and Citrix, specific payloads feed additional publisher-specific data apart from software installations.

If multiple discovery sources are enabled and if the key details of the software, such as the display name and the version for all discovery sources, match, the Installation record is overwritten. If multiple discovery sources identify the same software with different field values, an entry is created in the Software Installation \[cmdb\_sam\_sw\_install\] table. When the schedule job **SAM- Deduplication install table** runs and if all the normalized values of these installations match, only one record is set to active. The rest of the records are marked as inactive.

Domain separation is supported for third-party discovery with SAM with the following considerations:

-   The IRE REST API stamps the domain that you are logged in to when the REST call is made.
-   Log in to the domain where the CI resides and from where you run the payload.
-   Don't log in to the parent domain. Being logged in the parent domain updates the existing CI and also creates a new CI in the parent domain.
-   Send the payload from the same domain where the CIs reside. For example, if you send a payload from Domain A and if the payload has CIs that belong to Domain B, a new CI gets created in Domain A.

-   **[Configure third-party discovery sources for Software Asset Management](../task/configure-third-party-discovery.md)**  
Set up a third-party discovery source for Software Asset Management to populate the Software Installation \[cmdb\_sam\_sw\_install\] table with software found in your environment.
-   **[Delete uninstalled software from the Software Installation table](../task/delete-disco-entries-sam.md)**  
Delete installations from the Software Installation \[cmdb\_sam\_sw\_install\] table if those software installations are also uninstalled from a CI.
-   **[Sample payload for generic software install records](../reference/payload-details.md)**  
A sample payload that populates the Software Installation \[cmdb\_sam\_sw\_install\] table in the ServiceNow instance with discovery data collected by third-party discovery sources.
-   **[Sample payload for Oracle software install records](../reference/payload-oracle.md)**  
A sample payload for Oracle publisher pack that populates the Oracle Instance \[cmdb\_ci\_db\_ora\_instance\] table with software install records from third-party discovery sources.
-   **[Sample payload for VMware software install records](../reference/payload-vmware.md)**  
A sample payload for VMware publisher pack that populates the VMware Discovered License key consumption \[samp\_vmware\_license\_key\_usage\] table with software install records from third-party discovery sources.
-   **[Sample payload for Citrix software install records](../reference/payload-citrix.md)**  
A sample payload for the Citrix publisher pack that populates the Software Installation \[cmdb\_sam\_sw\_\_install\] table with software install records from third-party discovery sources.
-   **[Sample payload for BYOL](../reference/sample-payload-byol.md)**  
A sample payload that populates the Software Installation \[cmdb\_sam\_sw\_install\] table in the ServiceNow instance with discovery data collected by the BYOL licensing model.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

