---
title: Hide the chat button on the custom portal
description: Hide the chat option for your custom portal that appears in the Employee Center tab within Microsoft Teams.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Embed a custom portal, Configuring Employee Center, HR Service Delivery integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Hide the chat button on the custom portal

Hide the chat option for your custom portal that appears in the Employee Center tab within Microsoft Teams.

## Before you begin

Ensure that you set the **com.glide.cs.advanced-chat-popover** system property to false.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **CSS**.

2.  Select the custom CSS that you want to edit.

3.  Select the **click here** link to edit the CSS.

4.  Paste the following code in the **CSS** field.

    **Note:** In the following code example, the `.embedded-experience .sp-ac-btn` element specifies the chat button and the `display: none;` property hides the button. You can customize the code based on your requirement.

    ```css
    /* Embedded portal */
    
    .embedded-experience .sp-ac-btn {
            display: none;
          }
    
    ```

5.  Select **Update**.

6.  Refresh the custom portal tab in Microsoft Teams.


**Parent Topic:**[Embed a custom portal](customize-custom-portal-employee-center.md)

