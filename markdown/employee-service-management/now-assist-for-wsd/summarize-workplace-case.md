---
title: Summarize a workplace case using Now Assist for WSD
description: Use the workplace case summarization skill to summarize the case context and take appropriate action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-wsd/summarize-workplace-case.html
release: zurich
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2026-02-10"
reading_time_minutes: 2
breadcrumb: [Using Now Assist for WSD, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Summarize a workplace case using Now Assist for WSD

Use the workplace case summarization skill to summarize the case context and take appropriate action.

## Before you begin

Role required: sn\_wsd\_case.workplace\_agent

## About this task

As an admin, you can configure the workplace case summarization skill to customize the input fields and output summary. For more information about customizing the skill, see [Configure the workplace case summarization skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-wsd/customize-workplace-summarization.md).

You can use the workplace case summarization skill in either the Core UI or Workplace Central.

-   In the Core UI, the summary appears in a banner in the case record.
-   In Workplace Central, the summary is generated in the **Details** tab.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

    You can also open Workplace Central from the Employee Center directly by navigating to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  Select the **Case Management** icon \[Omitted image "casemgmt-icon.png"\] Alt text:.

3.  On the Case Management dashboard, select a case from the Overview section or the All active cases section.

    The list view displays the cases as WCASEXXXX for normal workplace cases, WMCXXXX for maintenance cases, and WMOVEXXXX for move cases.

    The case details are displayed in a new tab. For more information about the Case details page, see [Case Management - Key features, Actions &amp; Case details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/workplace-central/case-management-key-features-actions-case-details.md) topic.

4.  In the Workplace Case summary by Now Assist component, select **Summarize**.

    **Note:** Generating the summary may take several seconds.

5.  When you finish summarizing a case, you can add it to the work notes, expand or collapse it, provide feedback, copy it, or view information about the case.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d234068e201">

Option

</th><th align="left" id="d234068e204">

Procedure

</th></tr></thead><tbody><tr><td id="d234068e210">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share**.
2.  In the Share to work notes dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d234068e237">

**Expand or collapse the summary**

</td><td>

Select **Show more** or **Show less** to see more or fewer summary details.

</td></tr><tr><td id="d234068e252">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \[Omitted image "icon-helpful.png"\] Alt text:. If you think that the summary wasn’t helpful, select the not helpful icon \[Omitted image "icon-not-helpful.png"\] Alt text:.This feedback improves the generative AI model and can help to improve the future versions of this skill.

</td></tr><tr><td id="d234068e273">

**Copy the case summary**

</td><td>

Select the copy icon \[Omitted image "icon-copy.png"\] Alt text: to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d234068e288">

**View the information about the case summary**

</td><td>

If you want to check some details about the summary, select the more info icon \[Omitted image "icon-more-info.png"\] Alt text:.

</td></tr></tbody>
</table>
