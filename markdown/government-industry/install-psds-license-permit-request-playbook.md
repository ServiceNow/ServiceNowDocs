---
title: Install License and Permit Playbook for Public Sector Digital Services
description: You can install the License and Permit Playbook application \(sn\_gsm\_lic\_prmt\) if you have the admin role.If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plug-ins if they aren’t already installed.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [License and Permit Playbook, Playbooks, Configure Agent Workspaces, Configuring Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Install License and Permit Playbook for Public Sector Digital Services

You can install the License and Permit Playbook application \(sn\_gsm\_lic\_prmt\) if you have the admin role.The application includes demo data and installs related ServiceNow® Store applications and plug-ins if they aren’t already installed.

## Before you begin

-   Ensure that the application and all of its associated ServiceNow Store applications have valid ServiceNow entitlements. For more information, see [Get entitlement for a ServiceNow product or application](https://store.servicenow.com/$appstore.do#!/store/help?article=KB0030186).
-   Certain features in the License and Permit Playbook application are available based on your ServiceNow entitlements and may require installation of other ServiceNow applications and activation of specific plug-ins.

    **Note:** Install the [Playbooks for Customer Service Management](https://store.servicenow.com/sn_appstore_store.do#!/store/application/7be17355874010108ef7a7da0acb0bb5/2.1.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPlaybooks%2520for%2520Customer%2520Service%2520Management&sl=sh) application to enable the playbook experience.

-   Review the [License and Permit Playbook](https://store.servicenow.com/sn_appstore_store.do#!/store/application/50f57c9d93d4f950e3e7b0627cba1045) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

The License and Permit Request \[sn\_gsm\_license\_permit\_case\] table is installed with License and Permit Playbook.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the License and Permit Playbook application \(sn\_gsm\_lic\_prmt\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find the application, you might have to request it from the ServiceNow Store.

    In the list next to the **Install** button, the versions available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data are sample records that describe application features for common use cases. Load the demo data when you first install the application on a development or test instance.

6.  Select **Install**.


