---
title: Summarize test for a service problem case using Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Generate the test run summary for a service problem case record to quickly understand the context of test outcomes and the root cause of the problem.
locale: en-US
release: xanadu
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Now Assist for Telecommunications, Media and Technology \(TMT\), Now Assist for Telecommunications, Media and Technology \(TMT\), Telecommunications, Media, and Technology]
---

# Summarize test for a service problem case using Now Assist for Telecommunications, Media and Technology \(TMT\)

Generate the test run summary for a service problem case record to quickly understand the context of test outcomes and the root cause of the problem.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

The test summarization skill provides you with a concise summary of the test executed for a service problem case, including the test outcome, test interpretation, and other parameters configured for the specific test definition. With this skill, you can generate the test summary of a service problem case so that you can analyze the root cause of the problem.

The test summarization skill is available in CSM/FSM Configurable Workspace and in Core UI.

-   In CSM/FSM Configurable Workspace, you use the Test Run summary by Now Assist component to generate a summary. This component appears in the test results record.
-   In Core UI, you select the **Summarize** button on the test result record to generate a summary.

The test summarization skill checks the test results record to determine if there is enough information available to create a summary. If there is enough data, the Test summary component displays the **Summarize** button. If there is not enough data to generate a summary, the system displays a message in the Test summary component field.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Service Problem Case**.

2.  Open a service problem case.

3.  In the **Diagnose** tab, select **Test results**.

4.  Identify the test result that you want to open and select the View Details icon \(![View details](../image/mab-icon-launch-weblink-sol.png)\)

5.  In the Test Run summary by Now Assist component, select **Summarize**.

    The Test Run summary by Now Assist component appears in the test result record. The component is collapsed by default and expands to display the summary. For longer summaries that don't fit in the window, select **View more** and use the scroll bar to view the rest of the content.

    **Note:** Generating and displaying the summary may take several seconds.

6.  After you're finished summarizing the test for the service problem case, manage the results.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d20376e159">

Option

</th><th align="left" id="d20376e162">

Procedure

</th></tr></thead><tbody><tr><td id="d20376e168">

**Expand or collapse the summary**

</td><td>

-   See more summary details by selecting the expand card icon \(![Expand card icon.](../image/icon-expand.png)\).
-   See fewer summary details by selecting the collapse card icon \(![Collapse card icon.](../image/icon-collapse.png)\).


</td></tr><tr><td id="d20376e198">

**Provide feedback for the summary**

</td><td>

-   If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\).
-   If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).
 This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d20376e231">

**Copy the test summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d20376e246">

**Refresh the test summary**

</td><td>

Fetch the latest test run summary by selecting the refresh icon \(![Refresh test summary](../image/refresh-sync-new.png)\).

</td></tr></tbody>
</table>7.  Set the test result to either fail or pass by selecting the **Set result**.

8.  Save or cancel the results.

    -   To set the results, select **Save**.
    -   To go back to the test results list, select **Cancel**.

**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

