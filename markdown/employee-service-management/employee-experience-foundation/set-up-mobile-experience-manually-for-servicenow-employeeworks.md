---
title: Set up Mobile experience manually for ServiceNow EmployeeWorks Web App
description: Enable employees to use EmployeeWorks in Now Mobile. Configure the set up manually.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/set-up-mobile-experience-manually-for-servicenow-employeeworks.html
release: brazil
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-11-19"
reading_time_minutes: 2
breadcrumb: [Mobile experience setup for ServiceNow EmployeeWorks Web App, Mobile, EmployeeWorks Web App channels, EmployeeWorks, Employee Service Management]
---

# Set up Mobile experience manually for ServiceNow EmployeeWorks Web App

Enable employees to use EmployeeWorks in Now Mobile®. Configure the set up manually.

## Before you begin

The following procedure applies if you're using ServiceNow EmployeeWorks Web App with one of these versions:

-   Brazil Patch 00 and 01
-   Australia Patch 7 and previous
-   Zurich Patch 13 and previous

If you're using later versions, refer to [Configure mobile experience for ServiceNowEmployeeWorks Web App](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/employee-experience-foundation/configure-mobile-experience-of-employeeworks.md).

Role required: mobile\_admin and mobile\_admin\_experience

## Procedure

1.  Create the Mobile app config record for EmployeeWorks.

    1.  Navigate to **System Mobile** &gt; **Mobile Branding** &gt; **Mobile App Configs**.

        You can also directly type `sys_sg_native_client_list.do` in the navigation and press Enter.

    2.  Select **New**.

    3.  On the form, do the following:

        1.  Enter the **Name** as `EmployeeWorks`.
        2.  Set the **Type** as **Request**.
        3.  In the **Order** field, set the order.

            The specified order decides which experience loads by default when a user opens Now Mobile®. The experience with the lowest order is set as default. To make EmployeeWorks the default experience, set the order to any value below the order of the other configured experiences.

        4.  In the **Web Experience** field, select **EmployeeWorks**.
        5.  Select **Submit** to save the form.
        \[Omitted image "mobile-exp-manual-mobile-config.png"\] Alt text: Mobile App Config form

2.  Add the AIUX configuration records.

    1.  On the EmployeeWorks mobile app config record that you created, right click the form header, and select **Configure** &gt; **Related Lists**

    2.  On the Configuring related list form, move **AIUX Configurations** from Available to the Selected side.

    3.  Select **Save**.

    4.  Go to the AI UX Configurations related list, select **New**.

    5.  Search for `Employee Works`, and select the following records:

        \[Omitted image "mobile-exp-manual-aiux-config.png"\] Alt text: AIUX Configuration Scripts

        -   **EmployeeWorks Navigation**: Controls the header structure, including the logo, buttons, and their orientation.
        -   **EmployeeWorks Settings**: Controls what appears on the Settings page, such as connectors and accessibility options.
        **Note:** Don't customize the records during initial setup. The experience reads these values to drive core behavior, and any changes can cause it to render incorrectly.

    6.  Save the changes.

3.  Enable the Experience switcher.

    Add an experience picker inside Now Mobile®, enabling users to toggle between available experiences from the **Settings** menu.

    1.  Add the Experience switcher system property.

        1.  In the navigation, type and search `sys_properties.list`.
        2.  Select **New**.
        3.  Set the Application scope to **Global**.
        4.  Enter the following details:
            -   **Name**: **glide.sg.enable\_experience\_switching.request**
            -   **Description**: Enable Experience Switcher on Mobile App type Request.
            -   **Type**: string
            -   **Value**: true
    2.  Select **Save**.

        **Note:** After saving the changes, to see the experience picker, users must log out and log in again on Now Mobile®. The Experience picker is available in **Settings**.

4.  Verify the EmployeeWorks Mobile experience on a test device.

    1.  Open Now Mobile® on a test device, and sign in to your instance.

    2.  Check the result based on the **Order** value you set on the EmployeeWorks Mobile app config record:

        -   **Order 1 to 4 \(default experience\)**: The app opens directly with EmployeeWorks.
        -   **Order 11 or higher \(switchable experience\)**: The app opens in Now Mobile®. Go to **Settings**, and select **EmployeeWorks**.

            **Note:** If the Experience picker doesn't appear, confirm that the switcher property was created in the Global scope and that its value is `true`.


## Result

EmployeeWorks is available in Now Mobile® as the default experience or as a switchable experience, depending on the set order.

**Parent Topic:**[Mobile experience setup for ServiceNow EmployeeWorks Web App](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/employee-experience-foundation/mobile-experience-setup-for-servicenow-employeeworks.md)

**Related topics**  


[Configure mobile experience for ServiceNowEmployeeWorks Web App]()

