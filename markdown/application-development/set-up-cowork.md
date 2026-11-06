---
title: Set up ServiceNow Arc
description: Connect Arc to your ServiceNow instance and prepare your workspace and secure sandbox.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/set-up-cowork.html
release: australia
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [Set up Cowork]
breadcrumb: [Configure, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Set up ServiceNow Arc

Connect Arc to your ServiceNow instance and prepare your workspace and secure sandbox.

## Before you begin

Role required: sn\_app\_arc.admin or sn\_app\_arc.user

## Procedure

1.  Select and open the ServiceNow Arc application.

2.  When macOS asks for access to your keychain, enter your login keychain password, and then select **Always Allow** or **Allow** to grant access for this session only.

    Your login keychain is your macOS password.

3.  On the Meet ServiceNow Arc screen, select **Get Started**.

4.  On the Connect ServiceNow screen, enter your instance name in the **Instance URL** field.

5.  Select a sign in method.

    -   **Sign in within ServiceNow Arc**: Use your password or PIN.
    -   **Sign in via browser**: Use any sign in option your instance supports, such as SSO.
6.  Select **Sign in with ServiceNow**.

7.  Enter your user name and password, and then select **Log in**.

8.  If the Update Required dialog appears, select **Update &amp; Restart**.

    After Arc restarts, sign in again.

9.  On the Workspace &amp; Security screen, confirm the default workspace folder or select **Choose** to pick a different folder.

10. Monitor the secure sandbox setup progress.

    Setup completes when **Secure Sandbox** shows **Ready** and these checks finish:

    -   Rootfs image ready
    -   OpenShell gateway started
    -   MicroVM sandbox ready
    These checks apply to macOS. On Windows, Arc uses a different sandbox, so the checks shown can differ.

    If setup stalls or fails, select **Retry**.

11. Select **Continue**.

12. On the You're All Set screen, confirm the model that Arc uses, and then select **Start Using ServiceNow Arc**.


## Result

Arc opens and is ready to use. You can change your workspace and other options anytime in **Settings**.

## What to do next

For more information about resolving common issues, see [Troubleshoot Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/troubleshoot-arc.md).

**Parent Topic:**[Configuring ServiceNow Arc](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-configuring.md)

