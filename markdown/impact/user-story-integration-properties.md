---
title: User story integration
description: The User story integration creates agile tasks and stories directly from Scan Engine finding records in ServiceNow, Azure DevOps, or any external system using the Other type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/user-story-integration-properties.html
release: brazil
topic_type: concept
last_updated: "2026-11-12"
reading_time_minutes: 1
breadcrumb: [Scan Engine integrations, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# User story integration

The User story integration creates agile tasks and stories directly from Scan Engine finding records in ServiceNow, Azure DevOps, or any external system using the Other type.

When a finding is identified, the integration can automatically or manually generate a work item in your agile system of record. Role required: `sn_se.scan_engine_admin`.

Configure the ServiceNow user story integration on the source instance where the findings originate. The integration creates stories in the target instance, such as production, from those findings. Define both instances in My SN Instances.

Configure Azure DevOps, or the Other type on the instance where Scan Engine runs and the findings are generated. Those types don't need a My SN Instances record.

|Type|Authentication|Description|
|----|--------------|-----------|
|ServiceNow instance|My SN Instances + OAuth or Basic|Creates stories in a Production instance from sub-production findings using Agile 2.0.|
|Azure DevOps|Basic auth record + API token|Creates work items in an Azure DevOps project from findings.|
|Other|Username and API token on Scan Engine Properties|Connects to any external system via a custom payload script.|

**Note:** Azure DevOps authenticates with a Basic auth record and an API token, configured in Scan Engine Properties. The Other type takes a username and API token directly on Scan Engine Properties. Neither type uses My SN Instances.

-   **[Configure ServiceNow user story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-sn-integration-options.md)**  
Configure the ServiceNow instance user story integration to create stories in a production instance directly from finding records on a non-production instance.
-   **[Configure Azure DevOps story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-azure-devops-integration-options.md)**  
Configure the Azure DevOps story integration to create work items in an Azure DevOps project directly from Scan Engine finding records.

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/instance-integration-scan-engine.md)

**Related topics**  


[Configure ServiceNow user story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configuring-sn-integration-options.md)

[Configure Azure DevOps story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-azure-devops-integration-options.md)

[Configure other integration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/impact/configure-other-integration-options.md)

