---
title: Embed a custom portal
description: Embed your custom portal to replace the Employee Center tab in Microsoft Teams by configuring the system property. The custom portal shows up in the Employee Center tab in Microsoft Teams.You can hide the chat option for your custom portal that appears in the Employee Center tab within Microsoft Teams.You can hide the logout option for your custom portal that appears in the Employee Center tab within Microsoft Teams.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Employee Center, IT Service Management integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Embed a custom portal

Embed your custom portal to replace the Employee Center tab in Microsoft Teams by configuring the system property. The custom portal shows up in the Employee Center tab in Microsoft Teams.

## Before you begin

Role required: admin

If you’re using a custom portal rather than the Employee Center, you can replace the embedded Employee Center with your custom portal, so that it’s accessible within Microsoft Teams. The following steps take you through the configuration to embed your portal.

## Procedure

1.  In the navigation pane, enter `sys_properties.list`.

2.  Search for `sn_now_teams.portal.suffix` property under Name.

    ![System properties list](../images/sys-properties-list.png)

3.  Select **sn\_now\_teams.portal.suffix**.

4.  Enter the value of your custom portal in the **Value** field.

    ![Custom value](../images/custom-value-sys-properties.png)

5.  Select **Update**.

6.  Create a custom header for the embedded portal after you configure your custom portal.

    For more information on adding header configuration, see [Configure HTTP response headers](https://www.servicenow.com/docs/access?context=configure-http-response-header&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

    1.  In the Navigator pane, type `sys_response_header.list`.

    2.  Select **New**.

    3.  On the HTTP Response Header form, fill in the following fields based on your requirement.

        -   Active
        -   Application
        -   Record
        -   Description
    4.  Enter the following field values.

<table id="table_lq5_5ct_fwb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Applies to

</td><td>

Specify Type

</td></tr><tr><td>

Type

</td><td>

Service Portal \[sp\_portal\]

</td></tr><tr><td>

Name

</td><td>

Content-Security-Policy

</td></tr><tr><td>

Value

</td><td>

Frame-ancestors 'self' [https://teams.microsoft.com](https://teams.microsoft.com)**Important:**

To enable the custom portal in all Microsoft 365 apps, add the following domains to the Value field.

-   \*.office.com
-   \*.office365.com
-   \*.microsoft365.com
-   \*.cloud.microsoft
For example: `Frame-ancestors 'self' https://teams.microsoft.com *.office.com *.office365.com *.microsoft365.com *.cloud.microsoft`

</td></tr></tbody>
</table>    5.  Select **Submit**.


**Parent Topic:**[Configuring Employee Center](../concept/employee-center-dashboard-admin-it.md)

## Hide the chat button on the custom portal

You can hide the chat option for your custom portal that appears in the Employee Center tab within Microsoft Teams.

### Before you begin

Ensure that you set the **com.glide.cs.advanced-chat-popover** system property to false.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **CSS**.

    ![CSS list](../images/system-css.png)

2.  Select the custom CSS that you want to edit.

3.  Select the **click here** link to edit the CSS.

    ![Edit CSS](../images/edit-css-2.png)

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


## Hide the logout button on the custom portal

You can hide the logout option for your custom portal that appears in the Employee Center tab within Microsoft Teams.

### Before you begin

Role required: admin

### Procedure

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


