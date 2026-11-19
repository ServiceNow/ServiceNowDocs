---
title: Generate activity stream responses
description: Generate recommendations for work notes or comments in a case record using ServiceNow Otto and add them to enhance the quality of your interactions with the user.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/generate-a-recommendation-to-respond-to-an-activity.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2025-11-08"
reading_time_minutes: 1
breadcrumb: [Use generative AI skills, ServiceNow Otto for CSM, Customer Service Management]
---

# Generate activity stream responses

Generate recommendations for work notes or comments in a case record using ServiceNow Otto and add them to enhance the quality of your interactions with the user.

## Before you begin

These skills are inactive by default. Your administrator must enable the skills that you want to use.

Role required: sn\_customerservice\_agent and sn\_customerservice.consumer\_agent

## Procedure

1.  Navigate to a case record in the CSM/FSM Configurable Workspace or Core UI where you want to generate work notes or comments using ServiceNow Otto.

2.  Select **Compose**, then select **Compose Comments** or **Compose Work Notes** from the drop down in front line case page.

    If you haven’t switched to the front line case page, you can also do the same actions in **Work notes** or **Comments** tabs.

    1.  Select the Sparkle icon \[Omitted image "icon-ai-sparkle.png"\] Alt text: GenAI icon.

        The following four options appear:

        -   **Acknowledge task**: Confirm receipt and understanding of the customer’s request or issue.
        -   **Follow up**: Reconnect with the customer to check progress or ensure resolution.
        -   **Post response**: Provide a clear, timely reply to the customer’s query or concern.
        -   **Summarize actions taken**: Create a summary of all steps taken to resolve the case.
        **Note:** The options display based on the configurations by your admin. Under work notes only 3 options are available – Post response, Summarize actions taken and Follow up.

    2.  Select one of the options based on the type of response you want Now Assist to generate.

        The response appears in the ServiceNow Otto Context Menu \(NACM\).

    3.  You can select the **Refine** menu and elaborate, shorten, or change the tone of the response.

3.  Select **Insert**.


**Parent Topic:**[Using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/now-assist-csm-using.md)

**Related topics**  


[Configure activity response generation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/now-assist-for-csm/configure-activity-response-generation.md)

