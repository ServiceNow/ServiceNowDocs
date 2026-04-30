---
title: Install Operational Technology Incident Management
description: You can install the Operational Technology Incident Management application \(sn\_ot\_inc\_mgmt\) if you have the admin role. The application installs related ServiceNow Store applications and plugins if they are not already installed.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the above sentence. Changed Service to Incident in these topics.
locale: en-US
release: yokohama
product: Operational Technology Incident Management
classification: operational-technology-incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configure, Operational Technology Incident Management, Operational Technology]
---

# Install Operational Technology Incident Management

You can install the Operational Technology Incident Management application \(sn\_ot\_inc\_mgmt\) if you have the admin role. The application installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Operational Technology Incident Management requires the following plugins. Ensure that these plugins are activated before you install Operational Technology Incident Management.
    -   **Required ServiceNow plugins**
        -   **CMDB CI Class Models \(sn\_cmdb\_ci\_class\)**

            The CMDB CI Class Models store app adds class models that extend the CMDB class hierarchy, including class descriptions, identification rules, identifier entries, and dependent relationships. For more information, see [CMDB CI Class Models store app](https://www.servicenow.com/docs/access?context=cmdb-ci-class-models&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

        -   **ISA Equipment Model \(sn\_isa\_model\)**

            The data model for ISA-95 equipment model entities and templates. For more information, see [ISA-95 equipment model](../../mftg-manufacturing-process-mgr/concept/isa-95-equipment-model.md).

-   Operational Technology Incident Management requires either one or both of the following ServiceNow Store applications. Ensure that at least one of these applications is installed before you install Operational Technology Incident Management.
    -   **Required ServiceNow Store applications**
        -   **Operational Technology Manager**

            The Operational Technology Manager application creates the foundational data and relationships that enables your enterprise to use the ServiceNow® Operational Technology solution. Operational Technology Manager supports the use of the Configuration Management Database \(CMDB\), Service Graph Connectors, and Discovery applications in the ServiceNow AI Platform. For more information, see [Configuring the Operational Technology Manager](../../mftg-manufacturing-oper-tech-mgr/concept/configuring-operational-technology-manager.md).

        -   **Industrial Process Manager**

            The Industrial Process Manager application creates the ISA-95 Equipment Model data foundation that is required for the ServiceNow® Industrial solution, enabling you to create your own version of the equipment models in each of your industrial sites. For more information, see [Configuring the Industrial Process Manager](../../mftg-manufacturing-process-mgr/concept/configuring-manufacturing-process-mgr.md).

-   Role required: admin

## About this task

The following items are installed with Operational Technology Incident Management:

-   Plugins
-   Store applications
-   Roles and ACLs

For more information about the roles and ACLs installed, see [Components installed with Operational Technology Incident Management](../reference/components-installed-with-operational-technology-service-management.md).

**Note:** For Operational Technology Service Management users with no license for Operational Technology Visibility, note the following:

-   When you have the latest version of Operational Technology Incident Management installed, Industrial Process Manager is also installed.
-   When you have the latest version of Operational Technology Change Management installed, Industrial Process Manager is also installed.

You should upgrade to the latest versions so you have access to the Operational Technology Service Management experience.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Operational Technology Incident Management application \(sn\_ot\_inc\_mgmt\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install Operational Technology Incident Management.

4.  Select **Install**.


**Parent Topic:**[Configuring Operational Technology Incident Management](configuring-operational-technology-incident-mgt.md)

