---
title: Configure mobile experience for ServiceNowEmployeeWorks Web App
description: Turn on the mobile experience and configure who can use it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/employee-experience-foundation/configure-mobile-experience-of-employeeworks.html
release: brazil
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-11-19"
reading_time_minutes: 1
breadcrumb: [Mobile experience setup for ServiceNow EmployeeWorks Web App, Mobile, EmployeeWorks Web App channels, EmployeeWorks, Employee Service Management]
---

# Configure mobile experience for ServiceNowEmployeeWorks Web App

Turn on the mobile experience and configure who can use it.

## Before you begin

The following procedure applies if you're using ServiceNow EmployeeWorks Web App with one of these versions:

-   Brazil Patch 02 or later
-   Australia Patch 8 or later

If you're using previous versions, refer to [Set up Mobile experience manually for ServiceNow EmployeeWorks Web App](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/employee-experience-foundation/set-up-mobile-experience-manually-for-servicenow-employeeworks.md).

Role required: mobile\_admin and mobile\_admin\_experience

## Procedure

1.  Enable the **sn\_ex\_emp\_hub\_mw.enable\_mobile\_experience** system property.

    This turns on the mobile experience for your instance.

    1.  In the navigation, type and search `sys_properties.list`.

    2.  From the list, select **sn\_ex\_emp\_hub\_mw.enable\_mobile\_experience** system property.

    3.  Enable the property.

2.  Configure Mobile experience.

    1.  Navigate to **ServiceNow EmployeeWorks Web App** &gt; **Configure**.

    2.  Under Mobile Experience, select **Mobile setup**.

    3.  In the Mobile setup page, do the following:

        1.  Enable **Make EmployeeWorks available on mobile** to make it available to the users.
        2.  Specify who can use EmployeeWorks on Now Mobile® using the **Define roles below to limit access to specific groups** option.
        3.  Enable **Set EmployeeWorks as default mobile experience**.

            EmployeeWorks opens by default for users with access. Users can switch to the classic experience at any time using their mobile app settings.

        4.  Enable **Enable experience switcher** if you want to enable users to switch between EmployeeWorks experience and classic experience.
        \[Omitted image "mobile-experience-empworks-setup.png"\] Alt text: EmployeeWorks Mobile setup

3.  Select **Mark as configured** to complete the configuration.


## Result

The mobile experience is available to users with access.

**Parent Topic:**[Mobile experience setup for ServiceNow EmployeeWorks Web App](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/employee-experience-foundation/mobile-experience-setup-for-servicenow-employeeworks.md)

**Related topics**  


[Set up Mobile experience manually for ServiceNow EmployeeWorks Web App]()

