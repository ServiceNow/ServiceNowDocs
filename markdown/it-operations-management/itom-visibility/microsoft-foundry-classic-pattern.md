---
title: Microsoft Foundry \(Classic\) pattern-based discovery
description: AI Agent Topology Mapping discovers Microsoft Foundry \(Classic\) services and agents during horizontal discovery.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 9
keywords: [Azure AI Foundry, Microsoft Foundry, AI Agent Topology Mapping, Azure AI, AI discovery]
breadcrumb: [Reference, AI Agent Topology Mapping, ITOM Visibility, IT Operations Management]
---

# Microsoft Foundry \(Classic\) pattern-based discovery

AI Agent Topology Mapping discovers Microsoft Foundry \(Classic\) services and agents during horizontal discovery.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Microsoft Foundry data model

The following diagram illustrates the tables and relationships that the AI Agent Topology Mapping application creates when discovering Microsoft Foundry resources.

![Microsoft Foundry data model](../images/microsoft-foundry-data-model.png "Tables and relationships populated during Microsoft Foundry discovery")

**Note:** The **Deployed as::Deployment of** relationship between the AI Function \[cmdb\_ci\_function\_ai\] and AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] tables is stored in the Asset-CI Relationship \[cmdb\_rel\_asset\_ci\] table and isn't represented in the Dependency View map.

## Discovery requirements

-   **Verify that the applications are up to date**

    Discovering these resources may require updating to the latest version of the following applications from the ServiceNow Store:

    -   AI Agent Topology Mapping
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
    -   CMDB CI Class Models
-   **Activate the cloud-related CI relationships**

    To include discovered components into service instances, enable CI relationships used in tag-based discovery by Service Mapping. These CI relationships are available from the 1.0.68 release on the ServiceNow Store. For operational steps, see [Tag-based discovery configuration](../../service-mapping/concept/tag_discovery_configuration.md).

-   **Azure Availability Set**

    Wait for the **Clean-Up job for Availability zone to clear availability set record** schedule job to delete all the pre-populated availability set's Configuration Items \(CI\) in the **cmdb\_ci\_azure\_availability\_set** table.

-   **Azure Availability Zone**

    To run a discovery with Azure Availability Zone, register the subscription ID to the **AvailabilityZonePeering** feature with AZ CLI using `az feature register -n AvailabilityZonePeering --namespace Microsoft.Resources` to use the Check Zone Peering API. Check the status with `az feature show -n AvailabilityZonePeering --namespace Microsoft.Resources` before running discovery.

-   **Set up Azure service accounts**

    Enable Cloud Discovery to access your Azure environment.

    Discovering Azure GovCloud \(US\) accounts requires using a datacenter URL when setting up an Azure service account. For more information, see [Set up Azure service accounts](../../it-operations-management/task/setup-azure-service-accounts.md).

-   **Create an Azure cloud discovery schedule**

    For more information, see [Create an Azure Discovery schedule in Discovery Admin Workspace](../../discovery/task/create-azure-schedule-DAW.md).

-   **\(Optional\) Discover datacenters only for new subscriptions**

    Starting with Zurich Patch 2, you can discover datacenters only for new subscriptions added since the last discovery. For more information, see [Discover datacenters only for new cloud accounts](../../service-mapping/task/discover-datacenter-only-new-account.md).

-   **\(Optional\) Populate Service Account and Logical Datacenter fields in cloud CIs**

    Starting with Discovery and Service Mapping Patterns version 1.30.2, you can improve query performance by populating Service Account and Logical Datacenter fields directly in cloud CIs. For more information, see [Improved query performance with direct field population in CI tables](../../service-mapping/concept/query-service-account-ldc-fields.md).


## Verify the REST API Permissions

