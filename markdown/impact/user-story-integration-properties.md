---
title: User story integration
description: The User story integration creates agile tasks and stories directly from Scan Engine finding records in ServiceNow, Jira, Azure DevOps, or any external system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/user-story-integration-properties.html
release: australia
topic_type: concept
last_updated: "2026-05-05"
reading_time_minutes: 1
breadcrumb: [Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# User story integration

The User story integration creates agile tasks and stories directly from Scan Engine finding records in ServiceNow, Jira, Azure DevOps, or any external system.

When a finding is identified, the integration can automatically or manually generate a work item in your agile system of record. Role required: `sn_se.scan_engine_admin`.

|Type|Authentication|Description|
|----|--------------|-----------|
|ServiceNow instance|My SN Instances + OAuth or Basic|Creates stories in a Production instance from sub-production findings using Agile 2.0.|
|Jira|Basic auth record + API token|Creates work items in a Jira project from findings.|
|Azure DevOps|Basic auth record + API token|Creates work items in an Azure DevOps project from findings.|
|Other|Basic auth record + API token|Connects to any external system via a custom payload script.|

**Note:** Jira, Azure DevOps, and the Other integration type do not use My SN Instances. They authenticate using a basic auth record and an API token configured directly in Scan Engine Properties.

-   **[Configure ServiceNow user story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-sn-integration-options.md)**  
Configure the ServiceNow instance user story integration to create stories in a production instance directly from finding records on a non-production instance.
-   **[Configure Jira user story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-jira-integration-options.md)**  
Configure the Jira user story integration to create work items in a Jira project directly from Scan Engine finding records.
-   **[Configure Azure DevOps story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-azure-devops-integration-options.md)**  
Perform the following procedure to configure your Azure DevOps integration options.

**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/instance-integration-scan-engine.md)

**Related topics**  


[Configure ServiceNow user story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-sn-integration-options.md)

[Configure Jira user story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-jira-integration-options.md)

[Configure Azure DevOps story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-azure-devops-integration-options.md)

[Configure other integration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-other-integration-options.md)

