---
title: Skill inputs and triggers for Now Assist for Software Asset Management \(SAM\)
description: Get a quick overview of the skill inputs and triggers for Now Assist for Software Asset Management \(SAM\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.
locale: en-US
release: zurich
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Skill inputs and triggers for Now Assist for Software Asset Management \(SAM\)

Get a quick overview of the skill inputs and triggers for Now Assist for Software Asset Management \(SAM\). By configuring the inputs or triggers for a skill, you can determine how and when a skill is used.

## Now Assist for SAM skills and triggers overview

Depending on the selected skill, you can configure the inputs or triggers. These settings determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate a publisher summary. A trigger initiates an action, such as when the system generates a publisher summary.

## Publisher compliance summarization skill

For the publisher compliance summarization skill, select the triggers that determine when a publisher compliance summary is generated. You can also select the properties that control how a publisher compliance summary is displayed. To display the publisher compliance summary, you need to select the **Display** toggle button on the Choose where to display page while configuring Now Assist for SAM. For details on the **Display** toggle button, see [Configuring Now Assist for Software Asset Management \(SAM\)](../task/configure-now-assist-sam.md).

The following table lists the triggers that determine when a publisher compliance summary is generated and how a publisher compliance summary is displayed.

|Trigger|Description|
|-------|-----------|
|User triggered|Publisher compliance summary that is generated when the agent manually triggers the skill by selecting **Summarize** in the Publisher details page.|

The following table lists the inputs for the publisher compliance summarization skill.

|Input|Description|
|-----|-----------|
|Reconciliation results|Compliance status of the software products with regards to the discovery and entitlements.|
|Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\]|Product life-cycle details for all the software products that are installed in your environment.|
|Dashboards|Dashboards include Discovered inventory, Normalization and content, and Health check.|

## Product compliance summarization skill

For the product compliance summarization skill, select the triggers that determine when a product compliance summary is generated. You can also select the properties that control how a product compliance summary is displayed. To display the product compliance summary, you need to select the **Display** toggle button on the Choose where to display page while configuring Now Assist for SAM. For details on the **Display** toggle button, see [Configuring Now Assist for Software Asset Management \(SAM\)](../task/configure-now-assist-sam.md).

The following table lists the triggers that determine when a product compliance summary is generated and how a product compliance summary is displayed.

|Trigger|Description|
|-------|-----------|
|User triggered|Product compliance summary is generated when the agent manually triggers the skill by selecting **Summarize** in the Publisher details page.|

The following table lists the inputs for the product compliance summarization skill.

<table id="table_dg5_c5k_y2c"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reconciliation results

</td><td>

Compliance status of the software products with regards to the discovery and entitlements.

</td></tr><tr><td>

Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\]

</td><td>

Contains product life-cycle details for all the software products that are installed in your environment.

</td></tr><tr><td>

Dashboards

</td><td>

Dashboards include Discovered inventory, Normalization and content, Health check, and Optimization and Savings dashboard.

</td></tr><tr><td>

SAP related tables

</td><td>

The SAP related tables include:-   SAP Document Type \[samp\_sap\_document\_type\]
-   SAP Digital Access Usage \[samp\_sap\_digital\_access\_usage\]
-   SAP Engine Usage \[samp\_sap\_sw\_client\_access\]
-   SAP System User \[samp\_sap\_system\_user\]

</td></tr><tr><td>

Software Subscription \[samp\_sw\_subscription\] table

</td><td>

Contains information pertaining to user software subscriptions.

</td></tr><tr><td>

Purchased Subscription Details \[samp\_purchased\_subscription\_details\]

</td><td>

Contains the information pulled from the Microsoft Azure portal related to subscriptions purchased and assigned for Microsoft 365.

</td></tr><tr><td>

Software Installation table \[cmdb\_sam\_sw\_install\]

</td><td>

Contains information on all software installed in your environment.

</td></tr></tbody>
</table>## Recommended actions skill

For the recommended actions skill, select the triggers that determine when a list of recommended actions is generated. You can also select the properties that control how recommended actions is displayed. To display recommended actions, you need to select the **Display** toggle button on the Choose where to display page while configuring Now Assist for SAM. For details on the **Display** toggle button, see [Configuring Now Assist for Software Asset Management \(SAM\)](../task/configure-now-assist-sam.md).

