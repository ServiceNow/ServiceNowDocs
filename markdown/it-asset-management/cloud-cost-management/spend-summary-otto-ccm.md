---
title: Analyze cloud spend using the Cloud cost summarizer generative AI skill
description: View actionable optimization insights with a comprehensive AI-generated summary of your cloud spend trends, top cost drivers, and budget alignment with your selected filters and groupings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/spend-summary-otto-ccm.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2026-08-10"
reading_time_minutes: 1
breadcrumb: [Use, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Analyze cloud spend using the Cloud cost summarizer generative AI skill

View actionable optimization insights with a comprehensive AI-generated summary of your cloud spend trends, top cost drivers, and budget alignment with your selected filters and groupings.

## Before you begin

All the required plugins must be installed for the Cloud cost summarizer generative AI skill to function smoothly. For more details, see [Supported version and required plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/supporting-info-ai-ccm.md).

Role required: insights\_admin

## About this task

**Important:** This generative AI skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [AI agents, skills, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-skills-on-by-default.md).

The Cloud cost summarizer generative AI skill generates comprehensive summary of your cloud spend trends across cloud providers, top cost drivers, and optimization recommendations. The summary displays month-over-month and year-over-year changes, commitment coverage, and the top five recommendations to reduce costs. These insights help you to make more informed decisions about your cloud spend.

## Procedure

1.  Navigate to **Workspaces** &gt; **Cloud Cost Management Workspace**.

2.  Select **Cloud cost overview**.

3.  In the Monthly spend breakdown report, select appropriate values in the **Group by**, **Time range**, and **Cost type** fields.

4.  Select **Summarize**.

    A spend summary card of your cloud spend trends, top cost drivers, and actionable optimization recommendations is displayed.

5.  You can perform the following actions on the generated summary.

<table id="choicetable_swv_41f_f2c"><thead><tr><th align="left" id="d106019e136">

Action

</th><th align="left" id="d106019e139">

Description

</th></tr></thead><tbody><tr><td id="d106019e145">

**Copy to clipboard icon**

</td><td>

Copies the summary to a clipboard.

</td></tr><tr><td id="d106019e154">

**Refresh icon**

</td><td>

Regenerates the publisher summary.

</td></tr><tr><td id="d106019e163">

**Feedback**

</td><td>

If you found that the summary was helpful, select the helpful icon \[Omitted image "icon-helpful.png"\] Alt text: Helpful icon. If you found that the summary wasn't helpful, select the not helpful icon \[Omitted image "icon-not-helpful.png"\] Alt text: Not helpful icon.This feedback improves the generative AI model and can help to improve future versions of this skill. The system gathers the feedback on each generated summary and stores it in the generative AI logs \(sys\_generative\_ai\_log\_list.do\).

</td></tr></tbody>
</table>
**Parent Topic:**[Using Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/using-cloud-insights.md)

