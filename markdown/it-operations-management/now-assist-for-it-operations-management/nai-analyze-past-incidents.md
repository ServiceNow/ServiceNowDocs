---
title: Generate a Now Assist summary of past related incidents
description: View a Now Assist summary of past incidents on the same or related Configuration Items \(CIs\) and strategies used to resolve them.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/nai-analyze-past-incidents.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Accelerate alert resolution with past incident analysis, Use generative AI, Now Assist for ITOM, IT Operations Management]
---

# Generate a Now Assist summary of past related incidents

View a Now Assist summary of past incidents on the same or related Configuration Items \(CIs\) and strategies used to resolve them.

## Before you begin

-   Install the ITOM plugin in the Now Assist feature. For more information, see [Install the Now Assist for IT Operations Management \(ITOM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/install-now-assist-itom.md).
-   Ensure that the Alert investigation skill is active. For more information, see [Install the Now Assist for IT Operations Management \(ITOM\) plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/install-now-assist-itom.md).
-   View important information about the ServiceNow® Now Assist for IT Operations Management \(ITOM\) application in [Now Assist for IT Operations Management \(ITOM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom.md).

For comprehensive information about the Now Assist panel, see [Now Assist panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/enable-ai-experiences/now-assist-panel-overview.md).

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/now-assist-skills/now-assist-skills-on-by-default.md).

Role required: evt\_mgmt\_operator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  Select the List icon \(\[Omitted image "icon-lists.png"\] Alt text: List icon.\) in the navigation bar.

3.  Select **Lists** &gt; **Alerts** &gt; **All Alerts**.

4.  Open an alert.

5.  Select the Now Assist panel icon \(\[Omitted image "icon-ai-sparkle.png"\] Alt text: Now Assist panel icon.\).

    The Now Assist panel displays.

6.  Request a Now Assist past incidents investigation by selecting **Analyze related incidents**.

    An additional Large Language Model \(LLM\) validation layer is added to the AI search capability to improve the accuracy of results returned by AI skills.

    A summary of the most relevant related incidents displays in the panel.

7.  Inspect the details of a related incident by selecting the relevant link under Related Incidents.

    The incident page opens, showing the Overview tab.


**Parent Topic:**[Speed up alert resolution with a Now Assist analysis of past related incidents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/nai-past-incidents.md)

