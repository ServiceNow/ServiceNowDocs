---
title: Summarize case insights by using Now Assist for Customer Service Management \(CSM\)
description: Use Now Assist for Customer Service Management \(CSM\) to generate a consolidated view of case insights directly from the case record. The Case Insights section surfaces a summary of the case alongside key contextual information to help service reps understand and act on cases quickly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/now-assist-csm-summarize-case.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Use generative AI skills, Now Assist for CSM, Customer Service Management]
---

# Summarize case insights by using Now Assist for Customer Service Management \(CSM\)

Use Now Assist for Customer Service Management \(CSM\) to generate a consolidated view of case insights directly from the case record. The **Case Insights** section surfaces a summary of the case alongside key contextual information to help service reps understand and act on cases quickly.

## Before you begin

\[Omitted image "now-assist-csm-case-summary.png"\] Alt text: AI-generated case summary for a case record.

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

The **Case Insights** section requires the case summarization skill to be enabled. [Customer summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-customer-summarization-in-now-assist-for-csm.md) and [Special handling notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-special-handling-notes-summarization-in-now-assist-for-csm.md) must be active to enable all sections. The **Case Insights** section is available in the CSM default record page and front line record page in the CSM Configurable Workspace version 26.1.1 and later. Earlier version was **Case summary** and is available in CSM Configurable Workspace version 26.1.0 and earlier.

## About this task

When a customer service agent opens a case or navigates to the case record page, Now Assist checks whether there is enough information to generate a summary. If there is, the **Summarize** button appears. If not, the component displays a message instead.

The **Case Insights** section includes:

-   **Banner**: Shows SLA status and trending topic information.
-   **Case summary**: A generated summary of the case including the reported issue, actions taken, Service Level Agreement \(SLA\) details, and a trending topic banner when applicable.
-   **Customer summary**- Key account details including lifetime value, plan type, average handling time, and CSAT score. Also shows the number of recent cases and interactions, recent issue history, and links to navigate to all cases and interactions.
-   **Special handling notes**- Notes that bring important information about individual records, such as a case or account record, to the service rep's attention.
-   **Ask AI**- An open prompt for follow-up questions in the Now Assist panel, with a drop-down for additional options.

    **Note:**

    -   When the [Provide customer 360 insights AI agent workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/customer-service-management-ai-agent-collection-customer-360.md) is enabled in the Now Assist panel, the **Ask AI** button is visible. When the AI agent workflow is turned off, the **Ask AI** button is hidden.
    -   When an agent selects the **Ask AI** button, the Now Assist panel opens and initiates the **Provide customer 360 insights** AI agent workflow without a template question. The panel returns a general summary of the case, which is the same output produced when an agent selects the **Provide customer 360 insights** pill directly in Now Assist panel. Agents can then submit follow-up questions within the panel.
    -   When an agent selects a preset question from the **Ask AI** drop-down, Now Assist panel opens and initiates the **Provide customer 360 insights** AI agent workflow with the selected question. The panel returns a response specific to that question. Agents can then submit follow-up questions within the panel.
    -   To customize Ask AI drop-down menu and quick questions, see [Customize Case Insights Ask AI button system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/customize-ask-ai-system-properties.md)

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM Configurable Workspace** and open a customer service case.

2.  In the **Case Insights** section, select **Generate**.

    -   If automatic triggering is enabled, Now Assist generates the summary automatically when the case is opened.
    -   If automatic triggering is off, the **Summarize** button appears and service agent can generate the summary on demand.
3.  The **Case Insights** section displays the summary.

    -   Generating and displaying the summary may take several seconds.
    -   The section is collapsed by default on the record form- select **View more** and use the scroll bar to view the rest.
4.  After generating case insights, you can take any of the following actions:

    -   Copy the case summary: Select the copy to clipboard icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\) to use the case summary information for another purpose, such as pasting into an email.
    -   Provide feedback:
        -   Select the helpful icon \( \[Omitted image "icon-helpful.png"\] Alt text: Helpful icon\) or the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon. \).
        -   This feedback improves the generative AI model and can help to improve the future versions of this skill. The system stores feedback in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).
    -   Ask follow-up questions:
        -   Select the **Ask AI** button to open the Now Assist panel and view key findings, or
        -   Select the **Ask AI** drop-down button and select one of the menu options: **Identify potential root cause**, **Recommend resolution steps**, **Show similar resolved cases**, and **Show similar open issues**.
        -   The Now Assist panel opens and triggers the [Provide customer 360 insights AI agent workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/customer-service-management-ai-agent-collection-customer-360.md), which retrieves answers based on the context of the current case.
    -   Expand or collapse the summary: Select the expand card icon \(\[Omitted image "icon-expand.png"\] Alt text: Expand card icon.\) or the collapse card icon \(\[Omitted image "icon-collapse.png"\] Alt text: Collapse card icon.\) to see more details or fewer summary details.

**Parent Topic:**[Using Now Assist for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/now-assist-csm-using.md)

**Related topics**  


[Configure Case Summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/case-summarization-generation-in-now-assist.md)

