---
title: Summarize an ER case using ServiceNow Otto for HRSD
description: Use the ER case summarization skill to obtain a comprehensive overview of the ER case, which includes key details such as allegations, evidences, and interviews.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-summarize-er-case.html
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2025-10-28"
reading_time_minutes: 6
breadcrumb: [Use generative AI skills, ServiceNow Otto for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Summarize an ER case using ServiceNow Otto for HRSD

Use the ER case summarization skill to obtain a comprehensive overview of the ER case, which includes key details such as allegations, evidences, and interviews.

## Before you begin

Role required: sn\_hr\_er.case\_writer

## About this task

You can use the ER case summarization skill in either Core UI or Agent Workspace for HR Case Management.

-   In Core UI, the summary appears in a banner in the case record.
-   In Agent Workspace for HR Case Management, the summary is generated in the **Details** tab.

**Note:** For information on how to configure the case summarization skill, see [Configure ServiceNow Otto for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md).

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **HR Agent Workspace**.

2.  In Workspace, open an ER case that is assigned to you.

    Alternatively, you can navigate to **All** &gt; **HR Cases** and select an ER case.

3.  Select **Summarize**.

4.  **Note:** Generating and displaying the summary may take several seconds.

5.  Review the summary details.

    A summary of a case is displayed. The summary varies based on the state of the case:

    -   In **Ready** state: Case Information, Case Overview, Involved Parties, Allegations, and Key Dates are displayed.
    -   In **Work in progress** or **Closed complete** state: Case Information, Case Overview, Involved Parties, Allegations, Interviews Summary, Evidence Summary, Allegation Outcomes, Corrective Actions, and Key Dates are displayed.

        **Note:** Attachment related details are added to the summary only when an attachment is present on ER case irrespective of case state.

    \[Omitted image "er-summarize-aws.png"\] Alt text: ER case summary on Agent Workspace for HR Case Management \[Omitted image "er-summarize-aws1.png"\] Alt text: ER case summary on Agent Workspace for HR Case Management

    \[Omitted image "er-summarize-core.png"\] Alt text: ER case summary on Core UI \[Omitted image "er-summarize-core1.png"\] Alt text: ER case summary on Core UI

6.  When you finish summarizing a case, you can add it to the work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d372647e241">

Option

</th><th align="left" id="d372647e244">

Procedure

</th></tr></thead><tbody><tr><td id="d372647e250">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share**.
2.  In the Share Case summary as Work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d372647e277">

**Expand or collapse the summary**

</td><td>

Select the expand card icon \(\[Omitted image "icon-expand.png"\] Alt text: Expand card icon.\) or the collapse card icon \(\[Omitted image "icon-collapse.png"\] Alt text: Collapse card icon.\) to see more details or fewer summary details.

</td></tr><tr><td id="d372647e298">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\). If you think that the summary wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).This feedback improves the generative AI model and can help to improve the future versions of this skill.

</td></tr><tr><td id="d372647e321">

**Copy the case summary**

</td><td>

Select the copy to clipboard icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d372647e337">

**View the information about the case summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text: More info icon.\).

</td></tr><tr><td id="d372647e352">

**Refine list**

</td><td>

Elaborate or shorten the summary.

</td></tr></tbody>
</table>
**Parent Topic:**[Using ServiceNow Otto for HR Service Delivery \(HRSD\) in Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-hrsd/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation using ServiceNow Otto for HR Service Delivery \(HRSD\)]()

[Summarize a Sidebar discussion by using ServiceNow Otto for HRSD]()

[Generate a chat reply recommendation by using ServiceNow Otto for HRSD]()

[Generate a knowledge article from HR Agent Workspace with ServiceNow Otto for HRSD]()

[Generate a knowledge article from multiple cases]()

[Generate an email reply recommendation using ServiceNow Otto for HRSD]()

[Summarize an HR case using ServiceNow Otto for HRSD]()

[Summarize an ER case interview using ServiceNow Otto for HRSD]()

[Generate resolution notes using ServiceNow Otto for HRSD]()

[View employee summary reports]()

[Summarize actions while transferring an HR case]()

[Use Knowledge Graph in ServiceNow Otto for HRSD]()

[Use ServiceNow Otto for HRSD – Galileo Inside to answer HR-related questions]()

[Use the ServiceNow Otto panel in HR Agent Workspace]()

[Submit an HR request with Gen AI Virtual Agent]()

[ServiceNow Otto for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework]()

[Analyze sentiments in ServiceNow Otto for HR Service Delivery \(HRSD\)]()

