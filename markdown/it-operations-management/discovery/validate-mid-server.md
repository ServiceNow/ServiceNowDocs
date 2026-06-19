---
title: Validate a MID Server
description: Validate a newly installed MID Server so it can communicate with the ServiceNow instance. During validation, you can optionally define which applications, capabilities, and IP ranges the MID Servers is allowed to use.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/validate-mid-server.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 1
keywords: [ITOM, user roles, Now Assist]
breadcrumb: [ITOM Configuration Console, Discovery setup, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Validate a MID Server

Validate a newly installed MID Server so it can communicate with the ServiceNow instance. During validation, you can optionally define which applications, capabilities, and IP ranges the MID Servers is allowed to use.

## Before you begin

Verify the following:

-   You're using the Zurich Patch 8 or later version of the ServiceNow AI Platform.
-   You have installed the ITOM Visibility plugin. For more information, see [Install ITOM Visibility using Setup Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/install-nowassist-setup-itom-visibility.md).
-   You have installed the Now Assist for IT Operations Management plugin. For more information, see [Install Now Assist for IT Operations Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/install-na-itom.md).
-   You're on the Configure IT Operations Management page of the Configuration Console. For more information, see [Access the ITOM Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/access-itom-config-console-disco.md).

Role required: admin

## About this task

Validating a MID Server establishes trust between ServiceNow and the MID Server, allowing it to securely access credentials and perform automation and Discovery tasks while preventing untrusted systems from executing work on behalf of the instance.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Discovery** &gt; **Platform foundations**.

2.  Select **Validate MID server**.

3.  Select the Application manager icon \(\[Omitted image "application-manager-icon.png"\]\).

    The ITOM Infra Services Workspace displays.

4.  In the Total MID Servers list, select the check box next to the MID Server you want to validate.

5.  Select the **Server Actions** drop-down list and select **Validate**.

6.  Select **X** to close the window and return to the Configuration Console.

7.  To complete the setup, select **Mark as configured**.


