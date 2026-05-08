---
title: Install Operational Technology Change Management
description: You can install the Operational Technology Change Management application \(sn\_ot\_chg\_mgmt\) if you have the admin role.
locale: en-US
release: australia
product: Operational Technology Change Management
classification: operational-technology-change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Operational Technology Change Management, Operational Technology]
---

# Install Operational Technology Change Management

You can install the Operational Technology Change Management application \(sn\_ot\_chg\_mgmt\) if you have the admin role.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   The Operational Technology Change Management application requires the following plugins. Ensure that these plugins are activated before you install the Operational Technology Change Management application.
    -   **Required ServiceNow plugins**
        -   **CMDB CI Class Models \(sn\_cmdb\_ci\_class\)**

            The Configuration Management Database \(CMDB\) CI Class Models store app adds class models that extend the CMDB class hierarchy, including the class descriptions, identification rules, identifier entries, and dependent relationships. For more information, see CMDB CI Class Models store app.

        -   **ISA Equipment Model \(sn\_isa\_model\)**

            The data model for ISA-95 equipment model entities and templates. For more information, see [ISA-95 equipment model](../../mftg-manufacturing-process-mgr/concept/isa-95-equipment-model.md).

-   The Operational Technology Change Management application requires either one or both of the following ServiceNow Store applications. Ensure that at least one of these applications is installed before you install the Operational Technology Change Management application.
    -   **Required ServiceNow Store applications**
        -   **Operational Technology Manager**

            The Operational Technology Manager application creates the foundational data and relationships that enable your organization to use the Operational Technology solution. The Operational Technology Manager application supports the use of the Configuration Management Database \(CMDB\), Service Graph Connectors, and Discovery applications in the ServiceNow AI Platform. For more information, see [Configuring the Operational Technology Manager](../../mftg-manufacturing-oper-tech-mgr/concept/configuring-operational-technology-manager.md).

        -   **Industrial Process Manager**

            The Industrial Process Manager application creates the ISA-95 Equipment Model data foundation that is required for the ServiceNow® Industrial solution, enabling you to create your own version of the equipment models in each of your industrial sites. For more information, see [Configuring the Industrial Process Manager](../../mftg-manufacturing-process-mgr/concept/configuring-manufacturing-process-mgr.md).


Role required: admin

## About this task

The following items are installed with the Operational Technology Change Management application:

-   Plugins
-   Store applications
-   Roles and ACLs

For more information about the roles and ACLs installed, see [Components installed with Operational Technology Change Management](../reference/components-installed-with-operational-technology-change-request.md).

**Note:** For Operational Technology Service Management users with no license for Operational Technology Visibility, note the following:

-   When you have the latest version of Operational Technology Incident Management installed, Industrial Process Manager is also installed.
-   When you have the latest version of Operational Technology Change Management installed, Industrial Process Manager is also installed.

You should upgrade to the latest versions so you have access to the Operational Technology Service Management experience.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Operational Technology Change Management application by using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can’t find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they’ll be installed, are currently installed, or must be installed. If any plugins or applications must be installed, you must install them before you can install the Operational Technology Change Management application.

4.  Select **Install**.


**Parent Topic:**[Configuring Operational Technology Change Management](../concept/configuring-operational-technology-change-request.md)

