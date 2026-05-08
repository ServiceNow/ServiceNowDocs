---
title: Manage customizations to applications
description: You can manage your company's customizations for applications that belong to other organizations or a scoped ServiceNow plug-in.
locale: en-US
release: australia
product: Application Repository \(Self-Hosted\)
classification: application-repository-self-hosted
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [ServiceNow application repository, Application sharing, Administer your apps, Deploying applications, Building applications]
---

# Manage customizations to applications

You can manage your company's customizations for applications that belong to other organizations or a scoped ServiceNow plug-in.

## Before you begin

Role required: admin

The entitlements of your company's application-customizations are controlled solely by the entitlements of the respective store or vendor-released application. There are no separate entitlements for application-customizations, so you can't customize instances that don't have an entitlement to a base store application.

The development instance that you are using to create application-customizations should have its respective store or plugin application entitled and installed.

**Note:** ISV partners who want to customize their own applications must first publish to the ServiceNow Store and install on an instance before they can use application-customizations via the Application Repository. This is the case even though all of the records are in the same scope. Installing on the instance enables ISV partners to publish a different set of capabilities for ServiceNow Store applications versus extensions used internally for their own use.

## About this task

You cannot change the actual applications that belong to other organizations \(purchased from the Store\) or the global plugins provided in the ServiceNow base system. But you can create and manage your company's customizations for store applications or scoped applications that are installed via plugins, using the ServiceNow Application Repository.

There are two ways to create application-customizations.

-   Create from ServiceNow Studio
-   Create from the navigation pane

**Important:** An App Customization package is intended to be authoritative and a full representation of the desired changes or customizations of the application that you're building on top of. Local customizations \(typically tied to the sys\_update\_xml\) are not honored because of this. If a specific field must be persisted \(for example a MID Server\) – consider using the Loader exempt attribute, see Altering tables and fields using dictionary attributes. If a specific property must be set – consider making it ‘private’, see Available system properties.

## Procedure

1.  Use these steps to create application-customizations from ServiceNow Studio.

    1.  Open the Store application or the application installed via plugin from ServiceNow Studio.

        To learn more, see [Legacy - Access ServiceNow Studio](t_AccessStudio.md).

        The application opens in Studio.

    2.  Make application changes from Studio.

2.  Use these steps to create application-customizations from the navigation pane.

    1.  Navigate to **System Applications** **&gt;All**.

    2.  Search for the installed application you want to customize.

        **Note:** You can open the application in either Studio or select it as the current working application in the Store application record.

    3.  To open this application in Studio, select the stack menu, and then select **Edit in Studio**.

        The application opens in Studio. You can make application changes from Studio.

    4.  To edit the Store application record, select the name of the application.

    5.  In the Related Links section of the Store application record, select **Switch to this Application**.

        The application becomes the current working application in the Application picker. You can make application changes from the Store application record.


**Related topics**  


[Manage application entitlements from the application repository](manage-app-entitlements.md)

