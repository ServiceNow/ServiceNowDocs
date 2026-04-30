---
title: Scan Engine integrations
description: You can integrate the Scan Engine into a variety of processes, such as the syncing of definitions or exception reasons, as well as integrating with your existing agile project management systems.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-10-20"
reading_time_minutes: 2
breadcrumb: [Scan Engine, Platform Health, Using Impact, Impact]
---

# Scan Engine integrations

You can integrate the Scan Engine into a variety of processes, such as the syncing of definitions or exception reasons, as well as integrating with your existing agile project management systems.

Scan Engine has the ability to integrate with your other environments running Impact so that you can:

-   Compare technical debt across instances
-   Sync custom definitions across instances
-   Enable approvals for finding exceptions in production
-   Create user stories from findings

The following integrations are available for the Scan Engine.

<table id="table_i33_xr5_3hc"><thead><tr><th>

Integration

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Definitions integration](definitions-integrations.md)

</td><td>

Allows users to synchronize definition overrides and custom definitions between sub-production and production instances. Ensuring a consistent ruleset is being applied throughout the instance stack.

</td></tr><tr><td>

[Exception reason integration](../task/exception-reason-integration.md)

</td><td>

-   Synchronizes exception reasons between sub-production and production instances.
-   Facilitates the approval or rejection of exception reasons in the production environment.

</td></tr><tr><td>

[User story integration](user-story-integration-properties.md)

</td><td>

Creates tasks for findings from a ServiceNow instance to:-   ServiceNow production Instance
-   Jira
-   Azure DevOps
-   Others

</td></tr><tr><td>

[Update set integration](update-set-integration.md)

</td><td>

Synchronizes update set summary scans to the production instance from instances where this integration is enabled.

</td></tr><tr><td>

[AES/AEMC integration properties](../task/aes-aemc-integration-properties.md)

</td><td>

Provides automated governance for custom app deployments by validating deployment requests against admin-defined conditions before approval. When a developer submits a deployment request, the system automatically runs compliance checks to ensure all required rules are met, blocking deployment if conditions fail.

</td></tr></tbody>
</table>**Note:** Except for Jira, Azure DevOps and AES/AEMC integration types, you must first register your instances as part of **My SN Instances**. You will then need to configure either your basic or OAuth authentication methods for your instances to enable synchronization.

