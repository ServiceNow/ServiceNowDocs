---
title: Generate recommended actions for products by using Now Assist for SAM
description: Generate a list of recommended actions to manage software license compliance and optimize licensing spend. The recommended actions help you to take appropriate steps to fix any configuration, maintenance, and optimization issues.
locale: en-US
release: australia
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Generate recommended actions for products by using Now Assist for SAM

Generate a list of recommended actions to manage software license compliance and optimize licensing spend. The recommended actions help you to take appropriate steps to fix any configuration, maintenance, and optimization issues.

## Before you begin

Role required: sam\_user

## About this task

Now Assist for SAM generates the recommended actions for products by using reconciliation results, product life-cycle reports, and dashboards such as Discovered inventory, Normalization and content, and Health check.

**Note:** Health check details are shown only for Windows Server, SQL Server, and Oracle Database.

When you run reconciliation with grouping, product summarization and recommended actions are available only for the parent product results, not for the individual child product results.

## Procedure

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.

2.  Select the License usage view.

3.  Select a publisher.

4.  On the Publisher details page, select a product for the publisher.

5.  Select **Summarize** or the Recommended actions icon on the right hand side of the page and then select **Get recommendations**.

    Now Assist for SAM application starts generating recommended actions for the selected product. After the recommended actions are generated, the results appear as cards under the following three categories:

    -   Configuration
    -   Maintenance
    -   Optimization
    ![List of recommended actions for a product](../image/now-assist-sam-recommended-actions.png)

    The compiled results can differ from product to product based on the current compliance level of a product.

    Recommended actions are generated even if a product is fully compliant. Recommended actions are generated if there are any actions related to health issues, maintenance or optimization.

6.  Select a button on a card to view the list view page for that action.

    After the recommended actions are generated, the results aren't automatically saved. If you close the Publisher details page where you generated the recommended actions, or if you reload the page, the results aren't available.

7.  You can perform the following actions on the generated recommended actions.

<table id="choicetable_swv_41f_f2c"><thead><tr><th align="left" id="d213135e162">

Action

</th><th align="left" id="d213135e165">

Description

</th></tr></thead><tbody><tr><td id="d213135e171">

**Regenerate icon**

</td><td>

Regenerates the list of recommended actions.

 You can find this icon in the top right corner of the Recommended actions box.

</td></tr><tr><td id="d213135e186">

**Feedback**

</td><td>

If you found that the recommended actions was helpful, select the helpful icon. If you found that the recommended actions wasn't helpful, select the not helpful icon.

 You can find these icons at the bottom of the Recommended Actions box.

 This feedback improves the generative AI model and can help to improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>8.  Select the Dismiss icon to dismiss an action; whether you have resolved the action or decided not to work on the action.

    Once you have dismissed all the actions, a message appears mentioning that all recommendations have been dismissed.


**Parent Topic:**[Using generative AI skills in Now Assist for SAM](../concept/using-now-assist-sam.md)

