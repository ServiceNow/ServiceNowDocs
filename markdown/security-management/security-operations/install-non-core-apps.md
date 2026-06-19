---
title: Install a Security Operations integration
description: All ServiceNow integrations are available on the ServiceNow Store. Core applications, such as Security Incident Response, are visible in the ServiceNow Products tab on the store. Integration add-ons are visible in the Certified Apps tab.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-operations/install-non-core-apps.html
release: australia
product: Security Operations
classification: security-operations
topic_type: task
last_updated: "2026-03-12"
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

    \[Omitted image "config\_tiles.png"\] Alt text: Configuration tiles for integrations

2.  Locate the integration you want to install and click **Configure**.

    The selected integration is shown in the ServiceNow Store

    \[Omitted image "palo\_alto.png"\] Alt text: Store application

3.  Click **View Dependencies** and review the app dependencies listed.

    \[Omitted image "dependency-notice-palo-alto.png"\] Alt text: Dependency Notice

4.  If the integration has any core application dependencies, such as Security Incident Response, to which your company is not yet entitled:

    1.  [Follow these instructions to obtain entitlements, download dependency plugins, and activate the applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-operations/download-app-first-time.md).

    2.  Return to this procedure.

    3.  Click **Continue**.

5.  Click **Get**.

    The ServiceNow Terms and Conditions appear.

6.  Click **Continue**.

    A Purchase screen similar to the following opens.

    \[Omitted image "integration-purchase.png"\] Alt text: Purchase screen

7.  Identify which instances you want the integration to be available on, manage your notifications, and select the **ServiceNow Store Addendum** check box.

8.  Click **Get**.

    **Note:** If you are downloading an application for purchase, click **Buy**. If you are downloading an application that requires you to get prior approval from the vendor, click **Request App**.

9.  Enter the instance name and a reason for the request, then click **Request**.

    You are sent an email with detailed installation instructions.

10. Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

    A list of applications available for installation is displayed.

11. Locate the application, select it, and click **Install**.

    Your integration is automatically installed on your instance.


