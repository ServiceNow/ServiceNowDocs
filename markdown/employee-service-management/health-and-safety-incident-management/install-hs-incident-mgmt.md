---
title: Install Health and Safety Incident Management
description: You can install the Health and Safety Incident Management application \(sn\_hs\_im\_incident\) if you have the admin role. The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: australia
product: Health and Safety Incident Management
classification: health-and-safety-incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configure, Health and Safety Incident Management, Health and Safety, Employee Service Management]
---

# Install Health and Safety Incident Management

You can install the Health and Safety Incident Management application \(sn\_hs\_im\_incident\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

**Important:**

-   Starting from version 10, the previously known Health and Safety Incident Management \(sn\_ohs\_im\) application has been renamed to Health and Safety Core. There is no impact on existing customers using versions up to 9. However, to receive the latest updates for incident management, customers on version 9 and earlier must also install \(sn\_hs\_im\_incident\).
-   When you upgrade from Health and Safety Incident Management v9 to Health and Safety Core v10, certain reference fields and column labels related to Health and Safety user profile might not update correctly. To resolve this issue, see the [KB article \[KB2057452\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2057452) in the Now Support Knowledge Base to create and run a Fix Script.

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Review the [Health and Safety Incident Management](https://store.servicenow.com/sn_appstore_store.do#!/store/application/f27b42a72f373010f2bf532a2799b693) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

**Tip:** The application installation does not install the location demo data for the Workplace Core location model. The location picker on incident and observation forms is mandatory so that users can't submit these forms unless they are populated with locations. As a workaround, repair the Workplace Core plugin with the **Load demo data** option.

Role required: admin

## About this task

The following items are installed with Health and Safety Incident Management:

-   Plugins
-   Store applications
-   Roles
-   Scheduled jobs
-   Tables

For more information, see [Components installed with Health and Safety Incident Management](../reference/components-installed-with-hs-incident-mgmt.md).

This table lists the optional applications that can be installed for additional features:

<table id="table_ix1_bff_gxb"><thead><tr><th>

Application

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Anonymous Report Center

 \[com.sn\_anonymous\_report\_center\]

</td><td>

Installs anonymous reporting capability for Health and Safety Incident Management.For more information, see [Activate the Anonymous Report Center](../../human-resources/task/arc-activate.md).

To configure the **Anonymous report center**, see [Setting up the Anonymous Report Center](../../human-resources/concept/arc-setup.md).

</td></tr><tr><td>

Expanded Model and Asset Classes

 \[sn\_ent\]

</td><td>

Enables tracking and managing of enterprise assets that are associated with the safety incidents and observations.

</td></tr><tr><td>

Geo map component

 \[sn\_geo\_map\]

</td><td>

Provides access to enable the map component in the Health and Safety Workspace from the application properties.

 To install, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

</td></tr><tr><td>

Geolocation plugin

 \[com.snc.geolocation\]

</td><td>

Enables geolocation feature on the Now Mobile app and gives access to manual tracking options.

 For more information, see [Enabling and selecting location tracking options](https://www.servicenow.com/docs/access?context=location-tracking-enable&version=australia&pubname=australia-mobile&ft:locale=en-US)

</td></tr><tr><td>

Health and Safety Case Management \[sn\_hs\_cm\]

</td><td>

Installs case management capability for Health and Safety Incident Management.For more information, see [Install Health and Safety Case Management](../../hs-case-management/task/install-hs-case-management.md).

</td></tr><tr><td>

Human Resources Scoped App: Core \[com.sn\_hr\_core\]

</td><td>

Installs Case and Knowledge Management for creating HR cases from injury and illness records.For more information, see [Activate Case and Knowledge Management](../../human-resources/task/activate-case-and-knowledge-management-scoped.md).

**Note:** For creating HR cases from injury and illness records, this plugin needs to be activated together with the Health and Safety Case Management \(sn\_hs\_cm\) application. For more information, see [Create an HR case from an injury or illness](create-hr-case-injury-illness.md).

</td></tr><tr><td>

Health and Safety Contractor Management \[sn\_hs\_crm\]

</td><td>

Installs contractor management capability for Health and Safety Incident Management.For more information, see [Install Health and Safety Contractor Management](../../hs-contractor-management/task/hs-install-contractor-management.md).

</td></tr><tr><td>

Health and Safety Incident Management OSHA Content Pack\[com.snc.sn\_hs\_im\_osha\]

</td><td>

Installs OSHA reporting capability for Health and Safety Incident Management.For more information, see [Install Health and Safety Incident Management OSHA Content Pack](install-hs-osha-content-pack.md).

</td></tr><tr><td>

Learning Core\[sn\_lc\]

</td><td>

Installs Learning Core to enable learning content in Health and Safety actions.For more information, see [Configuring Learning Core](../../human-resources/concept/configuring-learning-core.md).

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Health and Safety Incident Management application \(sn\_ohs\_im\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions that are available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


**Parent Topic:**[Setting up Health and Safety Incident Management](../concept/setting-up-hs-incident-mgmt.md)

