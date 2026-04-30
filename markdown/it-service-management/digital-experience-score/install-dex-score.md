---
title: Install Digital Experience Score​
description: You can install the Digital Experience Score​ application \(sn\_dex\_score\) if you have the admin role. The application includes demo data that you can load after the installation is complete. It also installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Digital Experience Score
classification: digital-experience-score
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring Digital Experience Score​, Digital Experience Score​, Digital End-User Experience, IT Service Management]
---

# Install Digital Experience Score​

You can install the Digital Experience Score​ application \(sn\_dex\_score\) if you have the admin role. The application includes demo data that you can load after the installation is complete. It also installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the Digital Experience Score​ application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The following items are installed with Digital Experience Score​:

-   Plugins:

    ITOM Java Utilities \(com.itom.jutils\)

-   Store applications:
    -   Digital Experience Feedback Survey \(sn\_dex\_feedback\_sur\): This app is installed with Digital Experience Score​ and is used to send the surveys to employees to collect feedback on their digital experience.

        For more information, see [Components installed with Digital Experience Feedback Survey](../reference/dexscr-installed-with-survey-feedback.md).

    -   Digital End-User Experience: The Digital End-User Experience \(DEX\) suite offers proactive visibility to help you understand and improve the end-user experience across your organization. It includes Application &amp; Device Health, DEX Content Playbook, and Desktop Assistant, combined to provide unique benefits to diagnose and address any negative experiences.
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Digital Experience Score​](../reference/dexscr-installed-with-dex-score.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Digital Experience Score​ application \(sn\_dex\_score\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.


## What to do next

Load the demo data for Digital Experience Score​. For more information, see [Load Digital Experience Score​ demo data](dexscr-load-demo-data.md).

Demo data comprises the sample records that describe application features for the common use cases. Load the demo data when you first install the application on a development or test instance.

-   **[Load Digital Experience Score​ demo data](dexscr-load-demo-data.md)**  
Load the demo data for Digital Experience Score​ after installing the application.
-   **[Delete Digital Experience Score​ demo data](dexscr-delete-demo-data.md)**  
Delete the demo data for Digital Experience Score​ when you no longer need it.

**Parent Topic:**[Configuring Digital Experience Score​](../concept/dexscr-configuring-dex-score.md)

