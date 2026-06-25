---
title: Summarize a workplace case using Now Assist for WSD
description: Use the case summarization skill to summarize the case context and take appropriate action.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/now-assist-for-wsd/summarize-workplace-case.html
release: australia
product: Now Assist for WSD
classification: now-assist-for-wsd
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Now Assist for Workplace Service Delivery \(WSD\), Workplace Service Delivery, Employee Service Management]
---

# Summarize a workplace case using Now Assist for WSD

Use the case summarization skill to summarize the case context and take appropriate action.

## Before you begin

Role required: sn\_wsd\_case.workplace\_agent

## About this task

As an admin, you can configure the Workplace Case Summarization skill to customize the input fields and output summary. For more information about customizing the skill, see [Configure the Workplace Case Summarization Skill](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/now-assist-for-wsd/customize-workplace-summarization.md).

You can use the case summarization skill in either Core UI or Workplace Central.

-   In Core UI, the summary appears in a banner in the case record.
-   In Workplace Central, the summary is generated in the **Details** tab.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

## Procedure

1.  Navigate to **All** &gt; **Workplace Central** &gt; **Workplace Central**.

    You can also open Workplace Central from the Employee Center directly. Navigate to **Workspaces** &gt; **Workplace Central**.

    The Workplace Analytics dashboard opens.

2.  Select the **Case Management** icon \(\[Omitted image "casemgmt-icon.png"\] Alt text: Case Management icon.\).

    The Case Management dashboard opens.

3.  Select a case from the **Overview** section or the **All active cases** section.

    The list view displays the cases as WCASEXXXX for normal workplace cases, WMCXXXX for maintenance cases and WMOVEXXXX for move cases.

    The case details are displayed in a new tab. For more information about the Case details page, see [Case Management - Key features, Actions &amp; Case details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-central/case-management-key-features-actions-case-details.md) topic.

4.  In the Workplace Case summary by Now Assist component, select **Summarize**.

    **Note:** Generating the summary may take several seconds.

5.  When you finish summarizing a case, you can add it to the work notes, expand or collapse it, provide feedback, copy it, or view information about it.

<table id="choicetable_md1_nyf_xyb"><thead><tr><th align="left" id="d254042e211">

Option

</th><th align="left" id="d254042e214">

Procedure

</th></tr></thead><tbody><tr><td id="d254042e220">

**Save the summary information by adding it to the case work notes**

</td><td>

1.  Select **Share**.
2.  In the **Share to work notes** dialog box, edit the summary.
3.  Select **Save to Work notes**.


</td></tr><tr><td id="d254042e250">

**Expand or collapse the summary**

</td><td>

Select the **Show more** or **Show less** button to see more or fewer summary details.

</td></tr><tr><td id="d254042e265">

**Provide feedback for the summary**

</td><td>

If you think that the summary was helpful, select the helpful icon \(\[Omitted image "icon-helpful.png"\] Alt text: Helpful icon.\). If you think that the summary wasn’t helpful, select the not helpful icon \(\[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.\).This feedback improves the generative AI model and can help to improve the future versions of this skill.

</td></tr><tr><td id="d254042e288">

**Copy the case summary**

</td><td>

Select the copy icon \(\[Omitted image "icon-copy.png"\] Alt text: Copy to clipboard icon.\) to use the case summary information for another purpose, such as pasting into an email.

</td></tr><tr><td id="d254042e304">

**View the information about the case summary**

</td><td>

If you want to check some details about the summary, select the more info icon \(\[Omitted image "icon-more-info.png"\] Alt text: More info icon.\).

</td></tr></tbody>
</table>
