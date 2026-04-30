---
title: Microsoft Azure Functions discovery with Patterns
description: The Discovery and Service Mapping Patterns application uses the Azure - Functions \(LP\) and Azure - Functions TD Patterns to discover Azure Functions apps and map them in the context of application services. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
keywords: [Azure, Function]
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Microsoft Azure Functions discovery with Patterns

The Discovery and Service Mapping Patterns application uses the Azure - Functions \(LP\) and Azure - Functions TD Patterns to discover Azure Functions apps and map them in the context of application services. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Azure Functions detailed information**

    [Detailed information on products discovered by ITOM Visibility](../reference/r_SupportedApplications.md)

-   **Azure service account**

    Configure the Azure service account. For more information, see [Set up a cloud account for Azure](../../cloud-management-v2-setup/task/azure-cloud-accts-cloud-mgt.md)

-   **Azure Principal credentials**

    On the ServiceNow AI Platform, create a service account for cloud discovery. Set the account Id to the Azure Service Principal as it appears at the Microsoft Azure Console. For more information see: [Create Azure cloud credentials](../../discovery/task/create-azure-cloud-credentials.md)

-   **Privileges**

    On the Microsoft Azure Console, provide a user with the API Management Service Reader role.

-   **Run Azure Cloud discovery**

    For detailed information, see: [Discovery for Microsoft Azure Cloud](../../discovery/concept/azure-cloud-discovery.md)

-   **Create discovery schedule**

    [Create a discovery schedule in Cloud Discovery Workspace](../../discovery/task/cloud-operations-disco-create-schedule.md)


## Data collected by Discovery during horizontal discovery

|Table and field|Description|
|---------------|-----------|
|Azure Function \[cmdb\_ci\_cloud\_function\]|
|name|The name of the Function app.|
|Object\_id|The ID of the Function app.|
|ip\_address|The IP Address of the Function app.|
|fqdn|The Fully Qualified Domain Name \(FQDN\) of the Function app.|
|code\_location\_url|The URL of the Function app source code.|
|app\_function\_state|The state of the Function app.|
|operational\_status|The operational status of the Function app.|
|install\_status|The installation status of the Function app.|

## CI relationships

These relationships are created to support Azure Functions discovery:

|CI|Relationship|CI|
|---|------------|---|
|Azure Functions \[cmdb\_ci\_cloud\_function\]|Hosted on::Hosts|Azure datacenter \[cmdb\_ci\_azure\_datacenter\]|

## Connections found by Service Mapping during top-down discovery

Service Mapping can discover the following connections:

-   Connections to the following databases: MSSql, MySql, MongoDB, and Documentum.
-   HTTP connections belonging to Azure Functions environment, for example, https://scenario4-hop1-azure-function.azurewebsites.net.

    **Note:** Service Mapping does not scan java classes/jars and binary files for possible information about outgoing HTTP connections of Azure Functions. If java classes/jars and binary files are the only source of information about some outgoing HTTP connections, Service Mapping does not find such HTTP connections.


**Parent Topic:**[Available discovery patterns](available-patterns.md)

**Related topics**  


[Define a Cloud REST Query for cloud computing devices](../task/cloud-rest-query-pattern.md)

