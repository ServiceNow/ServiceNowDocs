---
title: Summarize a case by using Now Assist for Supplier Lifecycle Operations \(SLO\) in Source-to-Pay Workspace
description: Summarize supplier-related cases to learn more about their status, progress, and action items by using the supplier case summarization skill in the Now Assist for Supplier Lifecycle Operations \(SLO\) application.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [generative AI, gen AI, genai, artificial intelligence]
breadcrumb: [Use, Now Assist for SLO, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Summarize a case by using Now Assist for Supplier Lifecycle Operations \(SLO\) in Source-to-Pay Workspace

Summarize supplier-related cases to learn more about their status, progress, and action items by using the supplier case summarization skill in the Now Assist for Supplier Lifecycle Operations \(SLO\) application.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

Role required: sn\_supplier\_gen\_ai.now\_assist\_fulfiller

## About this task

You can use the supplier case summarization skill in either Core UI or Source-to-Pay Workspace.

-   In Core UI, the summary appears in a banner in the record.
-   In Source-to-Pay Workspace, the summary is generated in the **Details** tab.

## Procedure

1.  Navigate to **Source-to-Pay Workspace**.

2.  Select the list icon \(![List icon.](../image/cases-list-icon.png)\).

3.  Navigate to **Lists** &gt; **All work** and select either of the following records:

    -   Cases
    -   Closed cases
4.  Under the Number column, select the link to the supplier case.

5.  In the Record summary section, select **Summarize**.

    ![Summarize option in the Source-to-Pay Workspace.](../image/case-summarization.png)

6.  Review the summary details.

    A concise summary of a case includes the overview, actions completed, and next steps. The information that is displayed is based on the type of the case:

    -   **Overview**: Provides information about the case.
    -   **Actions Completed**: Lists all the actions that have been taken so far.
    -   **Next steps**: Lists the actions that the supplier managers must take next.
7.  When you finish summarizing a case, you can add it to the work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d37653e235">

Option

</th><th align="left" id="d37653e238">

Procedure

</th></tr></thead><tbody><tr><td id="d37653e244">

**Save the summary information by adding it to the record work notes**

</td><td>

1.  Select **Share to work notes**.
2.  In the Share to work notes dialog box, edit the summary.
3.  Select **Save to work notes**.


</td></tr><tr><td id="d37653e271">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(![Expand card icon.](../../sourcing-procurement-operations/image/icon-expand.png)\) or the collapse card icon \(![Collapse card icon.](../../sourcing-procurement-operations/image/icon-collapse.png)\) to see more details or fewer summary details.

</td></tr><tr><td id="d37653e292">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../../sourcing-procurement-operations/image/icon-helpful.png)\). If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../../sourcing-procurement-operations/image/icon-not-helpful.png)\).This feedback improves the generative AI model and can help to improve the future versions of this skill.

</td></tr><tr><td id="d37653e315">

**Copy the record summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\) to use the record summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d37653e331">

**View the information about the record summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(![More info icon.](../../sourcing-procurement-operations/image/icon-more-info.png)\).

</td></tr><tr><td id="d37653e346">

**Refresh the record summary**

</td><td>

If you want to refresh the summary, select the refresh icon \(![Refresh icon.](../../sourcing-procurement-operations/image/icon-refresh.png)\).

</td></tr></tbody>
</table>
**Related topics**  


[Use Now Assist for Supplier Lifecycle Operations \(SLO\)](../concept/now-assist-slo-using.md)

[Use Now Assist for Supplier Lifecycle Operations \(SLO\) in a Virtual Agent chat](../concept/now-assist-slo-va.md)

