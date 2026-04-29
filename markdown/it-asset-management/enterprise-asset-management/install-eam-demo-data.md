---
title: Install EAM Demo Data
description: You can install the EAM Demo Data application \(com.sn\_eam\_demo\_data\) if you have the admin role. The application includes demo data for the Enterprise Asset Management application.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Enterprise Asset Management, IT Asset Management]
---

# Install EAM Demo Data

You can install the EAM Demo Data application \(com.sn\_eam\_demo\_data\) if you have the admin role. The application includes demo data for the Enterprise Asset Management application.

## Before you begin

**Warning:**

Do not install the EAM Demo Data application in any production environments, as it can cause data loss and corruption. The application is intended for internal use only.

Please consult with your account manager prior to installing the application. If you install the application without prior consent, ServiceNow is not responsible for any data loss or corruption that may occur.

-   Review the [EAM Demo Data](https://store.servicenow.com/sn_appstore_store.do#!/store/application/6b695412ff2e62103233ffffffffff30/1.0.0) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.
-   Install the Enterprise Asset Management \(com.sn\_eam\) application or one of the following Enterprise Asset Management-dependent applications on your ServiceNow instance:

    **Note:** For instructions on how to install the Enterprise Asset Management application, see [Install Enterprise Asset Management](request-enterprise-asset-management.md).

    -   OT Asset Management \(com.sn\_otam\)

        For instructions on how to install this application, see [Install OT Asset Management](install-otam.md).

    -   Enterprise Asset Management for Healthcare \(com.sn\_eamhc\)

        For instructions on how to install this application, see [Install Enterprise Asset Management for healthcare](install-eam-for-healthcare.md).

    -   Enterprise Asset Management for Facilities \(com.sn\_eamfam\)
    -   Enterprise Asset Management for Data Center and Network Asset Management \(com.sn\_eam\_dcnam\)

        For instructions on how to install this application, see [Install Enterprise Asset Management for Data Center and Network Asset Management \(DCNAM\)](install-eam-dcnam.md).


Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the EAM Demo Data application \(com.sn\_eam\_demo\_data\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    A list of the versions available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select the **Load demo data** check box.

6.  Select **Install**.


