---
title: Generate recommended actions for products by using ServiceNow Otto for Software Asset Management \(SAM\)
description: Generate a list of recommended actions to manage software license compliance and optimize licensing spend. The recommended actions help you to take appropriate steps to fix any configuration, maintenance, and optimization issues.Triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate recommended actions. A trigger initiates an action, such as when the system generates recommended actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/recommended-actions-now-assist-sam.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Use generative AI skills, Using AI in Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Generate recommended actions for products by using ServiceNow Otto for Software Asset Management \(SAM\)

Generate a list of recommended actions to manage software license compliance and optimize licensing spend. The recommended actions help you to take appropriate steps to fix any configuration, maintenance, and optimization issues.

## Before you begin

To generate recommended actions for products, select the **Display** toggle button on the **Choose where to display** page while you configure ServiceNow Otto for SAM. For details on the **Display** toggle button, see [Configuring ServiceNow Otto for Software Asset Management \(SAM\) skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-now-assist-sam.md).

Before you use the Recommended actions skill, install the following plugin and the store apps that match your platform release version.

<table id="table_g1b_jrs_1lc"><thead><tr><th>

Platform release

</th><th>

Plugin

</th><th>

Store apps

</th></tr></thead><tbody><tr><td>

Zurich or later releases

</td><td>

Software Asset Management Professional \[com.snc.samp\]

</td><td>

-   ServiceNow Otto for Software Asset Management \(SAM\) \[sn\_now\_assist\_sam\] - 3.3.0 or later
-   Software Asset Workspace \[sn\_sam\_workspace\] - 9.0.4 or later

</td></tr></tbody>
</table>Role required: sam\_user

## About this task

**Note:** The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

Starting with the Australia Patch 4 release, AWS Claude is the default model provider for the Recommended actions generative AI skill.

ServiceNow Otto for SAM generates the recommended actions for products by using reconciliation results, product life-cycle reports, and dashboards such as Discovered inventory, Normalization and content, and Health check.

**Note:** Health check details are shown only for Windows Server, SQL Server, and Oracle Database.

Use a product summary and its recommended actions to decide which follow-up steps a product needs.

When you run reconciliation with grouping, product summarization and recommended actions are available only for the parent product results, not for the individual child product results.

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  Select the License usage view.

3.  Select a publisher.

4.  On the Publisher details page, select a product for the publisher.

5.  Select **Summarize** or the Recommended actions icon on the right hand side of the page and then select **Get recommendations**.

    ServiceNow Otto for SAM application starts generating recommended actions for the selected product. After the recommended actions are generated, the results appear as cards under the following three categories:

    -   Configuration
    -   Maintenance
    -   Optimization
    \[Omitted image "now-assist-sam-recommended-actions.png"\] Alt text: List of recommended actions for a product

    The compiled results can differ from product to product based on the current compliance level of a product.

    Recommended actions are generated even if a product is fully compliant. Recommended actions are generated if there are any actions related to health issues, maintenance or optimization.

6.  Select a button on a card to view the list view page for that action.

    After the recommended actions are generated, the results aren't automatically saved. If you close the Publisher details page where you generated the recommended actions, or if you reload the page, the results aren't available.

7.  You can perform the following actions on the generated recommended actions.

<table id="choicetable_swv_41f_f2c"><thead><tr><th align="left" id="d303038e290">

Action

</th><th align="left" id="d303038e293">

Description

</th></tr></thead><tbody><tr><td id="d303038e299">

**Regenerate icon**

</td><td>

Regenerates the list of recommended actions.

 You can find this icon in the top right corner of the Recommended actions box.

</td></tr><tr><td id="d303038e314">

**Feedback**

</td><td>

If you found that the recommended actions was helpful, select the helpful icon. If you found that the recommended actions wasn't helpful, select the not helpful icon.

 You can find these icons at the bottom of the Recommended Actions box.

 This feedback improves the generative AI model and can help to improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>8.  Select the Dismiss icon to dismiss an action; whether you have resolved the action or decided not to work on the action.

    Once you have dismissed all the actions, a message appears mentioning that all recommendations have been dismissed.


**Parent Topic:**[Using generative AI skills in ServiceNow Otto for Software Asset Management \(SAM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/using-now-assist-sam.md)

## Recommended actions skill - Triggers and Inputs

Triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate recommended actions. A trigger initiates an action, such as when the system generates recommended actions.

### Triggers for recommended actions skill

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
</table>### Inputs for the recommended actions skill

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
</table>