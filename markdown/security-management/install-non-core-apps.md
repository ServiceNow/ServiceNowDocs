---
title: Install a Security Operations integration
description: All ServiceNow integrations are available on the ServiceNow Store. Core applications, such as Security Incident Response, are visible in the ServiceNow Products tab on the store. Integration add-ons are visible in the Certified Apps tab.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Security Operations and the ServiceNow Store, Security Operations]
---

# Install a Security Operations integration

All ServiceNow integrations are available on the ServiceNow Store. Core applications, such as Security Incident Response, are visible in the **ServiceNow Products** tab on the store. Integration add-ons are visible in the **Certified Apps** tab.

## Before you begin

Role required: admin

Store installations require a Now Support account and permission to request applications for the instances under consideration.

## Procedure

1.  Navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations** after you install the application from ServiceNow store.

    Configuration tiles for the integrations appears

    **Note:**

    ![Configuration tiles for integrations](../image/config_tiles.png)

2.  Locate the integration you want to install and click **Configure**.

    The selected integration is shown in the ServiceNow Store

    ![Store application](../image/palo_alto.png)

3.  Click **View Dependencies** and review the app dependencies listed.

    ![Dependency Notice](../image/dependency-notice-palo-alto.png)

4.  If the integration has any core application dependencies, such as Security Incident Response, to which your company is not yet entitled:

    1.  [Follow these instructions to obtain entitlements, download dependency plugins, and activate the applications](../reference/download-app-first-time.md).

    2.  Return to this procedure.

    3.  Click **Continue**.

5.  Click **Get**.

    The ServiceNow Terms and Conditions appear.

6.  Click **Continue**.

    A Purchase screen similar to the following opens.

    ![Purchase screen](../image/integration-purchase.png)

7.  Identify which instances you want the integration to be available on, manage your notifications, and select the **ServiceNow Store Addendum** check box.

8.  Click **Get**.

    **Note:** If you are downloading an application for purchase, click **Buy**. If you are downloading an application that requires you to get prior approval from the vendor, click **Request App**.

9.  Enter the instance name and a reason for the request, then click **Request**.

    You are sent an email with detailed installation instructions.

10. Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

    A list of applications available for installation is displayed.

11. Locate the application, select it, and click **Install**.

    Your integration is automatically installed on your instance.


