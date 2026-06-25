---
title: Summarize a case by using Now Assist for Customer Service Management \(CSM\)
description: Generate a summary from the fields that you selected on the case record and quickly understand the case context by using the case summarization skill in the Now Assist for Customer Service Management \(CSM\) application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/now-assist-csm-summarize-case.html
release: australia
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI, Now Assist for CSM, Customer Service Management]
---

# Summarize a case by using Now Assist for Customer Service Management \(CSM\)

Generate a summary from the fields that you selected on the case record and quickly understand the case context by using the case summarization skill in the Now Assist for Customer Service Management \(CSM\) application.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

The case summarization skill provides you with a concise summary of a customer service case, including the issue, actions taken, and resolution details. With this skill, you can do the following tasks:

-   Generate an initial summary of a case so that you can understand the case context.
-   Summarize all the work that has been done on a case.

The case summarization skill is available in CSM Configurable Workspace and in Core UI.

-   In CSM Configurable Workspace, you use the Case summary by Now Assist component to generate a summary. This component appears before the activity stream.

    **Note:** You can also generate a case summary on demand from the Now Assist panel.

-   In Core UI, you select the **Summarize** button on the case record to generate a summary.

The case summarization skill checks the case record to determine if there’s enough information available to create a summary:

-   When an agent opens the case record
-   When an agent refreshes the case record page

If there’s enough data the Case summary component displays the **Summarize** button. If there isn’t enough data, the component displays a message in place of the button.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM Configurable Workspace** and open a customer service case.

2.  In the Case insights section by Now Assist component, select **Generate**.

    The Case insights section by Now Assist component appears above the activity stream. When automatic triggering is enabled for case summarization, the system proactively generates a summary when a case is opened. When automatic triggering is turned off, **Generate** button is displayed, enabling agents to generate the summary on demand. The case summary appears in the **Case insights** section, which provides a consolidated view of key information—including the reported issue, actions taken, Service Level Agreement \(SLA\) details, and a trending topic banner when applicable. The **Case insights** section contains the following additional details:

    -   **Customer summary**- Displays key account details including lifetime value, plan type, average handling time, and iCSAT score. Also shows the number of recent cases and interactions, recent issue history. There are links to navigate to all case and all interactions.
    -   **Special handling notes**- Creates notes that bring important information about individual records, such as a case or account record, to the user's attention.
    -   Feedback icons- Copy, thumbs up, thumbs down, and a more options menu.
    -   Access to the most needed information is displayed as buttons links- **Show similar resolved issues** and **Summarize customer’s recent history**.
    -   **Ask AI** button- Opens an AI prompt for follow-up questions in the Now Assist panel, with a drop down arrow for additional options

        **Note:** When the **Provide customer 360 insights** AI agent workflow is enabled in the Now Assist panel, the **Ask AI** button is visible. When the AI agent workflow is turned off, the **Ask AI** button is hidden.

    The **Case insights** section is visible on the record form only when the case summarization skill is active. When the skill is inactive, the card is hidden from the agent workspace.The component is collapsed by default and expands to display the summary. For longer summaries that don't fit in the window, select **View more** and use the scroll bar to view the rest of the content.

    **Note:**

    -   The case summary card is available in CSM Configurable Workspace version 26.1.0 and earlier.
    -   The **Case insight** section, which displays insights about the case, is available in CSM Configurable Workspace version 26.1.1 or later.
    -   Generating and displaying the summary may take several seconds.
    \[Omitted image "now-assist-csm-case-summary.png"\] Alt text: AI-generated case summary for a case record.

3.  After summarizing a case, you can add it to the case work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d156876e279">

Option

</th><th align="left" id="d156876e282">

Procedure

</th></tr></thead><tbody><tr><td id="d156876e288">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share as Work notes**.
2.  In the Share Case summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d156876e315">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(\[Omitted image "icon-expand.png"\] Alt text: Expand card icon.\) or the collapse card icon \(\[Omitted image "icon-collapse.png"\] Alt text: Collapse card icon.\) to see more details or fewer summary details.

</td></tr><tr><td id="d156876e336">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\). If you think that the summary wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).This feedback improves the generative AI model and can help to improve the future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr><tr><td id="d156876e359">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d156876e375">

**View the information about the case summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(\[Omitted image "circle-info-outline-24.svg"\] Alt text: More info icon.\).

</td></tr><tr><td id="d156876e390">

**Ask AI**

</td><td>

The **Ask A** button enables you to ask questions in natural language and receive context‑aware answers, summaries, insights, or actions without navigating away from the page.

 When you select Ask AI:

-   When you select the **Ask AI** drop-down, a menu displays the top 4 related questions:**Identify potential root cause**, **Recommend resolution steps**, **Show similar resolved cases** and **Show similar open issues**.
-   When you select a question, the Now Assist panel opens. The system triggers the [Provide customer 360 insights AI agent workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/customer-service-management-ai-agent-collection-customer-360.md), which retrieves answers based on the context of the current case.
 **Note:**

-   When the **Provide customer 360 insights** AI agent workflow is enabled in the Now Assist panel, the **Ask AI** button is visible. When the AI agent workflow is turned off, the **Ask AI** button is hidden.
-   When an agent selects the **Ask AI** button, the Now Assist panel opens and initiates the **Provide customer 360 insights** AI agent workflow without a template question. The panel returns a general summary of the case, which is the same output produced when an agent selects the **Provide customer 360 insights** pill directly in Now Assist panel. Agents can then submit follow-up questions within the panel.
-   When an agent selects a preset question from the **Ask AI** drop-down, Now Assist panel opens and initiates the **Provide customer 360 insights** AI agent workflow with the selected question. The panel returns a response specific to that question. Agents can then submit follow-up questions within the panel.
-   To customize Ask AI drop-down menu and quick questions, see [Customize Case Insights Ask AI button system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/customize-ask-ai-system-properties.md)


</td></tr></tbody>
</table>
**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-using.md)

**Related topics**  


[Configure Case Summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/now-assist-for-csm/case-summarization-generation-in-now-assist.md)

