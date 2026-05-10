---
title: Discovery for Alibaba Cloud
description: Alibaba Cloud discovery is one of the overall Cloud discovery offerings within the IT Operations Management \(ITOM\) Visibility framework. It’s an automated process used to scan and identify Alibaba Cloud resources within your organization's cloud infrastructure. This discovery process is critical for maintaining an accurate and trustworthy data foundation—the Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
keywords: [Alibaba, cloud, Discovery, Service Mapping, Patterns, CMDB]
breadcrumb: [Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Discovery for Alibaba Cloud

Alibaba Cloud discovery is one of the overall Cloud discovery offerings within the IT Operations Management \(ITOM\) Visibility framework. It’s an automated process used to scan and identify Alibaba Cloud resources within your organization's cloud infrastructure. This discovery process is critical for maintaining an accurate and trustworthy data foundation—the Configuration Management Database \(CMDB\).

## Pattern-based cloud discovery

Using Discovery and Service Mapping Patterns to perform horizontal discovery enables you to find and map your organization's Alibaba Cloud resources. You can discover Alibaba Cloud metadata including:

-   Cloud service accounts.
-   Datacenters.
-   Availability zones.
-   Hardware types.

Patterns also support OS level discovery, for example OS images.

Discovery and Service Mapping Patterns create configuration items \(CIs\) for your Alibaba Cloud resources. Additionally, patterns discover the relationships between your organization's Alibaba Cloud resources, such as Hosted On :: Hosts.

See [Alibaba Cloud discovery using patterns](../../service-mapping/concept/alibaba-cloud-discovery-pattern.md) to learn about all Alibaba Cloud resources you can discover using Patterns.

## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Alibaba Cloud discovery configuration

The basic steps to configure pattern-based discovery for Alibaba Cloud involve preparation on the ServiceNow AI Platform side like installing necessary plugins and setting up credentials. The discovery\_admin role in ServiceNow AI Platform is required for creating Alibaba Cloud API credentials and service accounts.

The discovery process requires configuration within Alibaba Cloud, like setting up Identity and Access Management roles. The discovery permissions of Alibaba Cloud users are determined by their access levels within Alibaba Cloud.

To promote proper discovery, the Alibaba Cloud user must have at least read-only access to the necessary Alibaba Cloud services.

|Alibaba Cloud user|Discovery permissions|
|------------------|---------------------|
|Root Account \(Master Account\)|Full access to all Alibaba Cloud resources and services, including Elastic Compute Service \(ECS\), Object Storage Service \(OSS\), Relational Database Service \(RDS\), and Resource Access Management \(RAM\). Can create and manage RAM users, assign permissions, and perform billing operations.|
|RAM user|Access to specific Alibaba Cloud resources and services based on assigned policies. Can be granted read-only access for discovery purposes.|
|RAM Role \(AssumedRoleUser\)|Temporary access to Alibaba Cloud resources and services based on assumed role policies. Useful for cross-account access, temporary access, or access by ECS instances.|

<table><thead><tr><th>

Typical persona

</th><th>

Roles and permissions

</th><th>

Responsibility

</th><th>

Link to detailed documentation

</th></tr></thead><tbody><tr><td>

ServiceNow administrator or IT Implementation Specialist

</td><td>

admin

</td><td>

Install the store applications and update them on every store release:-   Discovery
-   Discovery and Service Mapping Patterns
-   Visibility content.
-   CMDB CI Class Models
-   Discovery Admin Workspace

</td><td>

[ITOM Store upgrades](store-upgrades-landing.md)

</td></tr><tr><td>

ServiceNow administrator

</td><td>

admin

</td><td>

-   Create a MID Server user.
-   Assign the MID Server role to the user.

</td><td>

[Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_SetupMIDServerRole.md)

</td></tr><tr><td>

ServiceNow administrator

</td><td>

admin, mid\_server

</td><td>

Install a MID Server.

</td><td>

-   [Install a MID Server on Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_InstallAMIDServerOnLinux.md)
-   [Install a MID Server on Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-install-prereqs.md)
-   [Install and configure MID Servers to access cloud environments](../../it-operations-management/task/mid-server-configuration-cloud.md)

</td></tr><tr><td>

ServiceNow administrator

</td><td>

admin

</td><td>

Validate that the MID Server is installed correctly.

</td><td>

[Validate the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_ValidateAMIDServer.md)

</td></tr><tr><td>

ServiceNow administrator

</td><td>

admin

</td><td>

Assigning users with discovery\_admin roles and giving them permission for discovery.

</td><td>

[Managing roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/user-administration/ua-creating-roles.md)

</td></tr><tr><td>

Cloud administrator or Discovery administrator

</td><td>

discovery\_admin

</td><td>

Creating Alibaba Cloud service accounts

</td><td>

[Set up Alibaba Cloud service accounts](../task/set-up-alibaba-cloud-service-account.md)

</td></tr><tr><td>

Cloud administrator or Discovery administrator

</td><td>

The person configuring the API credentials must have the discovery\_admin role in ServiceNow and must have access to the Alibaba Cloud **Access Key ID** and **Access Key Secret**.

</td><td>

Configuring Alibaba Cloud API credentials

</td><td>

[Create Alibaba Cloud API Credentials](../task/create-alibaba-cloud-api-credentials.md)

</td></tr><tr><td>

Discovery administrator

</td><td>

discovery\_admin

</td><td>

Use Discovery and Service Mapping Patterns

</td><td>

[Alibaba Cloud discovery using patterns](../../service-mapping/concept/alibaba-cloud-discovery-pattern.md)

</td></tr><tr><td>

Discovery administrator

</td><td>

discovery\_admin

</td><td>

Set up a discovery schedule for Alibaba Cloud

</td><td>

-   [Create a Discovery schedule for Alibaba Cloud](../task/create-alibaba-cloud-discovery-schedule.md)
-   [Create an Alibaba Cloud Discovery schedule in Discovery Admin Workspace](../task/create-alibaba-schedule-DAW.md)

</td></tr></tbody>
</table>-   **[Create Alibaba Cloud API Credentials](../task/create-alibaba-cloud-api-credentials.md)**  
Create Alibaba Cloud API credentials on the ServiceNow AI Platform to enable access to your Alibaba Cloud resources during Alibaba Cloud discovery.
-   **[Set up Alibaba Cloud service accounts](../task/set-up-alibaba-cloud-service-account.md)**  
Create Alibaba Cloud infrastructure service accounts on the ServiceNow AI Platform to access your Alibaba Cloud account during Alibaba Cloud discovery.
-   **[Create a Discovery schedule for Alibaba Cloud](../task/create-alibaba-cloud-discovery-schedule.md)**  
Create a Discovery schedule to run Alibaba Cloud discovery.
-   **[Create an Alibaba Cloud Discovery schedule in Discovery Admin Workspace](../task/create-alibaba-schedule-DAW.md)**  
Use the Discovery Admin Workspace dashboard to create an Alibaba Cloud Discovery schedule.

**Parent Topic:**[Discovery for cloud environment](cloud-discovery-wizard.md)

