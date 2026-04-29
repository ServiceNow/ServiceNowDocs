---
title: Smart Card in RPA Hub
description: Smart card login for a Windows machine is a secure method of logging into the system using a physical smart card instead of a username and password. It’s commonly used in organizations to enhance security, particularly in environments with high security requirements.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Secure login method for Windows machine, Smart Card for login to Windows machine]
breadcrumb: [Credential Management, Use, RPA Hub, Workflow Data Fabric]
---

# Smart Card in RPA Hub

Smart card login for a Windows machine is a secure method of logging into the system using a physical smart card instead of a username and password. It’s commonly used in organizations to enhance security, particularly in environments with high security requirements.

With Robotic Process Automation \(RPA\), you can run unattended automations on the machines that use smart cards for authentication. While configuring a robot credential, you can store the smart card username and password to allow the unattended robot to log in to machines that use smart card.

## Smart Card limitations

An intermittent issue is observed where Smart Card auto-login fails after a full sign-out, displaying the message: "Signing in with a smart card isn't supported for your account." This occurs only during automated login attempts post sign-out, while lock/unlock scenarios remain unaffected. The issue is a known infrastructure limitation. As a workaround, users are advised to use lock/unlock flows or implement a delay or retry mechanism after sign-out.

## Robotic Process Automation \(RPA\)

For more information and how to set up RPA, see [RPA Hub](rpa-hub-landing-page.md).

