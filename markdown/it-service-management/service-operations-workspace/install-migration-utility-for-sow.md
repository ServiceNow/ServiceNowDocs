---
title: Install the Migration Utility for Service Operations Workspace
description: You can install the Migration Utility for Service Operations Workspace application \(sn\_sow\_migration\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM, Configuring Service Operations Workspace for ITSM, Service Operations Workspace for ITSM, IT Service Management]
---

# Install the Migration Utility for Service Operations Workspace

You can install the Migration Utility for Service Operations Workspace application \(sn\_sow\_migration\) if you have the admin role.The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).

Role required: admin

## About this task

The Migration Utility for Service Operations Workspace application \(sn\_sow\_migration\) installs the on-screen migration utility that eases the migration process from ITSM Agent Workspace to Service Operations Workspace for ITSM.

The Agent Workspace Migration Request \(sn\_sow\_migration\_aw\_migration\_request\) table is installed with Migration Utility for Service Operations Workspace. This tables stores the following migration request details:

-   Customisations and configurations selected for various features
-   Migration status \(whether the migration is completed or in progress\)
-   Migration result \(Customizations or configurations that are migrated successfully or failed\)
-   Any post migration message for the selected customizations or configurations

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Migration Utility for Service Operations Workspace application \(sn\_sow\_migration\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Migration from ITSM Agent Workspace to Service Operations Workspace for ITSM](../concept/migration-from-itsm-aw-sow.md)

