---
title: Install Identity Provider Integration
description: You can install the Identity Provider Integration plugin \(sn\_idp\_integ\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plug-ins if they aren’t already installed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/psds-identity-framework-install.html
release: brazil
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 1
breadcrumb: [Identity Provider Integration, Integrate, Public Sector Digital Services \(PSDS\)]
---

# Install Identity Provider Integration

You can install the Identity Provider Integration plugin \(sn\_idp\_integ\) if you have the admin role.The application includes demo data and installs related ServiceNow® Store applications and plug-ins if they aren’t already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Certain features in the Identity Provider Integration \(sn\_idp\_integ\) application are available based on your ServiceNow entitlements and may require installation of other ServiceNow applications and activation of specific plug-ins.
-   Review the [https://store.servicenow.com/sn\_appstore\_store.do\#!/store/application/f8a220de91070710f87783bc40ac6f96/1.0.1](https://store.servicenow.com/sn_appstore_store.do#!/store/application/f8a220de91070710f87783bc40ac6f96/1.0.1) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the PSDSInvestigative Case Management application \(com.sn\_gsm\_icm\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are the sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


