---
title: Install Journey designer version 2
description: Install the Journey designer version 2 \[sn\_jny\] application to enable administrators and managers to create and manage various professional and personal events and journeys.
locale: en-US
release: xanadu
product: Journey Designer
classification: journey-designer
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installation and configuration overview, Journey designer, HR Service Delivery, Employee Service Management]
---

# Install Journey designer version 2

Install the Journey designer version 2 \[sn\_jny\] application to enable administrators and managers to create and manage various professional and personal events and journeys.

## Before you begin

**Note:** You must upgrade to Utah before you can install Journey designer version 2.

Dependent plugins and apps for Journey designer:

-   Human Resources Scoped App: Core \[com.sn\_hr\_core\]
-   Human Resources Scoped App: Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\]
-   Employee Center Pro 28.0.1 \[sn\_ex\_sp\_pro\]
-   HR Taxonomy 1.2.1\[sn\_hr\_emp\_taxonomy\]
-   Journey Accelerator 6.0.5 \[sn\_ja\]
-   Retry Framework 1.0.2 \[sn\_retry\_handler\]

Role required: admin.

## About this task

Journey designer version 2 \(JD\) must be installed as a store application on the Utah family release.

**Note:** The Journey designer app also installs the Journey Accelerator v6.0.0 \[sn\_ja\] application.

## Procedure

1.  Go to the ServiceNow Store and find the Journey designer \[sn\_jny\] application using the filter criteria and search bar.

    In the list next to the **Install** button, the versions that are available to you’re displayed.

2.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

3.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

4.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

5.  Select **Install**.


## What to do next

When Journey designer is installed, outstanding Lifecycle Events cases aren’t affected. You can migrate existing HR services to use journeys instead of Lifecycle Events. See, [Journeys Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1124255).

**Parent Topic:**[Installation and configuration overview](../concept/jny-inst-config-overview.md)

