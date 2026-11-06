---
title: Scan Engine integrations
description: Scan Engine integrates with other ServiceNow instances and external agile systems to synchronize definitions, manage exception reasons, create user stories, and enforce governance over app deployments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/instance-integration-scan-engine.html
release: australia
topic_type: concept
last_updated: "2026-10-27"
reading_time_minutes: 4
breadcrumb: [Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Scan Engine integrations

Scan Engine integrates with other ServiceNow instances and external agile systems to synchronize definitions, manage exception reasons, create user stories, and enforce governance over app deployments.

Scan Engine integrates with your other environments running Impact so that you can:

-   Compare technical debt across instances
-   Sync custom definitions across instances
-   Enable approvals for finding exceptions in production
-   Create user stories from findings

Before you configure any integration, complete the setup in [Instance integration setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integrations-overview.md). It covers the inputs, setup sequence, required roles, and platform notes that apply to every integration.

The following integrations are available for the Scan Engine. The table shows where each integration is configured.

<table id="table_i33_xr5_3hc"><thead><tr><th>

Integration

</th><th>

Description

</th><th>

Where to configure

</th></tr></thead><tbody><tr><td>

[Definitions integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/definitions-integrations.md)

</td><td>

Synchronizes definition overrides and custom definitions between non-production and production instances so a consistent ruleset applies throughout the instance stack.

</td><td>

-   Development instances only. Enable it in My SN Instances on each development instance.
-   Only development instances can manually push definition sync requests to the rest of the stack.
-   Test and production instances don't trigger definition syncs.

</td></tr><tr><td>

[Exception reason integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/exception-reason-integration.md)

</td><td>

-   Synchronizes exception reasons between non-production and production instances.
-   Facilitates the approval or rejection of exception reasons in the production environment.

</td><td>

-   Configure it on each instance where exceptions are raised.
-   On production, the approval group is specified here, and that group is notified when a new exception is raised.

</td></tr><tr><td>

[User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/user-story-integration-properties.md)

</td><td>

Creates tasks for findings from a ServiceNow instance to:

 -   ServiceNow production instance
-   Jira
-   Azure DevOps
-   Others

 **Note:** Jira and Azure DevOps authenticate with a Basic auth record and an API token, configured in Scan Engine Properties. The Other type takes a username and API token directly on Scan Engine Properties. None of these types use My SN Instances.

</td><td>

-   ServiceNow user story integration:
    -   Configure on the source instance where the findings originate.
    -   The target is production.
-   Jira, Azure DevOps, or the Other types:
    -   Configure on the instance where Scan Engine runs and the findings are generated.
    -   These types don't need a My SN Instances record.

</td></tr><tr><td>

[Deployment and synchronization integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/deployment-sync-integrations.md)

</td><td>

-   Update sets: Synchronizes update set summary scans to the production instance from instances where this integration is enabled.
-   AES/AEMC:
    -   Provides automated governance for custom app deployments by validating deployment requests against admin-defined conditions before approval.
    -   When a developer submits a deployment request, the system automatically runs checks to verify all required rules are met, blocking deployment if conditions fail.

</td><td>

-   Update sets:
    -   Enable it on each instance whose update set scan data you want to share.
    -   Scan data goes to production and to all other instances in the integration, so you can check it from any instance.
-   AES/AEMC:
    -   Enable it on production only. Production needs one My SN Instances record whose environment is Production.
    -   Cross-instance deployment calls also depend on the `sn_pipeline_environment` table from Pipelines and Deployments.
    -   Each Environment record has an **Instance credential** field that points to a Connection and Credential Alias.

</td></tr></tbody>
</table>-   **[Instance integration setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integrations-overview.md)**  
Setup for Scan Engine integrations between instances starts with common steps. The roles and platform requirements depend on the integration.
-   **[Create an integration user account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/task-create-integration-user.md)**  
Create a dedicated integration user account and assign the required roles so that the Scan Engine can authenticate and communicate between your ServiceNow instances.
-   **[Grant Key Management Framework access on an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/complete-kmf-access.md)**  
Give the setup user KMF roles and approve the Scan Engine decryption policy so that imported credentials can be decrypted on the instance.
-   **[Integrations across multiple instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/multi-instance-integration.md)**  
A stack with more than two instances needs an OAuth provider registry and an OAuth client registry for every instance in the stack.
-   **[Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md)**  
Register each participating ServiceNow instance in the My SN Instances table before configuring any instance-to-instance integration.
-   **[Definitions integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/definitions-integrations.md)**  
The Definitions integration manually syncs new, customized, and overridden definitions from development to production and the other instances.
-   **[Exception reason integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/exception-reason-integration.md)**  
You can synchronize exception reasons from non-production to Production instances after a record is created or updated.
-   **[User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/user-story-integration-properties.md)**  
The User story integration creates agile tasks and stories directly from Scan Engine finding records in ServiceNow, Jira, Azure DevOps, or any external system.
-   **[Deployment and synchronization integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/deployment-sync-integrations.md)**  
The AES/AEMC and Update set integrations control how custom app deployments are governed and how scan results are synchronized across your instance stack.
-   **[Configure other integration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-other-integration-options.md)**  
Configure the Other integration to create work items in any external system by using a payload script, an endpoint, a username, and an API token.

**Parent Topic:**[Activate Scan Engine and review settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-initial-scan-engine-settings.md)

