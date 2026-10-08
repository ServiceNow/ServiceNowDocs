---
title: Request ServiceNow Otto capabilities for Customer Success Management
description: Request generative AI capabilities for Customer Success Management, such as an engagement summary or a renewal insight, by using the conversational interface in the ServiceNow Otto panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-otto-request-panel.html
release: brazil
topic_type: task
last_updated: "2026-09-22"
reading_time_minutes: 1
keywords: [Otto panel, Customer Success Management, conversational interface]
breadcrumb: [Customer success, Use, Customer Success Management]
---

# Request ServiceNow Otto capabilities for Customer Success Management

Request generative AI capabilities for Customer Success Management, such as an engagement summary or a renewal insight, by using the conversational interface in the ServiceNow Otto panel.

## Before you begin

Make sure the Next Experience is enabled. For more information, see [Next Experience UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/next-experience-landing-page.md).

Role required: `sn_acct_lc.customer_success_agent`

## About this task

Use the ServiceNow Otto panel in CRM Workspace to request a summary or generated draft for an engagement, touchpoint, risk signal, or success play. The panel opens within the record, so you don't have to navigate away.

For more information about the ServiceNow Otto panel, see [ServiceNow Otto panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-panel-overview.md). For information about activating the panel, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/activate-now-assist-panel.md).

## Procedure

1.  Log in to an instance where Customer Success Management is installed.

2.  Navigate to **Workspaces** &gt; **CRM Workspace** &gt; **Lists** &gt; **Customer Success** and select the record type you want, such as **All Engagements**, **All Touchpoints**, or **All Risks and issues**.

3.  Open a record.

4.  From the header menu, select the AI icon \(\[Omitted image "icon-ai-sparkle.png"\] Alt text: ServiceNow Otto icon.\).

5.  Select the relevant generative AI capability from the ServiceNow Otto panel.

    -   To summarize the record, select **Summarize a record**.
    -   On a risk signal, to get recommended solutions, select **Recommend solutions**.
    -   On an engagement due for renewal, to get a renewal insight, select **Generate renewal insight**.
    The capabilities available depend on the record type and the skills your administrator has activated. See [ServiceNow Otto skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-otto-skills-overview.md) for the full list.


**Parent Topic:**[Customer success](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/acct-lifecycle-events/account-lifecycle-use-cust-success.md)

