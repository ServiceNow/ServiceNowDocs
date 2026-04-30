---
title: Install SRM from Admin Center or ServiceNow Store
description: Install the SRM application from the Admin Center or ServiceNow Store.
locale: en-US
release: xanadu
product: Service Reliability Management
classification: service-reliability-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring Service Reliability Management, Service Reliability Management, ITOM Health, IT Operations Management]
---

# Install SRM from Admin Center or ServiceNow Store

Install the SRM application from the Admin Center or ServiceNow Store.

## Before you begin

Subscriptions required: ITSM Standard and ITOM Operator Professional subscriptions.

**Note:** Data visualizations store app v24.1.8 is also required. See [Data visualizations](https://store.servicenow.com/sn_appstore_store.do#!/store/application/2926d7e8a2ac632a750a9c9101f4cff0/24.0.2?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%25253Bgenerative_ai%25253Bsnow_solution%26q%3DData%2520Visualizations&sl=sh) in the ServiceNow Store to install the app.

To create and manage alert automations, install the Alert automation application available upon request in the ServiceNow Store.

Role required: admin

## About this task

Roles and demo data are installed with SRM. The demo data includes templates that speed up implementation and help users to understand and use it SRM quickly.

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Overview**.

2.  From the **Service Operations Management** card, select **Install**.

3.  In the pop-up window, select **Start Install**.

    You are taken to the ServiceNow Store portal.

4.  Complete any steps necessary.

    **Note:** If any dependencies are showing up in red on the app store listing, select the row to open the dependent app and install it. If you already have the dependent app and it is still showing up in red, you can get or reopt it as needed.

    ![To install the Service Reliability Management application, first confirm that all dependencies are resolved.](../image/sr-install-store.png)

    The example shows us that we have two unresolved dependencies. Before installing the app, we must first resolve this by selecting the two dependencies.![Select the unresolved dependencies to resolve them before installing the application from the ServiceNow store.](../image/sr-install-store2.png)

    Demo data comprises the sample records that describe application features for the common use cases. Demo data is loaded when you first install the application on a development or test instance.

    Following installation, the **Service Operations Management** card can be used to configure SRM.


**Parent Topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Previous topic:**[Configuring Service Reliability Management](../concept/configuring-service-reliability-management.md)

**Next topic:**[Assign an administrator to Service Reliability Management](sr-assign-admins.md)

