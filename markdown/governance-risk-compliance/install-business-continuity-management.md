---
title: Install Business Continuity Management from ServiceNow Store
description: You can install the Business Continuity Management application if you have the admin role. This application includes demo data and installs the related store applications if they are not already installed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [BCM and ServiceNow Store, Configure, Business Continuity Management, Governance, Risk, and Compliance]
---

# Install Business Continuity Management from ServiceNow Store

You can install the Business Continuity Management application if you have the admin role. This application includes demo data and installs the related store applications if they are not already installed.

## Before you begin

Role required: admin

In the ServiceNow Store, you must verify that you have entitlements \(or licenses\) to the application and its dependent applications.

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

    The navigation path is shown in the example.

    ![Navigation path for installing the application.](../image/install-menu.png)

2.  Find the Business Continuity Management application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

    The path using the filter criteria is shown in the examples.

    ![Application manager.](../image/install-application-manager.png)![Selecting the applications.](../image/bcm-install-select-install.png)

3.  Select **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    Review the application listing in the instance for information on dependencies, licensing or subscription requirements, and release compatibility.

    ![Review installation details.](../image/bcm-install-review-details.png)

    The Business Continuity Management application \(com.snc.sn\_bcm\) requires that the required applications are downloaded as shown in the example.

    ![Required applications.](../image/bcm-install-dependencies-roles.png)

    -   BCM core \(com.snc.bcm.app\_bcm\_core\)
    -   BIA \(com.snc.bcm.app\_bcm\_bia\)
    -   BCP \(com.snc.bcm.app\_bcm\_planning\)
    -   Crisis Management \(com.snc.bcm.app\_bcm\_exercise\)
    -   Crisis Map with Everbridge integration \(com.snc.bcm.app\_crisis\_ebn\_intg\)
    -   Data registry \(com.snc.data\_registry\_dep\)
    -   Gantt UI Builder Component \(servicenow-now-gantt\)
    -   Data registry application \(app-grc-data-registry\)
    -   Document Templates \(app-document-templates\)
    -   Data relationship framework \(app-grc-relationship-config\)
    -   GRC Common Workspace \(app-grc-base-workspace\)
    -   GRC: Approver Configurator \(app-bcm-approval-config\)
    -   IRM shared components \(irm-shared-common-components\)
5.  If demo data is available and you want to load it, select **Load demo data**.

    Some applications include demo data, which are sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Note:** If you do not select the **Load demo data** check box for a store application during installation, demo data is not available to install from the **Application Manager** later. For information on how to install or reinstall demo data after the initial installation, see the [Workaround to install demo data if application is already installed \[KB0722909\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0722909) article in the HI Knowledge Base.

6.  Select **Install**.

    **Note:** Installing GRC: Business Impact Analysis, GRC: Business Continuity Planning, or GRC: Crisis Management automatically installs GRC: Business Continuity Management – Core and GRC: Business Continuity Management – Components.


**Parent Topic:**[Business Continuity Management and ServiceNow Store](../concept/bcm-and-store.md)

