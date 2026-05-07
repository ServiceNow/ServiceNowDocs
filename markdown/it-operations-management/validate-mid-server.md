---
title: Validate a MID Server
description: Validate a newly installed MID Server so it can communicate with the ServiceNow instance. During validation, you can optionally define which applications, capabilities, and IP ranges the MID Servers is allowed to use.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-28"
reading_time_minutes: 1
keywords: [ITOM, user roles, Now Assist]
breadcrumb: [ITOM Configuration Console for Discovery, Now Assist for Setup \(ITOM Visibility\), Now Assist for Setup \(ITOM\), IT Operations Management]
---

# Validate a MID Server

Validate a newly installed MID Server so it can communicate with the ServiceNow instance. During validation, you can optionally define which applications, capabilities, and IP ranges the MID Servers is allowed to use.

## Before you begin

Verify the following:

-   You have installed the ITOM Visibility plugin. For more information, see [Install ITOM Visibility using Now Assist for Setup](install-nowassist-setup-itom-visibility.md).
-   You have installed the Now Assist for IT Operations Management plugin. For more information, see [Install Now Assist for IT Operations Management](install-now-assist-itom.md).
-   You're on the Configure IT Operations Management page of the Configuration Console. For more information, see [Access the ITOM Configuration Console](access-itom-config-console-disco.md).

Role required: admin

## About this task

Validating a MID Server establishes trust between ServiceNow and the MID Server, allowing it to securely access credentials and perform automation and Discovery tasks while preventing untrusted systems from executing work on behalf of the instance.

## Procedure

1.  Navigate to **Configuration Summary** &gt; **Discovery** &gt; **Platform foundations**.

2.  Select **Validate MID server**.

3.  Select the Application manager icon \(![](../image/application-manager-icon.png)\).

    The ITOM Infra Services Workspace displays.

4.  In the Total MID Servers list, select the check box next to the MID Server you want to validate.

5.  Select the **Server Actions** drop-down list and select **Validate**.

6.  Select **X** to close the window and return to the Configuration Console.

7.  To complete the setup, select **Mark as configured**.