Download the [Cloud Discovery patterns spreadsheet](https://downloads.docs.servicenow.com/resource/enus/api/servicenow-discovery-patterns-api-details.xlsx) so you can grant user permissions required for running the Discovery patterns. In addition to permissions, the spreadsheet also includes useful information such as pattern names, types, CI Classes, and links to vendor documentation. New patterns are available quarterly, so check periodically to be sure you have the latest version of the spreadsheet.

## Data collection

The AI Agent Topology Mapping application includes the following patterns for Microsoft Foundry discovery:

-   Azure - AI Foundry Agents
-   Azure - AI Service Foundry
-   Azure - AI Service Foundry Project

The Azure - AI Foundry Agents pattern collects AI System Digital Assets, AI Prompt Digital Assets, and Key Value information. You can view this information in the **Related Links** section of the CI record by navigating to **All** &gt; **Configuration** &gt; **Azure** &gt; **Azure AI Foundry Agents** and selecting the relevant record.

The AI Agent Topology Mapping application populates data in both CMDB and non-CMDB tables.

## Data stored in non-CMDB tables

The Azure - AI Foundry Agents pattern populates data in non-CMDB tables.

If you have the AI Control Tower application, you can view the information in the AI Control Tower Workspace.

|Field|Description|
|-----|-----------|
|Display name \[display\_name\]|Display name of the Microsoft Foundry agent.|
|External record reference \[external\_ref\_id\]|Unique identifier of the Microsoft Foundry agent.|
|Model \[model\]|References the AI System Component Product Model \[cmdb\_ai\_system\_component\_product\_model\] table.|
|Asset type \[model\_category\]|Asset type of the agent. Value is set to **Agentic AI**.|
|State \[install\_status\]|State of the agent. Value is set to **Deployed**.|
|AI prompts \[ai\_prompts\]|References the AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\] table.|
|AI models \[ai\_models\]|References the AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\] table.|
|Configuration Item \[ci\]|References the AI Function \[cmdb\_ci\_function\_ai\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Microsoft Foundry agent.|
|Short description \[short\_description\]|Description of the Microsoft Foundry agent.|
|Status \[status\]|Operational status of the agent. Value is set to **PREPARED**.|
|Version \[version\]|Version of the Microsoft Foundry agent.|
|Manufacturer \[manufacturer\]|Cloud provider of the resource. Value is set to **Azure**.|
|Model categories \[cmdb\_model\_category\]|Model category. Value is set to **Agentic AI**.|

|Field|Description|
|-----|-----------|
|Prompt information \[prompt\_info\]|Instruction text defined for the Microsoft Foundry agent.|
|Model \[model\]|References the AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\] table.|
|Asset type \[model\_category\]|Asset type of the prompt. Value is set to **AI prompt**.|
|Configuration Item \[ci\]|References the AI Function \[cmdb\_ci\_function\_ai\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Microsoft Foundry agent, used to identify the associated prompt model.|
|Manufacturer \[manufacturer\]|Cloud provider of the resource. Value is set to **Azure**.|
|Model categories \[cmdb\_model\_category\]|Model category. Value is set to **AI prompt**.|

|Field|Description|
|-----|-----------|
|Display name \[display\_name\]|Name of the foundation model.|
|External record reference \[external\_ref\_id\]|Resource identifier of the foundation model.|
|Model \[model\]|References the AI Model Product Model \[cmdb\_ai\_model\_product\_model\] table.|
|Asset type \[model\_category\]|Asset type of the model. Value is set to **AI model**.|
|Vendor \[vendor\]|Provider of the foundation model.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the foundation model.|
|Model number \[model\_number\]|Model ID assigned by Microsoft Foundry.|
|Version \[version\]|Version of the foundation model.|
|Description \[description\]|Description of the foundation model.|
|Manufacturer \[manufacturer\]|Provider of the foundation model.|
|Model categories \[cmdb\_model\_category\]|Model category. Value is set to **AI model**.|

## Data stored in CMDB tables

The AI Agent Topology Mapping application populates data in the CMDB when running the Microsoft Foundry patterns.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Microsoft Foundry agent.|
|Object ID \[object\_id\]|Unique identifier of the Microsoft Foundry agent.|
|Description \[short\_description\]|Description of the Microsoft Foundry agent.|
|Manufacturer \[manufacturer\]|Cloud provider of the resource. Value is set to **Azure**.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|Install Status \[install\_status\]|Install status of the resource. Default value is Installed.|
|Comments \[comments\]|Resource type identifier. Value is set to **Azure::Foundry::Agent**.|

<table id="table_ai_foundry"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the Microsoft Foundry service.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier of the Microsoft Foundry service.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

Description of the resource. Value is set to **Azure Foundry Service**.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Azure Service Type \[azure\_service\_type\]

</td><td>

Azure resource type. For example: microsoft.cognitiveservices/accounts.

</td></tr><tr><td>

Azure Service Kind \[azure\_service\_kind\]

</td><td>

Resource kind of the Microsoft Foundry service. For example: AIServices.

</td></tr></tbody>
</table><table id="table_ai_project"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the Microsoft Foundry project.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier of the Microsoft Foundry project.

</td></tr><tr><td>

Comments \[comments\]

</td><td>

Azure region where the Microsoft Foundry project is deployed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Model number \[model\_number\]

</td><td>

Internal identifier of the Microsoft Foundry project.

</td></tr><tr><td>

Azure Project Kind \[azure\_project\_kind\]

</td><td>

Resource kind of the Microsoft Foundry project. For example: AIServices.

</td></tr></tbody>
</table>## Dependency Views map

The following dependency views display the relationships between Microsoft Foundry resources. The CI relationships table captures all relationships across the three views.

![Microsoft Foundry AI Foundry CI and connections on a Dependency Views map](../images/microsoft-foundry-ai-foundry-dependency-view.png "Azure AI Foundry dependency view")

![Microsoft Foundry AI Project CI and connections on a Dependency Views map](../images/microsoft-foundry-ai-project-dependency-view.png "Azure AI Project dependency view")

![Microsoft Foundry AI Function CI and connections on a Dependency Views map](../images/microsoft-foundry-ai-function-dependency-view.png "AI Function dependency view")

## CI relationships

The Microsoft Foundry patterns create the following relationships and references to support Microsoft Foundry discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI/Table|Relationship|CI/Table|
|--------|------------|--------|
|AI Function \[cmdb\_ci\_function\_ai\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Azure AI Project \[cmdb\_ci\_azure\_ai\_project\]|Contains::Contained by|AI Function \[cmdb\_ci\_function\_ai\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|AI Function \[cmdb\_ci\_function\_ai\]|
|AI Function \[cmdb\_ci\_function\_ai\]|Deployed as::Deployment of|AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]|
|Azure AI Foundry \[cmdb\_ci\_azure\_ai\_foundry\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Azure AI Foundry \[cmdb\_ci\_azure\_ai\_foundry\]|
|Azure AI Foundry \[cmdb\_ci\_azure\_ai\_foundry\]|Contains::Contained by|Azure AI Project \[cmdb\_ci\_azure\_ai\_project\]|
|Azure AI Project \[cmdb\_ci\_azure\_ai\_project\]|Hosted on::Hosts|Azure Datacenter \[cmdb\_ci\_azure\_datacenter\]|
|Resource Group \[cmdb\_ci\_resource\_group\]|Contains::Contained by|Azure AI Project \[cmdb\_ci\_azure\_ai\_project\]|

|CI/Table|Field|Referenced CI/Table|
|--------|-----|-------------------|
|AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]|Model \[model\]|AI System Component Product Model \[cmdb\_ai\_system\_component\_product\_model\]|
|AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]|AI prompts \[ai\_prompts\]|AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\]|
|AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]|AI models \[ai\_models\]|AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]|
|AI System Digital Asset \[alm\_ai\_system\_digital\_asset\]|Configuration Item \[ci\]|AI Function \[cmdb\_ci\_function\_ai\]|
|AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\]|Model \[model\]|AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\]|
|AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\]|Configuration Item \[ci\]|AI Function \[cmdb\_ci\_function\_ai\]|
|AI Model Digital Asset \[alm\_ai\_model\_digital\_asset\]|Model \[model\]|AI Model Product Model \[cmdb\_ai\_model\_product\_model\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Azure AI Foundry \[cmdb\_ci\_azure\_ai\_foundry\]|
|Key Value \[cmdb\_key\_value\]|Configuration item \[configuration\_item\]|Azure AI Project \[cmdb\_ci\_azure\_ai\_project\]|

## Azure tag discovery

The Azure - AI Service Foundry pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Azure AI Foundry \[cmdb\_ci\_azure\_ai\_foundry\] table.|

The Azure - AI Service Foundry Project pattern collects tags and populates them in the Key Value \[cmdb\_key\_value\] table.

|Field|Description|
|-----|-----------|
|Key \[key\]|Tag name.|
|Value \[value\]|Tag value.|
|Configuration item \[configuration\_item\]|References the Azure AI Project \[cmdb\_ci\_azure\_ai\_project\] table.|

**Parent Topic:**[AI Agent Topology Mapping reference](ai-agent-topology-mapping-reference.md)

**Related topics**  


[Microsoft Azure Cloud discovery using patterns](../../service-mapping/reference/azure-cloud-discovery-patterns.md)

