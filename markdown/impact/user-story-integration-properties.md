---
title: User story integration
description: The User story integration creates agile tasks and stories directly from Scan Engine finding records in ServiceNow, Jira, Azure DevOps, or any external system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/user-story-integration-properties.html
release: australia
topic_type: concept
last_updated: "2026-06-03"
reading_time_minutes: 2
breadcrumb: [Scan Engine integrations, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# User story integration

The User story integration creates agile tasks and stories directly from Scan Engine finding records in ServiceNow, Jira, Azure DevOps, or any external system.

When a finding is identified, the integration can automatically or manually generate a work item in your agile system of record. Role required: `sn_se.scan_engine_admin`.

Configure the ServiceNow user story integration on the source instance where the findings originate. The integration creates stories in the target instance, such as production, from those findings. Define both instances in My SN Instances.

Configure Jira, Azure DevOps, or the Other type on the instance where Scan Engine runs and the findings are generated. Those types don't need a My SN Instances record.

|Type|Authentication|Description|
|----|--------------|-----------|
|ServiceNow instance|My SN Instances + OAuth or Basic|Creates stories in a Production instance from sub-production findings using Agile 2.0.|
|Jira|Basic auth record + API token|Creates work items in a Jira project from findings.|
|Azure DevOps|Basic auth record + API token|Creates work items in an Azure DevOps project from findings.|
|Other|Username and API token on Scan Engine Properties|Connects to any external system via a custom payload script.|

**Note:** Jira and Azure DevOps authenticate with a Basic auth record and an API token, configured in Scan Engine Properties. The Other type takes a username and API token directly on Scan Engine Properties. None of these types use My SN Instances.

-   **[Configure ServiceNow user story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configuring-sn-integration-options.md)**  
Configure the ServiceNow instance user story integration to create stories in a production instance directly from finding records on a non-production instance.
-   **[Configure Jira user story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-jira-integration-options.md)**  
Configure the Jira user story integration to create work items in a Jira project directly from Scan Engine finding records.
-   **[Configure Azure DevOps story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-azure-devops-integration-options.md)**  
Configure the Azure DevOps story integration to create work items in an Azure DevOps project directly from Scan Engine finding records.

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integration-scan-engine.md)

**Related topics**  


[Configure ServiceNow user story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configuring-sn-integration-options.md)

[Configure Jira user story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-jira-integration-options.md)

[Configure Azure DevOps story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-azure-devops-integration-options.md)

[Configure other integration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-other-integration-options.md)

