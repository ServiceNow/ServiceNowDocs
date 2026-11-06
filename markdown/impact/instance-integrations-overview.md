---
title: Instance integration setup
description: Setup for Scan Engine integrations between instances starts with common steps. The roles and platform requirements depend on the integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/instance-integrations-overview.html
release: australia
topic_type: concept
last_updated: "2026-10-28"
reading_time_minutes: 5
breadcrumb: [Scan Engine integrations, Activate Scan Engine and review settings, Configuring Impact, Impact]
---

# Instance integration setup

Setup for Scan Engine integrations between instances starts with common steps. The roles and platform requirements depend on the integration.

## Before you begin

Gather these inputs before you set up an integration between ServiceNow instances. The Jira, Azure DevOps, and Other integration types need different inputs, which their topics list. Each row shows where you use the input.

|Input|Details|Topic|
|-----|-------|-----|
|Instance name and URL|The instance name must match the `instance_name` system property. Use the URL format `https://instancename.service-now.com`.|[Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md)|
|Environment type|Development, Test, or Production. Only one instance in the stack can be Production.|[Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md)|
|Integration user ID and password|Record the password in a secure location. You re-enter it in several fields.|[Create an integration user account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/task-create-integration-user.md)|
|Authentication method|Use either OAuth or Basic authentication for an integration. You can't use both or combine them. OAuth is recommended.|[Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-oauth-auth-method.md) or [Configure the Basic authentication method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-basic-auth-method.md)|

## Setup roadmap

Complete steps 1 to 6 in order for integrations between ServiceNow instances, including the User story integration when its integration type is ServiceNow instance. The Jira, Azure DevOps, and Other integration types connect to an external system and don't use My SN Instances records, so those steps don't apply to them. Open the linked topic for details.

<table id="table_setup_roadmap"><thead><tr><th>

Step

</th><th>

Task

</th><th>

Run on

</th></tr></thead><tbody><tr><td>

1

</td><td>

[Create an integration user account](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/task-create-integration-user.md). Assign the roles in the table of integration user roles.

</td><td>

Each instance

</td></tr><tr><td>

2

</td><td>

[Register your instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/register-your-instance.md)

</td><td>

1.  Development first
2.  Then production
3.  Then any additional instances

</td></tr><tr><td>

3

</td><td>

[Configure the OAuth authentication method development instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-oauth-auth-method.md) and [Configure the OAuth authentication method production instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-oauth-auth-method-prod.md), or [Configure the Basic authentication method](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-basic-auth-method.md)

</td><td>

1.  Development
2.  Then production

</td></tr><tr><td>

4

</td><td>

[Grant Key Management Framework access on an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/complete-kmf-access.md)

</td><td>

Each instance that receives imported records

</td></tr><tr><td>

5

</td><td>

[Validate your instance connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/validate-instance-connection.md)

</td><td>

Each instance

</td></tr><tr><td>

6

</td><td>

[Integrations across multiple instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/multi-instance-integration.md)

</td><td>

After the first pair validates, each additional non-production instance

</td></tr><tr><td>

7

</td><td>

Configure the integrations you need:-   [Definitions integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/definitions-integrations.md)
-   [Exception reason integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/exception-reason-integration.md)
-   [User story integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/user-story-integration-properties.md)
-   [Deployment and synchronization integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/deployment-sync-integrations.md)
-   [Configure other integration options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-other-integration-options.md)

</td><td>

Varies by integration. Open each topic to see which instances to use.

</td></tr></tbody>
</table>## Role requirements

Two sets of roles apply to this setup. The first set is the roles you need to set up the integrations. The second set is the roles you assign to the integration user.

|Role|When you need it|
|----|----------------|
|Scan Engine admin, `sn_se.scan_engine_admin`|To configure Scan Engine properties and the integrations|
|admin|To create the integration user and the setup records|
|KMF admin, `sn_kmf.admin`|Only if validation fails after you complete all of the setup. See [Grant Key Management Framework access on an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/complete-kmf-access.md).|

|Role|Purpose|Where required|
|----|-------|--------------|
|`sn_se.scan_engine_admin`|Full admin access to Scan Engine configuration|Integration user on all instances|
|`sn_se.internal_rest_integration`|Allows REST calls between instances|Integration user on each instance that receives calls|
|`sn_se.scan_engine_user`|Runs update set scans|Scanning user for the Update set integration, unless that user also has `sn_se.scan_engine_admin`|

**Important:** The platform admin role does not include the Scan Engine roles. Assign them explicitly on every instance the integration user is imported to.

## Platform notes

-   **Key Management Framework \(KMF\)**

    KMF encrypts passwords with a key that is unique to each instance, so imported passwords must be re-entered on the receiving instance. See [Grant Key Management Framework access on an instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/complete-kmf-access.md) for the steps.

-   **ECMAScript 2021 \(ES12\) mode**

    For User Story integrations, enable ECMAScript 2021 \(ES12\) mode in Scan Engine Properties to use modern JavaScript syntax in field mapping scripts. Without this mode, only the application default JavaScript mode is available.


**Parent Topic:**[Scan Engine integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/instance-integration-scan-engine.md)

