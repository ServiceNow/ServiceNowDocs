---
title: Scan Engine integrations
description: Scan Engine integrates with other ServiceNow instances and external agile systems to synchronize definitions, manage exception reasons, create user stories, and enforce governance over app deployments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/instance-integration-scan-engine.html
release: australia
product: Impact
classification: impact
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure the Impact Store Application, Configuring Impact, Impact]
---

# Scan Engine integrations

Scan Engine integrates with other ServiceNow instances and external agile systems to synchronize definitions, manage exception reasons, create user stories, and enforce governance over app deployments.

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

[Definitions integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/definitions-integrations.md)

</td><td>

Allows users to synchronize definition overrides and custom definitions between non-production and production instances. Ensuring a consistent ruleset is being applied throughout the instance stack.

</td></tr><tr><td>

[Exception reason integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/exception-reason-integration.md)

</td><td>

-   Synchronizes exception reasons between non-production and production instances.
-   Facilitates the approval or rejection of exception reasons in the production environment.

</td></tr><tr><td>

[User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/user-story-integration-properties.md)

</td><td>

Creates tasks for findings from a ServiceNow instance to:-   ServiceNow production Instance
-   Jira
-   Azure DevOps
-   Others

</td></tr><tr><td>

[Deployment and synchronization integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/deployment-sync-integrations.md)

</td><td>

-   Update sets: Synchronizes update set summary scans to the production instance from instances where this integration is enabled.
-   AES/AEMC: Provides automated governance for custom app deployments by validating deployment requests against admin-defined conditions before approval. When a developer submits a deployment request, the system automatically runs checks to ensure all required rules are met, blocking deployment if conditions fail.

</td></tr></tbody>
</table>## Prerequisites

Most integrations share the same foundational setup. Complete the following before configuring any specific integration.

-   [Create an integration user account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/task-create-integration-user.md) in development and production environments.
-   [Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md): Register each participating instance in the My SN Instances table. Only one instance in your stack may be designated as Production.
-   Configure authentication using Basic or OAuth. OAuth is strongly recommended for all production environments. See [Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-oauth-auth-method.md) and [Configure the OAuth authentication method production instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-oauth-auth-method-prod.md) or [Configure the Basic authentication method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-basic-auth-method.md) for details.
-   [Validate your instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/validate-instance-connection.md): Validate each instance connection using the **Validate Connection** action on each My SN Instances record.

**Note:** Azure DevOps and the Other integration type authenticate via Basic auth records and API tokens configured directly in Scan Engine Properties, as they do not use My SN Instances. AES/AEMC only requires one My SN Instances record to designate the production controller, with no Authentication Type set.

## Role requirements

|Role|Purpose|Where required|
|----|-------|--------------|
|`sn_se.scan_engine_admin`|Full admin access to Scan Engine configuration|Integration user on all instances|
|`sn_se.internal_rest_integration`|Allows REST calls between instances|Integration user on all instances|
|`admin`|Platform admin|Update Set Scans integration only|

**Important:** Neither Scan Engine role is inherited by the platform admin role. Always assign both roles explicitly on every instance the integration user is imported to.

## Platform notes

-   **Key Management Framework \(KMF\)**

    KMF replaced the Glide Encryptor class for encrypting `password_2` fields. KMF encryption is instance-specific, an encrypted value from one instance cannot be decrypted on another. Any Auth record that crosses an instance boundary requires a password re-entry on the receiving instance. If a pending Scan Engine scripting scope request is blocking authentication, it must be approved in the Key Management Framework module access policies before retrying.

-   **ECMAScript 2021 \(ES12\) mode**

    For User Story integrations, enable ECMAScript 2021 \(ES12\) mode in Scan Engine Properties to use modern JavaScript syntax in field mapping scripts. Without this mode, only the application default JavaScript mode is available.


-   **[Create an integration user account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/task-create-integration-user.md)**  
Create a dedicated integration user account and assign the required roles so that the Scan Engine can authenticate and communicate between your ServiceNow instances.
-   **[Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/register-your-instance.md)**  
Register each participating ServiceNow instance in the My SN Instances table before configuring any instance-to-instance integration.
-   **[Definitions integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/definitions-integrations.md)**  
The Definitions integration synchronizes new, customized, and overridden definitions between non-production and production instances.
-   **[Exception reason integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/exception-reason-integration.md)**  
You can synchronize exception reasons from non-production to Production instances once a record is created or updated.
-   **[User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/user-story-integration-properties.md)**  
The User story integration creates agile tasks and stories directly from Scan Engine finding records in ServiceNow, Jira, Azure DevOps, or any external system.
-   **[Deployment and synchronization integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/deployment-sync-integrations.md)**  
The AES/AEMC and Update set integrations control how custom app deployments are governed and how scan results are synchronized across your instance stack.
-   **[Configure other integration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configure-other-integration-options.md)**  
Configure the Other integration type to create work items in any external system using a custom payload script and basic authentication.

**Parent Topic:**[Configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/configuring-impact-platform.md)

**Previous topic:**[Initiate data migration from IDI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/initiate-migration-idi.md)

**Next topic:**[Create an integration user account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/task-create-integration-user.md)

