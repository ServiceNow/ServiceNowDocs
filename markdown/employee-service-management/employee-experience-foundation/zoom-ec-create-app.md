---
title: Employee Center for Zoom
description: Integrate Employee Center with a Zoom account for your organization employees so they can use Employee Center capabilities from within the Zoom client application.
locale: en-US
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrate, Employee Center, Employee Service Management]
---

# Employee Center for Zoom

Integrate Employee Center with a Zoom account for your organization employees so they can use Employee Center capabilities from within the Zoom client application.

## Before you begin

Ensure you have installed the Employee Center integration with Zoom plugin \[sn\_ex\_ec\_zm\].

At least Zoom application version 5.13.11 and it must be installed on the ServiceNow® instance.

Role required: admin, Zoom admin

The Zoom admin role is the Zoom account admin role, and it is not a role in ServiceNow.

## About this task

Integrating Zoom with  Employee Center enables access  to Employee Center functionality from within the Zoom client either on Windows OS or iOS.​ For more information, see [Use Employee Center from Zoom](zoom-create-email-notification.md).

For information about ServiceNow integrations with the Zoom application, see [ServiceNow for Zoom](../../sn-zoom/concept/sn_zoomIntegration.md).

## Procedure

1.  Navigate to [Zoom App Marketplace](https://marketplace.zoom.us/) and sign in to your account as Zoom admin.

2.  Connect your Zoom account to ServiceNow Employee Center on your ServiceNow instance.

    1.  Log in to your ServiceNow instance.

    2.  Navigate to **All** &gt; **Employee Center** &gt; **Employee Center for Zoom** &gt; **Setup**.

        **Note:** Different domains can have different Zoom accounts mapped.

    3.  On the Connect to an account page, select **Connect** associated with Zoom.

        You are redirected to the Zoom App Marketplace.

        **Note:** If you are prompted to log in, log in to your Zoom account as an admin.

    4.  Enable **Approve for all users**.

    5.  Select **Enable** in the Enable App Approval for All Users dialog box.

        ServiceNow Employee Center access and usage in Zoom application is enabled for all employees in your organization.

    6.  Select **Allow**.

        The message `Successfully connected to Zoom account` is displayed in your ServiceNow instance setup.

3.  Access ServiceNow Employee Center in the Zoom application by an admin.

    1.  Open your Zoom application.

        The notification `ServiceNow Employee Center is added` is displayed.

    2.  Navigate to **Apps** &gt; **My Apps**.

        You can now access the ServiceNow Employee Center application.

    3.  Select **ServiceNow Employee Center**.

    4.  Enter your ServiceNow login credentials and select **Log in**.

        ServiceNow Employee Center homepage is displayed.


-   **[Set up a custom portal](zoom-set-up-custom-portal.md)**  
Configure the ServiceNow® Employee Center portal appearance of your organization’s custom portal in Zoom.
-   **[View connected Zoom accounts](zoom-view-connected-accounts.md)**  
View the list of Zoom accounts connected to your ServiceNow® instance.
-   **[Connect your Zoom account to a different ServiceNow instance](zoom-override-sn-instance.md)**  
Connect your Zoom account to another ServiceNow® instance by overriding your existing ServiceNow instance.
-   **[Change existing Zoom account connection](zoom-account-change.md)**  
Change your existing Zoom account connection in your ServiceNow® instance.

**Parent Topic:**[Integrating with Employee Center](../concept/integrate-ec.md)

**Related topics**  


[Use Employee Center from Zoom](zoom-create-email-notification.md)

