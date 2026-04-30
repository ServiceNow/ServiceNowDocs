---
title: Smart Card in RPA Hub
description: Smart card login for a Windows machine is a secure method of logging into the system using a physical smart card instead of a username and password. It’s commonly used in organizations to enhance security, particularly in environments with high security requirements.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-05-13"
reading_time_minutes: 1
keywords: [Secure login method for Windows machine, Smart Card for login to Windows machine]
breadcrumb: [Exploring RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Smart Card in RPA Hub

Smart card login for a Windows machine is a secure method of logging into the system using a physical smart card instead of a username and password. It’s commonly used in organizations to enhance security, particularly in environments with high security requirements.

With Robotic Process Automation \(RPA\), you can run unattended automations on the machines that use smart cards for authentication. While configuring a robot credential, you can store the smart card username and password to allow the unattended robot to log in to machines that use smart card. For more information about configuring Smart Card for an unattended robot, see [Create a robot credential in RPA Hub](../task/create-credential-set-botprocess.md).

## Smart Card limitations

-   Authentication support - Smart Card certificate-based authentication is supported only for single unattended RPA sessions. Smart Card authentication is not supported in high-density \(multi-session\) environments.
-   Credential type consistency - If a robot runs multiple processes, all Windows logins must use the same credential type—either Smart Card or Windows username and password.
-   Execution timing - Allow adequate time between process executions, including time for logout, to ensure proper session initialization and prevent authentication conflicts.

