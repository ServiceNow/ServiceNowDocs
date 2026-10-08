---
title: Configure the HRBP productivity assistant
description: Set the link for the button that appears in the weekly digest and critical urgency notifications so that HR business partners can access the HRBP productivity assistant. HR business partners can't access the assistant from these emails until you set the link in a system property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/configure-hrbp-pa.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-08-19"
reading_time_minutes: 1
keywords: [HRBP productivity assistant, productivity assistant, specialized\_assistant\_id, weekly digest, Otto]
breadcrumb: [Configure, HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# Configure the HRBP productivity assistant

Set the link for the button that appears in the weekly digest and critical urgency notifications so that HR business partners can access the HRBP productivity assistant. HR business partners can't access the assistant from these emails until you set the link in a system property.

## Before you begin

-   The HRBP Productivity app is installed.
-   Your HR business partners have access to the EmployeeWorks Web App.
-   Your organization has set up the HRBP productivity assistant in the EmployeeWorks Web App, and you have the assistant ID.

Role required: HRBP administrator \[sn\_hrbp\_hub.admin\]

## About this task

HR business partners use the HRBP productivity assistant in the EmployeeWorks Web App. The weekly digest and the critical urgency notification each include an **Ask HRBP Specialized Assistant** button that opens the assistant.

The button links to the value stored in the **sn\_hrbp\_hub.specialized\_assistant\_id** system property. Although the property name refers to an ID, its value is the path to your assistant. The property is installed with a placeholder in place of the ID, so you must replace it with the ID of your assistant.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The System Properties \[sys\_properties\] table appears.

2.  Select **Name** from the drop-down list associated with the **Search** field.

3.  In the **Search** field enter `sn_hrbp_hub.specialized_assistant_id`.

4.  Select the **sn\_hrbp\_hub.specialized\_assistant\_id** property.

    The following path appears in the **Value** field: `aiux/employeeworks/chat?mw_route=/assistant/agents/{ YOUR_ASSISTANT_ID }`.

5.  Replace the following placeholder text with the assistant ID of your HRBP productivity assistant: \{ YOUR\_ASSISTANT\_ID \}.

6.  Select **Update**.


## Result

The **Ask HRBP Specialized Assistant** button in the weekly digest and the critical urgency notification opens your HRBP productivity assistant.

## What to do next

Review the scheduled job and notification that send the weekly digest. For more information, see [Configure the HRBP weekly digest](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/configure-hrbp-weekly-digest.md).

