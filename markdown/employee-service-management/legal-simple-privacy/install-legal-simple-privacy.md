---
title: Install Legal Simple Privacy
description: Install the a Legal Simple Privacy \(sn\_lg\_privacy​\) application if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they aren’t already installed.
locale: en-US
release: australia
product: Legal Simple Privacy
classification: legal-simple-privacy
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Legal Simple Privacy, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Install Legal Simple Privacy

Install the a Legal Simple Privacy \(sn\_lg\_privacy​\) application if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they aren’t already installed.

## Before you begin

-   Review the Legal Simple Privacy application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Ensure that the application Legal Request Management \(sn\_lg\_ops\) is installed before you install Legal Simple Privacy.

Role required: admin

## About this task

The following items are installed with Legal Simple Privacy:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Tables

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Legal Simple Privacy \(sn\_lg\_privacy​\) application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    The available versions are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


## What to do next

\(Optional\) Reconfigure the forms in the application to use the new privacy assessment record producer, catalog category, and content taxonomy. For more information, see [Reconfigure forms to use new components](reconfigure-post-install-privacy.md)

Use the Legal Service Delivery Guided Setup to configure the application on your instance. To access Legal Service Delivery guided setup, navigate to **Legal Administration** &gt; **Legal Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

**Parent Topic:**[Configure Legal Simple Privacy](../concept/setting-up-legal-simple-privacy.md)

**Related topics**  


[Reconfigure forms to use new components](reconfigure-post-install-privacy.md)