The following table lists the triggers that determine when recommended actions are generated and how the list of recommended actions is displayed.

<table id="table_pfz_rtm_y2c"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User triggered

</td><td>

Recommended actions is generated when the user manually triggers the skill by selecting either of the two options in the Publisher details page:

-   Get recommendations icon on Recommended actions sidebar and then select **Get recommendations**.
-   **Summarize** button for a product. When you select **Summarize**, both the product summary along recommended actions gets generated.

</td></tr></tbody>
</table>The following table lists the inputs for the recommended actions skill.

<table id="table_wzh_45m_y2c"><thead><tr><th>

Inputs

</th><th>

Source

</th></tr></thead><tbody><tr><td colspan="2">

**Configuration inputs**

</td></tr><tr><td>

Health check issues

</td><td>

Scan Findings \[Scan\_finding\]

</td></tr><tr><td>

Installs requiring actions

</td><td>

Installs Unlicensed Reasons \[samp\_install\_unlicensed\_reason\]

</td></tr><tr><td>

Normalization Rate

</td><td>

Software Discovery Models \[cmdb\_sam\_sw\_discovery\_model\]

</td></tr><tr><td>

Normalization suggestions

</td><td>

Normalization Suggestions \[samp\_normalization\_suggestion\]

</td></tr><tr><td colspan="2">

**Maintenance inputs**

</td></tr><tr><td>

Remediation options

</td><td>

Remediation Options \[samp\_remediation\_option\]

</td></tr><tr><td>

End of Life

</td><td>

Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\]

</td></tr><tr><td>

Missing end of life dates

</td><td>

Software Lifecycle Report \[sam\_sw\_product\_lifecycle\_report\]

</td></tr><tr><td>

Expiring entitlements

</td><td>

Software Entitlements \[alm\_license\]

</td></tr><tr><td colspan="2">

**Optimization inputs**

</td></tr><tr><td>

Removal candidates

</td><td>

Removal Candidates \[samp\_sw\_reclamation\_candidate\]

</td></tr><tr><td>

Optimization \(Microsoft\):

-   Inactive subscriptions
-   Unassigned subscriptions
-   Licensing optimizations

</td><td>

Software Subscriptions \[samp\_sw\_subscription\]

 Purchased Subscription Details \[samp\_purchased\_subscription\_details\]

 Microsoft Core License Optimization Reports \[samp\_ms\_optimization\_report\]

</td></tr><tr><td>

Optimization \(Adobe\):

-   Inactive users
-   Unresolved subscriptions

</td><td>

Software Subscriptions \[samp\_sw\_subscription\]

</td></tr><tr><td>

Optimization \(Red Hat\): Licensing optimizations

</td><td>

Potential savings by optimizing licenses \[samp\_license\_optimization\_summary\]

</td></tr><tr><td>

Optimization \(SAP\):

-   Inactive users
-   Named user assignment
-   Locked out user
-   Licensed non-dialog users
-   Role based license optimization
-   Transaction based license optimization
-   Unused engines

</td><td>

SAP System Users \[samp\_sap\_system\_user\]

 License Metric Results \[samp\_license\_metric\_result\]

 Removal Candidates \[samp\_sw\_reclamation\_candidate\]

</td></tr></tbody>
</table>## SaaS user resolution skill

The following table lists the trigger for the SaaS user resolution skill.

<table id="table_vjv_3gn_dhc"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Auto triggered

</td><td>

User resolution rules are automatically generated upon the activation of the SaaS user resolution skill.

</td></tr></tbody>
</table>The following table lists the inputs for the SaaS user resolution skill.

|Input|Description|
|-----|-----------|
|List of fields with the **String** and **Email** type.|User \[sys\_user\]|

## Contract entitlement data extraction skill

<table id="table_r52_v2r_2hc"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User triggered

</td><td>

An entitlement is automatically generated from a contract when the user manually triggers the skill by selecting **Import contract document** in the software contract page.

</td></tr></tbody>
</table>The following table lists the inputs for the Contract entitlement data extraction skill.

|Input|Description|
|-----|-----------|
|The contract document|The contract document that the user uploads that is used for extracting the entitlement information.|

**Parent Topic:**[Configuring Now Assist for Software Asset Management \(SAM\)](../task/configure-now-assist-sam.md)

