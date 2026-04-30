---
title: Embed a custom portal
description: Embed your custom portal to replace the Employee Center tab in Microsoft Teams by configuring the system property. The custom portal shows up in the Employee Center tab in Microsoft Teams.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Employee Center, HR Service Delivery integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, ServiceNow for Microsoft 365 Add-ins and Microsoft Teams, Unified Employee Experience, Employee Service Management]
---

# Embed a custom portal

Embed your custom portal to replace the Employee Center tab in Microsoft Teams by configuring the system property. The custom portal shows up in the Employee Center tab in Microsoft Teams.

## Before you begin

Role required: admin

If you’re using a custom portal rather than the Employee Center, you can replace the embedded Employee Center with your custom portal, so that it’s accessible within Microsoft Teams. The following steps take you through the configuration to embed your portal.

## Procedure

1.  In the navigation pane, enter `sys_properties.list`.

2.  Search for `sn_now_teams.portal.suffix` property under Name.

    ![System properties list with sn_now_teams.portal.suffix highlighted](../images/sys-properties-list.png)

3.  Select **sn\_now\_teams.portal.suffix**.

4.  Enter the value of your custom portal in the **Value** field.

    Refer to the below example if you are adding your custom portal: ![System property [sn_now_teams.portal.suffix] form with the value field highlighted.](../images/custom-value-sys-properties.png)

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


-   **[Hide the chat button on the custom portal](disable-chat-button-teams-custom-portal.md)**  
Hide the chat option for your custom portal that appears in the Employee Center tab within Microsoft Teams.
-   **[Hide the logout button on the custom portal](disable-logout-button-teams-custom-portal.md)**  
You can hide the logout option for your custom portal that appears in the Employee Center tab within Microsoft Teams.

**Parent Topic:**[Configuring Employee Center](../concept/employee-center-dashboard-admin.md)

