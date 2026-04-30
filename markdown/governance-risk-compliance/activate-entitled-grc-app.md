---
title: Activate an entitled GRC ServiceNow Store application
description: After an application has been given entitlement, you can activate it. This process applies to applications downloaded to sub-production instances.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Download a GRC application from the ServiceNow Store for the first time, GRC and the ServiceNow Store, Governance, Risk, and Compliance]
---

# Activate an entitled GRC ServiceNow Store application

After an application has been given entitlement, you can activate it. This process applies to applications downloaded to sub-production instances.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

    ![System applications](../../security-incident-response/image/system-apps.png)

    **Note:**

    Starting with Orlando, dependency plugins are automatically activated when you activate a core application. For example, when you activate the Audit Management application, the Audit Management Dependencies plugin is also activated.

    **Important**The information in the previous Note does not apply to the Vendor Risk Management application. If you are activating Vendor Risk Management, proceed with the next step. If you are activating any of the other GRC applications, steps 2 through 5 are optional.

2.  Search for the dependencies plugin for the application you want to activate.

    For example, if you are activating Security Incident Response, locate the Security Incident Response Dependencies plugin.

    ![Dependency plugin](../../security-incident-response/image/sir-dependencies.png)

3.  Click **Install**.

    The Activate Plugin dialog box appears.

    ![Activate dependency plugin](../../security-incident-response/image/sir-dep-plugin.png)

4.  In the Activate Plugin dialog box, click **Activate**.

5.  When the activation is complete, click **Close &amp; Reload Form**.

6.  Locate the core product you are activating.

7.  If you want to load demo data, click the **Load demo data** check box.

8.  Click **Install**.

    Your application is automatically installed on your instance.

    **Note:** If you do not select the **Load demo data** check box, demo data is not available to install from the **Application Manager** later. For information on how to install or reinstall demo data after the initial installation, see the [Work around to install demo data if application is already installed \[KB0722909\]](https://support.servicenow.com/kb_view.do?sys_kb_id=71c74d03db7e6f807d3e02d5ca9619fe) article in the HI Knowledge Base.


