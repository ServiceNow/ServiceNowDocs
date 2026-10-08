---
title: View your automation opportunities \(Next Experience UI\)
description: Review the automation opportunities that AI Agent Advisor has identified for your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-center-view-automation-opportunities.html
release: brazil
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, AI, AI setup]
breadcrumb: [AI Agent Advisor in AI Admin Center, Use, AI Agent Advisor, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# View your automation opportunities\(Next Experience UI\)

Review the automation opportunities that AI Agent Advisor has identified for your instance.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Automation discovery must be set up and an analysis run must be completed. For more information, see [Setting up automation opportunity discovery in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-automation-discovery-setup.md).

Role required: sn\_na\_center.nac\_admin

## About this task

After AI Agent Advisor completes an analysis, it produces a prioritized list of automation opportunities based on your instance data. Follow these steps to review the identified opportunities and assess which ones to act on.

**Note:** This topic describes the AI Admin Center feature based on the Next Experience UI. If you're using the Lux user experience for AI Admin Center, see the Lux UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **AI Admin Center \(Legacy\)**.

2.  Review the Automation opportunitiessection of the home page to see the top automation opportunities.

    Each card displays the estimated time and cost savings.

    \[Omitted image "now-assist-center-agent-advisor-opportunities-home-2.png"\] Alt text: AI Agent Advisor section of the home page showing automation opportunities.

3.  Do one of the following:

    1.  Select **Review opportunity** in a cardto view its details.

        The Resolution Steps tab opens showing the opportunity details.

        AI Agent Advisor generates the resolution steps using the data from existing records on your instance.

        \[Omitted image "now-assist-center-agent-advisor-opportunity-detail-4.png"\] Alt text: Resolution Steps tab showing the opportunity details.

    2.  Select **View all** to view the complete list of automation opportunities.

        The Automation opportunities tab opens showing a searchable list of all automation opportunities.

        Use the search field or the filter and sort controls to adjust the list.

        \[Omitted image "ai-agent-advisor-opportunities-list-4.png"\] Alt text: Automation opportunities tab showing a list of all automation opportunities.

        The status of the opportunity displays in the **Status** column.

<table id="table_l3q_ky1_bkc"><thead><tr><th>

Status

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Requires installation

</td><td>

The instance requires installation of a plugin to get a base-system AI agent for this opportunity. No other prebuilt AI agents are available.

</td></tr><tr><td>

Ready to build

</td><td>

All resolution steps for the opportunity are matched to AI tools.

</td></tr><tr><td>

Ready to activate

</td><td>

There is a prebuilt AI agent available to activate for the opportunity.

</td></tr><tr><td>

Active

</td><td>

There is an activated AI agent for the opportunity.

</td></tr><tr><td>

\(Empty\)

</td><td>

The status is empty for an opportunity that has at least one step requiring an AI tool.

</td></tr></tbody>
</table>    3.  Select a combination of sort, filter, and display options to refine the list.

        -   Select a status filter option.
        -   Type in the search box and select the **Submit search** icon \(\[Omitted image "icon-now-assist-center-search.png"\] Alt text: Submit search icon.\) to filter by search criteria.
        -   Select the filter button \(\[Omitted image "icon-now-assist-center-filter.png"\] Alt text: Filter icon.\), choose one or more filters, and select **Apply**.
        -   Select an option from a sort menu.
        -   Select the **List layout** \(\[Omitted image "icon-now-assist-center-list.png"\] Alt text: List layout icon.\) to display the opportunities in a list or **Grid layout** \(\[Omitted image "icon-now-assist-center-grid.png"\] Alt text: Grid layout icon.\) to show them as stacked cards.

## What to do next

Implement an automation opportunity. For more information, see [Implement an automation opportunity from AI Admin Center \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-automation-opportunity-now-assist-center.md).

**Parent Topic:**[AI Agent Advisor in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/using-ai-agent-advisor-in-now-assist-center.md)

