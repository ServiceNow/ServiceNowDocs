---
title: Set up ServiceNow Cowork
description: Connect Cowork to your ServiceNow instance and prepare your workspace and secure sandbox.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/set-up-cowork.html
release: zurich
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [Set up Cowork]
breadcrumb: [Configure, ServiceNow Cowork, Enable AI experiences]
---

# Set up ServiceNow Cowork

Connect Cowork to your ServiceNow instance and prepare your workspace and secure sandbox.

## Before you begin

Role required: sn\_app\_cowork.admin or sn\_app\_cowork.user

## Procedure

1.  Select and open the ServiceNow Cowork application.

2.  When macOS asks for access to your keychain, enter your login keychain password, and then select **Always Allow** or **Allow** to grant access for this session only.

    Your login keychain is your macOS password.

3.  On the Meet ServiceNow Cowork screen, select **Get Started**.

4.  On the Connect ServiceNow screen, enter your instance name in the **Instance URL** field.

5.  Select a sign in method.

    -   **Sign in within ServiceNow Cowork**: Use your password or PIN.
    -   **Sign in via browser**: Use any sign in option your instance supports, such as SSO.
6.  Select **Sign in with ServiceNow**.

7.  Enter your user name and password, and then select **Log in**.

8.  If the Update Required dialog appears, select **Update &amp; Restart**.

    After Cowork restarts, sign in again.

9.  On the Workspace &amp; Security screen, confirm the default workspace folder or select **Choose** to pick a different folder.

10. Monitor the secure sandbox setup progress.

    Setup completes when **Secure Sandbox** shows **Ready** and these checks finish:

    -   Rootfs image ready
    -   OpenShell gateway started
    -   MicroVM sandbox ready
    If setup stalls or fails, select **Retry**.

11. Select **Continue**.

12. On the You're All Set screen, confirm the model that Cowork uses, and then select **Start Using ServiceNow Cowork**.


## Result

Cowork opens and is ready to use. You can change your workspace and other options anytime in **Settings**.

**Parent Topic:**[Configuring ServiceNow Cowork](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/servicenow-cowork-configuring.md)

