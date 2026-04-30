---
title: Hide the logout button on the custom portal
description: You can hide the logout option for your custom portal that appears in the Employee Center tab within Microsoft Teams.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Embed a custom portal, Configuring Employee Center, HR Service Delivery integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Hide the logout button on the custom portal

You can hide the logout option for your custom portal that appears in the Employee Center tab within Microsoft Teams.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **CSS**.

    ![CSS list](../images/system-css.png)

2.  Click on your custom CSS.

3.  Click **here** to edit the CSS.

    ![Edit CSS](../images/edit-css-2.png)

4.  To disable the logout button from Microsoft Teams desktop application.

    Customize the following code as required and paste in the CSS.

    ```
    /* Embedded portal */
    
    /*The code shared to disable the logout button is an example. You need to customize as required to disable logout button.*/
    
    .embedded-experience .avatar-drop-down .header-menu-item:last-child {
            display: none;
          }
    
    ```

5.  To disable the logout button from Microsoft Teams mobile application.

    Customize the following code as required and paste in the CSS.

    ```
    
    /* Embedded portal */
    
    /*The code shared to disable logout button is an example. You need to customize as required to disable logout button.*/
    
    .embedded-experience .impersonate-and-logout {
              div > ul > li:last-child {
                display: none !important;
             }
          }
    
    ```

6.  Click **Update**.

7.  Refresh the custom portal tab in Microsoft Teams.


**Parent Topic:**[Embed a custom portal](customize-custom-portal-employee-center.md)

