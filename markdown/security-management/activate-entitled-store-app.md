---
title: Activate a ServiceNow Store application
description: After an application has been given entitlement, you must activate its dependencies plugin and activate the application. This process also applies to applications downloaded to sub-production instances.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Download an application from the ServiceNow Store for the first time, Security Operations and the ServiceNow Store, Security Operations]
---

# Activate a ServiceNow Store application

After an application has been given entitlement, you must activate its dependencies plugin and activate the application. This process also applies to applications downloaded to sub-production instances.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

    ![System applications](../image/system-apps.png)

    **Note:** Starting with Orlando, dependency plugins are automatically activated when you activate a core application. For example, when you activate the Vulnerability Response application, the Vulnerability Response Dependencies plugin is also activated. Hence, steps 2 through 5 are optional.

2.  Search for the dependencies plugin for the application you want to activate.

    For example, if you are activating Security Incident Response, locate the Security Incident Response Dependencies plugin.

    ![Locating the Security Incident Response Dependencies plugin](../image/sir-dependencies.png)

3.  Click **Install**.

    The Activate Plugin dialog box appears.

    ![Activate dependency plugin](../image/sir-dep-plugin.png)

4.  In the **Activate Plugin** dialog box, click **Activate**.

5.  When the activation is complete, click **Close &amp; Reload Form**.

6.  Now locate the core product you are activating, click the **Install with demo data** check box if you want to load demo data, and click **Install**.

    Your application is automatically installed on your instance.

    **Note:** If you do not select the **Install with demo data** check box, demo data is not available to install from the **Application Manager** later. For information on how to install or reinstall demo data after the initial installation, see the [Work around to install demo data if application is already installed \[KB0722909\]](https://support.servicenow.com/kb_view.do?sys_kb_id=71c74d03db7e6f807d3e02d5ca9619fe) article in the HI Knowledge Base.


