---
title: Configure response feedback
description: Configure the response feedback options that appear when users select thumbs up or thumbs down on a ServiceNow Otto for Virtual Agent or ServiceNow Otto panel response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/conversational-interfaces/now-assist-in-virtual-agent/nava-configure-response-feedback-manually.html
release: zurich
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: task
last_updated: "2026-03-31"
reading_time_minutes: 1
breadcrumb: [Configuring assistants overview, ServiceNow Otto for Virtual Agent, Conversational Interfaces]
---

# Configure response feedback

Configure the response feedback options that appear when users select thumbs up or thumbs down on a ServiceNow Otto for Virtual Agent or ServiceNow Otto panel response.

## Before you begin

Role required: admin

## Procedure

1.  In the filter navigator, enter `sys_now_assist_deployment_config_attributes.list` to display the Now Assist in Virtual Agent Deployment Config Attributes table.

2.  In the search fields, select **Name** from the drop-down list and enter `granular` in the Search field.

3.  To change negative granular feedback settings, select **is\_negative\_granular\_feedback\_enabled** with ServiceNow Otto for Virtual Agent \(default\) as the Deployment Configuration.

4.  On the next screen, set the value to **true** to enable negative granular feedback or **false** to disable it.

5.  Select **Submit**.

6.  To change positive granular feedback settings, select **is\_positive\_granular\_feedback\_enabled** with ServiceNow Otto for Virtual Agent \(default\) as the Deployment Configuration.

7.  On the next screen, set the value to **true** to enable positive granular feedback or **false** to disable it.

8.  Select **Submit**.

9.  To configure the feedback options, in the filter navigator, enter `sys_now_assist_message_bundle.list` to display the Now Assist Message Bundles table.

10. In the search fields, select **for text** from the drop-down list and enter `granular` in the Search field.

11. Do one of the following:

    -   To create a new granular feedback selection, select **New**.
    -   To change an existing granular feedback option, select the option.
12. Complete the fields: **Description**, **Message**, **Message Key**, **Bundle Id**, **Application**, **Active**, **Order**.

13. Select **Submit**.

14. For more information on accessing the stored feedback data, see [Granular Feedback and Analytics in ServiceNow Otto for Virtual Agent \(KB3060968\).](https://support.servicenow.com/kb_view.do?sysparm_article=KB1213249)


