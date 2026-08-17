---
title: Enable Spend categorization agent in ServiceNow Otto panel
description: Enable the Spend categorization agent in AI Agent Studio so users can run it from the ServiceNow Otto panel to validate and update product and spend categories on procurement records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/enable-agent-na-panel.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-07-28"
reading_time_minutes: 1
keywords: [Spend categorization agent, ServiceNow Otto panel, AI Agent Studio, agent activation]
breadcrumb: [Activate the Spend categorization agent, Configure ServiceNow Otto for SPO, ServiceNow Otto for SPO, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Enable Spend categorization agent in ServiceNow Otto panel

Enable the Spend categorization agent in AI Agent Studio so users can run it from the ServiceNow Otto panel to validate and update product and spend categories on procurement records.

## Before you begin

Before you begin, verify the following:

-   The prediction solutions are verified.
-   The Category Prediction skills are active.
-   The category prediction system properties are verified.

Role required: sn\_aia.admin or admin.

## About this task

The Spend categorization agent is inactive when installed. After you enable the agent in AI Agent Studio, users can run it from the ServiceNow Otto panel on procurement records to validate a category, review AI suggestions, and apply an update. Because the agent uses AI, its suggestions can be inaccurate, so users review and confirm a category before the category is applied.

## Procedure

1.  Open AI Agent Studio by navigating to **All** &gt; **AI Agent Studio**.

2.  Select the **Spend categorization agent** from the AI agents list.

    Review the agent details to verify it predicts product and spend categories on purchase requisition lines.

3.  Verify that the agent is configured to run in the ServiceNow Otto panel.

    The agent is configured to run in the ServiceNow Otto panel and the virtual agent channel.

4.  Enable the agent.

    The Spend categorization agent is active and available in the ServiceNow Otto panel.

5.  Open a supported procurement record, then open the ServiceNow Otto panel to verify the agent is listed.

    The Spend categorization agent is listed and can validate or update the category for the record.


## Result

Users can run the Spend categorization agent from the ServiceNow Otto panel to predict, validate, and update product and spend categories.

**Parent Topic:**[Activate the Spend categorization agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/activate-spend-categorization-agent.md)

