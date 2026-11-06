---
title: Recommended actions skill - Triggers and Inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate recommended actions. A trigger initiates an action, such as when the system generates recommended actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/recommended-actions-triggers-inputs.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management, Asset Management]
---

# Recommended actions skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate recommended actions. A trigger initiates an action, such as when the system generates recommended actions.

## Triggers for recommended actions skill

The following table lists the triggers that determine when recommended actions are generated and how the list of recommended actions is displayed.

<table id="table_triggers_ras"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User-triggered

</td><td>

Recommended actions is generated when the user manually triggers the skill by selecting either of the two options in the Publisher details page:

 -   Get recommendations icon on Recommended actions sidebar and then select **Get recommendations**.
-   **Summarize** button for a product. When you select **Summarize**, both the product summary along recommended actions gets generated.

</td></tr></tbody>
</table>## Inputs for the recommended actions skill

The following table lists the inputs for the recommended actions skill.

<table id="table_inputs_ras"><thead><tr><th>

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
</table>**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/references.md)

