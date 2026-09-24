---
title: Generate resolution notes in case form
description: Use the ServiceNow Otto context menu in the resolution notes field of the case form in both Core UI \(UI16\) and Workspace to create resolution note.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/now-assist-for-csm/gen-resolution-notes-in-case-form.html
release: brazil
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Use generative AI, ServiceNow Otto for CSM, Customer Service Management]
---

# Generate resolution notes in case form

Use the ServiceNow Otto context menu in the resolution notes field of the case form in both Core UI \(UI16\) and Workspace to create resolution note.

## Before you begin

Role required: sn\_customerservice\_agent, sn\_customerservice.consumer\_agent

## About this task

Watch this video to learn how to generate the resolution notes for a case.\[Omitted video\] Description: Generate resolution notes for a case

You can generate resolution notes for a case in both the CRM Workspace and Core UI. Use the ServiceNow Otto context menu within the resolution notes field in the case form to generate resolution notes.

**Note:**

-   The context menu is the recommended experience. The popup window experience is going to be deprecated. Each interface operates differently.
-   The case must be in the open state.

An agent can do these actions by using the AI icon \[Omitted image "icon-ai-sparkle.png"\]:

-   Generate resolution notes based on the case context.
-   Refine the recommendation by elaborating or shortening the content.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace** and open a customer service case that is in an open state.

2.  Navigate to the Resolution notes field in the case form.

3.  Select the AI icon \[Omitted image "icon-ai-sparkle.png"\].

    AI icon \[Omitted image "icon-ai-sparkle.png"\] generates a recommended text that is based on the context of the case.

    \[Omitted image "now-assist-csm-resolutionnotes-caseform-generate.png"\] Alt text: Resolution notes is generated

4.  Select **Insert** to add the generated content into the resolution notes field.

5.  Review the generated content and select **Refine** to modify the content.

    You get the option to either elaborate or shorten the content as needed.

    \[Omitted image "now-assist-csm-resolutionnotes-caseform-refine.png"\] Alt text: Shorten or elaborate the resolution note


-   **[Generate the resolution notes for a case by using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-generate-resolution.md)**  
Use the resolution notes generation skill in ServiceNow Otto for Customer Service Management \(CSM\) to generate resolution notes for a case. You can propose the resolution to the customer and add it to the case record. By generating the resolution notes, you can wrap up cases faster and provide information about the case resolution to other agents who might encounter similar issues.

**Parent Topic:**[Using ServiceNow Otto for Customer Service Management \(CSM\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/now-assist-for-csm/now-assist-csm-using.md)

