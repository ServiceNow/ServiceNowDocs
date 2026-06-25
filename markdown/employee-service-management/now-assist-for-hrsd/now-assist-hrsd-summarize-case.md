---
title: Summarize an HR case using Now Assist for HRSD
description: Quickly understand the case context and respond to inquiries by using the case summarization skill.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-hrsd/now-assist-hrsd-summarize-case.html
release: australia
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use generative AI skills, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Summarize an HR case using Now Assist for HRSD

Quickly understand the case context and respond to inquiries by using the case summarization skill.

## Before you begin

[Configure Now Assist for HR Service Delivery \(HRSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/configure-now-assist-hr.md).

Role required: sn\_hr\_core.case\_writer

## About this task

You can use the case summarization skill in either Core UI or Agent Workspace for HR Case Management.

-   In Core UI, the summary appears in a banner in the case record.
-   In Agent Workspace for HR Case Management, the summary is generated in the **Details** tab.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

You can make a copy of this skill to configure it to meet your business needs. For more information, see [Make a copy of a Now Assist skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/make-a-copy-of-a-now-assist-skill.md).

## Procedure

1.  Navigate to **Agent Workspace for HRSD**.

2.  In Workspace, open an HR case that is assigned to you.

3.  Select **Summarize**.

4.  Review the summary details.\[Omitted image "case-summarization2.png"\] Alt text: Case summary that is shown in Workspace. It lists the issue and actions taken.

    A concise summary of a case, including the issue, actions taken, SLA, attachments, and resolution information appears. The information that is displayed is based on the state of the case:

    -   Draft or Ready: Issue
    -   Work in progress: Issue and Actions taken
    -   Awaiting acceptance, Awaiting approval, Closed complete, or Closed incomplete: Issue, Actions taken, and Resolution
    -   Canceled or Suspended: Summary isn’t visible
5.  When you finish summarizing a case, you can add it to the work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d499155e191">

Option

</th><th align="left" id="d499155e194">

Procedure

</th></tr></thead><tbody><tr><td id="d499155e200">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share**.
2.  In the **Share to work notes** dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d499155e230">

**Expand or collapse the summary**

</td><td>

Select the **Show more** or **Show less** button to see more or fewer summary details.

</td></tr><tr><td id="d499155e245">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\). If you think that the summary wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).This feedback improves the generative AI model and can help to improve the future versions of this skill.

</td></tr><tr><td id="d499155e268">

**Copy the case summary**

</td><td>

Select the copy icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d499155e284">

**View the information about the case summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text: More info icon.\).

</td></tr></tbody>
</table>
**Parent Topic:**[Use Now Assist for HR Service Delivery \(HRSD\) in Agent Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-hrsd/use-now-assist-hr.md)

**Related topics**  


[Summarize a chat conversation using Now Assist for HR Service Delivery \(HRSD\)]()

[Summarize a Sidebar discussion by using Now Assist for HRSD]()

[Generate a chat reply recommendation by using Now Assist for HRSD]()

[Generate a knowledge article from HR Agent Workspace with Now Assist for HRSD]()

[Generate a knowledge article from multiple cases]()

[Generate an email reply recommendation using Now Assist for HRSD]()

[Generate resolution notes using Now Assist for HRSD]()

[View employee summary reports]()

[Summarize actions while transferring an HR case]()

[Use Knowledge Graph in Now Assist for HRSD]()

[Use Now Assist for HR - Galileo Inside to answer HR-related questions]()

[Use the Now Assist panel in HR Agent Workspace]()

[Submit an HR request with Gen AI Virtual Agent]()

[Now Assist for HR Service Delivery \(HRSD\) integration with Enterprise Service Management Integrations Framework]()

[Analyze sentiments in Now Assist for HR Service Delivery \(HRSD\)]()

