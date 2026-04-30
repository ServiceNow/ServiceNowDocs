---
title: Summarize test for a technology product support case using Now Assist for Telecommunications, Media and Technology \(TMT\)
description: Generate the test run summary for a technology product support case record to understand the context of test outcomes and the root cause of the problem.
locale: en-US
release: zurich
product: Now Assist for Telecom, Media and Technology
classification: now-assist-for-telecom-media-and-technology
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Use generative AI skills, Now Assist for TMT, Telecommunications, Media, and Technology \(TMT\)]
---

# Summarize test for a technology product support case using Now Assist for Telecommunications, Media and Technology \(TMT\)

Generate the test run summary for a technology product support case record to understand the context of test outcomes and the root cause of the problem.

## Before you begin

Role required: sn\_customerservice\_agent and sn\_customerservice.consumer\_agent

## About this task

The test summarization skill provides you with a concise summary of the test executed for a technology product support case, including the test outcome, test interpretation, and other parameters configured for the specific test definition. With this skill, you can generate the test summary of a technology product support case so that you can analyze the root cause of the problem.

The test summarization skill is available in CSM/FSM Configurable Workspace and in Core UI.

-   In CSM/FSM Configurable Workspace, you use the Test Run summary by Now Assist component to generate a summary. This component appears in the test results record.
-   In Core UI, you select the **Summarize** button on the test result record to generate a summary.

The test summarization skill checks the test results record to determine if there’s enough information available to create a summary. If there’s enough data, the Test summary component displays the **Summarize** button. If there isn’t enough data to generate a summary, the system displays a message in the Test summary component field.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** &gt; **Lists** &gt; **Technology Product Support Case**.

2.  Open a technology product support case.

    If there are no test results available, run the tests to get test results.

3.  In the **Troubleshoot** tab, select **Test results**.

    ![Hi-tech test.](../image/test-result-hi-tech-cases.png)

4.  Identify the test result that you want to open and select the View Details icon \(![View details](../image/mab-icon-launch-weblink-sol.png)\)

5.  In the Test Run summary by Now Assist component, select **Summarize**.

    ![Summarize the hi-tech test.](../image/test-result-summarize-hi-tech-cases.png)

    The Test Run summary by Now Assist component appears in the test result record. The component is collapsed by default and expands to display the summary. For longer summaries that don't fit in the window, select **View more** and use the scroll bar to view the rest of the content.

    **Note:** Generating and displaying the summary may take several seconds.

6.  After you're finished summarizing the test for the technology product support case, manage the results.

<table id="choicetable_ebh_5tm_vdc"><thead><tr><th align="left" id="d28093e198">

Option

</th><th align="left" id="d28093e201">

Procedure

</th></tr></thead><tbody><tr><td id="d28093e207">

**Expand or collapse the summary**

</td><td>

-   See more summary details by selecting the expand card icon \(![Expand card icon.](../image/icon-expand.png)\).
-   See fewer summary details by selecting the collapse card icon \(![Collapse card icon.](../image/icon-collapse.png)\).


</td></tr><tr><td id="d28093e237">

**Provide feedback for the summary**

</td><td>

-   If you think that the summary was helpful, select the helpful icon \(![Helpful icon.](../image/icon-helpful.png)\).
-   If you think that the summary wasn’t helpful, select the not helpful icon \(![Not helpful icon.](../image/icon-not-helpful.png)\).
 This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d28093e270">

**Copy the test summary**

</td><td>

Select the copy to clipboard icon \(![Copy to clipboard icon.](../image/icon-copy.png)\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d28093e285">

**Refresh the test summary**

</td><td>

Fetch the latest test run summary by selecting the refresh icon \(![Refresh test summary](../image/refresh-sync-new.png)\).

</td></tr></tbody>
</table>7.  Set the test result to either fail or pass by selecting the **Set result**.

8.  Save or cancel the results.

    -   To set the results, select **Save**.
    -   To go back to the test results list, select **Cancel**.

**Parent Topic:**[Using Now Assist for Telecommunications, Media and Technology \(TMT\)](../concept/now-assist-spm-using.md)

