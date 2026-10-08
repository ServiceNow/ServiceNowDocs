---
title: View your automation opportunities \(Lux UI\)
description: Review the automation opportunities that AI Agent Advisor has identified for your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-admin-center-lux-view-automation-opportunities.html
release: brazil
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, AI Agent Advisor]
breadcrumb: [AI Agent Advisor in AI Admin Center, Use, AI Agent Advisor, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# View your automation opportunities \(Lux UI\)

Review the automation opportunities that AI Agent Advisor has identified for your instance.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Automation discovery must be set up and an analysis run must be completed. For more information, see [Set up a data source for analysis \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-set-up-data-source.md).

Role required: sn\_na\_center.nac\_admin

## About this task

After AI Agent Advisor completes an analysis, it produces a prioritized list of automation opportunities based on your instance data. Follow these steps to review the identified opportunities and assess which ones to act on.

**Note:** This topic describes the AI Admin Center feature based on the Lux user interface \(UI\). If you're using the Next Experience UI for AI Admin Center, see the Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Review the **Automation opportunities** section of the home page to see the top automation opportunities.

    Each card displays the estimated time and cost savings.

    \[Omitted image "ai-admin-center-lux-home-opportunities.png"\] Alt text: Automation opportunities section of the home page showing the top opportunities with estimated time and cost savings.

3.  Do one of the following:

    -   Select **Review** in a card to view its details.

        The opportunity opens in a side panel showing the opportunity details. AI Agent Advisor generates the resolution steps using the data from existing records on your instance.

        \[Omitted image "ai-admin-center-lux-advisor-details.png"\] Alt text: Side panel showing the details of an automation opportunity.

    -   Select **View all** to view the complete list of automation opportunities.

        The Automation opportunities page opens showing a searchable list of all automation opportunities. Use the search field or the filter and sort controls to adjust the list.

        \[Omitted image "ai-admin-center-lux-advisor-opportunities-page.png"\] Alt text: Automation opportunities page showing a list of opportunities.

        The status of the opportunity displays in the **Status** column.

        |Status|Description|
        |------|-----------|
        |Requires installation|The instance requires installation of a plugin to get a base system AI agent for this opportunity. No other prebuilt AI agents are available.|
        |Ready to build|All resolution steps for the opportunity are matched to AI tools.|
        |Ready to activate|There is a prebuilt AI agent available to activate for the opportunity.|
        |Active|There is an activated AI agent for the opportunity.|
        |\(Empty\)|The status is empty for an opportunity that has at least one step requiring an AI tool.|

4.  Select a combination of sort, filter, and display options to refine the list.

    -   Select a status filter option.
    -   Type in the search box and select the **Submit search** icon \(\[Omitted image "icon-now-assist-center-search.png"\] Alt text: Submit search icon.\) to filter by search criteria.
    -   Select the filter button \(\[Omitted image "icon-now-assist-center-filter.png"\] Alt text: Filter icon.\), choose one or more filters, and select **Apply**.
    -   Select the **Grid layout** \(\[Omitted image "icon-aiac-lux-grid.png"\] Alt text: Grid layout icon.\) to display the opportunities in a list or **Gallery layout** \(\[Omitted image "icon-aiac-lux-gallery.png"\] Alt text: Gallery layout icon.\) to show them as stacked cards.

## What to do next

Implement an automation opportunity. For more information, see [Implement an automation opportunity \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-implement-automation-opportunity.md).

**Parent Topic:**[AI Agent Advisor in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/using-ai-agent-advisor-in-now-assist-center.md)

