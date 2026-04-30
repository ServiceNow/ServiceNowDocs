---
title: Configure the UCF integration using the UCF Common Controls Hub
description: Compliance administrators can download content from Network Frontiers Unified Compliance Framework \(UCF\) to use as GRC authority documents, citations, controls, and control objectives.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Manage UCF integration, Classic UI, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Configure the UCF integration using the UCF Common Controls Hub

Compliance administrators can download content from Network Frontiers Unified Compliance Framework \(UCF\) to use as GRC authority documents, citations, controls, and control objectives.

## Before you begin

Role required: sn\_comp\_ucf.admin and oauth\_admin

The documents can be updated on pre-defined intervals. You must have a UCF Common Controls Hub account to create shared lists and import them into the ServiceNow® instance. API access is required to download UCF content from the UCF-CCH.

**Note:** Please take note of the following guidelines before configuring the UCF integration using the UCF Common Controls Hub

-   Only the UCF Oauth administrator has access to the system Oauth tables. You must grant the UCF Oauth administrator role to the GRC UCF administrator, so the UCF administrator can set up UCF configuration page.
-   UCF integration requires that GRC is configured and users must be a Common Controls Hub administrator.
-   The configuration page for the global domain is loaded by default. If you are using Domain Separation, delete the default configuration page, and create one specific to your domain.

## About this task

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **Unified Compliance Integration**.

2.  Click the UCF configuration.

    ![UCF Configuration for Oauth](../image/ucf-config-oauth.png)

3.  On the form, fill in the fields.

<table id="table_epy_qrq_f5"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Shared List

</td><td>

The shared list to be imported. **Note:** Shared lists appear for subscription authentication.

</td></tr><tr><td>

Authentication type

</td><td>

Select **Oauth**.

</td></tr><tr><td colspan="2">

**OAuth details**

</td></tr><tr><td>

Client ID

</td><td>

Enter the Client ID or UCF OAuth Client ID provided by Customer Service and Support. See [Create a Now Support Case for UCF-CCH account integration information](create-hi-request-ucf-integration.md) for information.

 **Note:** Configuration information is specific to the ServiceNow® instance. Be sure to enter accurate information for any test, development, or production instances you are using. Do not include spaces in the entry.

</td></tr><tr><td>

Client Secret

</td><td>

Enter a Client Secret to be used by the OAuth Client to authenticate to the Authorization Server. The Client Secret must be sufficiently random to not be guessable.

</td></tr><tr><td>

Oauth2 profile

</td><td>

Enter the OAuth2 profile to use for downloading. The default is the United Compliance Framework Default Profile that is installed with the UCF plugin. This field doesn't typically need to be changed.

</td></tr><tr><td>

Redirect URL

</td><td>

Enter the Redirect URL, provided by Customer Service and Support. For example, `https://mycompany.service-now.com/oauth_redirect.do`

</td></tr></tbody>
</table>4.  Right-click the form header and click **Save**.

5.  In the UCF Integration dialog that appears, click **Request New Token**.

    **Note:** For initial configuration, a user with an UCF administrator account performs this setp and the next step.

6.  Enter your Common Controls Hub credentials to log in.

7.  In the application authorization message that displays, click **Authorize**.

8.  Select a shared list and click **Save Configuration**.


## What to do next

If UCF introduces new fields and content, administrators can use staging tables and transform maps to accommodate those changes to UCF data formats. This is an advanced configuration and not required. The following import sets and tables can be configured to customize the UCF download logic.

|Staging table|Description|
|-------------|-----------|
|UCF Authority Document \[sn\_comp\_ucf\_authority\_document\]|The UCF Authority Document staging table is used to store authority documents that are downloaded from the UCF Common Controls Hub|
|UCF Citation \[sn\_comp\_ucf\_citation\]|The UCF Citation staging table is used to store citations that are downloaded from the UCF Common Controls Hub|
|UCF Control \[sn\_comp\_ucf\_control\]|The UCF Control staging table is used to store controls that are downloaded from the UCF Common Controls Hub|
|UCF Citation to Control \[sn\_comp\_ucf\_m2m\_control\_citation\]|The UCF Citation to Control staging table is used to store citation to controls that are downloaded from the UCF Common Controls Hub|

|Transform maps|Description|
|--------------|-----------|
|Default Authority document transform|Transforms data from the UCF Authority document staging table into the Authority Document table|
|Default Citation Transform|Transforms data from the UCF Citation staging table into the Citation table|
|Default Control transform|Transforms data from the UCF Control staging table into the Control Objective table|
|Control to Citation transform map|Transforms data from the UCF Citation to Control table into the Control Objective to Citation table|

-   **[Integrate with UCF Common Controls Hub to manage compliance frameworks](../concept/c_UCF.md)**  
Compliance administrators can download content from Network Frontiers Unified Compliance Framework \(UCF\) to use as GRC authority documents, citations, controls, and control objectives. The documents can be updated on pre-defined intervals. You must have a UCF Common Controls Hub account to create shared lists and import them into the ServiceNow® instance.
-   **[Elimination of duplicate citations from UCF Shared list download](../concept/ucf-deduplication-pc.md)**  
You can eliminate duplicate citations associated with the authority documents when you receive citations from UCF content as part of the same Shared list.

**Parent Topic:**[Manage the UCF integration](../concept/manage_compliance_frameworks.md)

