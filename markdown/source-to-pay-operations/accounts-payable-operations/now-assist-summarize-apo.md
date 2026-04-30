---
title: Summarize a record by using Now Assist for Accounts Payable Operations \(APO\)
description: Summarize invoice and inquiry cases to learn about their status, progress, and action items by using the record summarization skill in the Now Assist for Accounts Payable Operations \(APO\) application.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Using Now Assist for Accounts Payable Operations \(APO\), Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Summarize a record by using Now Assist for Accounts Payable Operations \(APO\)

Summarize invoice and inquiry cases to learn about their status, progress, and action items by using the record summarization skill in the Now Assist for Accounts Payable Operations \(APO\) application.

## Before you begin

**Important:** The invoice case summarization skill is now turned on by default. The skill will be automatically available to appropriate role users for the application. This change simply activates the skill and does not touch the roles that are needed to use the skill. The new default behavior works as follows:

-   **New customers**

    When you install a Now Assist product, designated skills are turned on automatically.

-   **Existing customers who are upgrading \(starting with Zurich Patch 4\)**

    Any previously unconfigured skill is turned on automatically \(the skill was never turned on, then off again\).

    There is no change to Now Assist skills that are currently enabled and customized.

    Previously configured skills that were turned on, then off, remain inactive.


Role required: sn\_ap\_apm.accounts\_payable\_specialist or sn\_ap\_cm.agent

## About this task

You can use these record summarization skills in either Core UI or Source-to-Pay Workspace.

-   In Core UI, the summary appears in a banner in the record.
-   In Source-to-Pay Workspace, the summary is generated on the **Details** tab.

## Procedure

1.  Navigate to **Source-to-Pay Workspace**.

2.  Select the list icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\).

3.  Generate a summary for either an invoice case record or an inquiry case record.

<table id="choicetable_x5b_1vk_pdc"><thead><tr><th align="left" id="d77067e148">

Option

</th><th align="left" id="d77067e151">

Procedure

</th></tr></thead><tbody><tr><td id="d77067e157">

**Generate a summary for the invoice case record.**

</td><td>

1.  Navigate to **Lists** &gt; **** &gt; **Invoices** &gt; **All invoices**.
2.  Select any invoice and the link to the record under the Number column.
3.  Open an invoice record and select **Cases**.


</td></tr><tr><td id="d77067e195">

**Generate a summary for the inquiry case record.**

</td><td>

1.  Navigate to **Lists** &gt; **** &gt; **All work** &gt; **Cases**.
2.  Select any inquiry case and the link to the record under the Number column.
3.  Open an invoice inquiry record.


</td></tr></tbody>
</table>4.  On the **Cases** tab, in the Record summary section, select **Summarize**.

    ![Summarize option that appears at the top of the record in Source-to-Pay Workspace.](../../source-to-pay-operations/image/record-summarization-apo.png)

    When you opt to summarize an invoice case, you see the following message: "Now Assist is summarizing your invoice case."

    **Note:** Generating and displaying the summary may take several seconds.

5.  Review the summary details.

    ![Summarized invoice case.](../../source-to-pay-operations/image/record-summarization-case-apo.png)

    A concise summary of the record, including the overview, actions completed, and next steps are displayed. The information that is displayed is based on the type of the record.

    -   **Overview**: Provides information about the record.
    -   **Actions Completed**: Lists all the actions that have been taken so far.
    -   **Next steps**: Lists the actions that the AP fulfillers must take next.
6.  When you finish summarizing a record, you can add it to the work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d77067e304">

Option

</th><th align="left" id="d77067e307">

Procedure

</th></tr></thead><tbody><tr><td id="d77067e313">

**Save the summary information by adding it to the recorded work notes**

</td><td>

1.  Select **Share to work notes**.
2.  In the Share to work notes dialog box, edit the summary.
3.  Select **Save to work notes**.![Save to work notes dialog box.](../image/sharetoworknotes-apo.png)


</td></tr><tr><td id="d77067e345">

**Expand or collapse the summary**

</td><td>

Select the expanded card icon \(![Expand card icon.](../../sourcing-procurement-operations/image/icon-expand.png)\) or the collapse card icon \(![Collapse card icon.](../../sourcing-procurement-operations/image/icon-collapse.png)\) to see more details or fewer summary details.

</td></tr><tr><td id="d77067e366">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../../sourcing-procurement-operations/image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../../sourcing-procurement-operations/image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill.

</td></tr><tr><td id="d77067e389">

**Copy the record summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\) to use the record summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d77067e405">

**View the information about the record summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(![More info icon.](../../sourcing-procurement-operations/image/icon-more-info.png)\).

</td></tr></tbody>
</table>
## Result

Invoice cases are summarized in Now Assist for Accounts Payable Operations \(APO\).

**Related topics**  


[Using Invoice Case Management](../concept/use-invoice-case-mgmt.md)

[Using Accounts Payable Invoice Processing](../concept/use-ap-invoice-processing.md)

[Invoice processing cases](../concept/working-with-ingestion-cases.md)

