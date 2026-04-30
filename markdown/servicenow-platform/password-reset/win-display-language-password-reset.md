---
title: Enable the Password Reset Windows Application to set the display language for the session
description: When the Password Reset Windows Application starts, the application passes the Windows language code to the instance. The instance then dynamically sets the language for the guest user session.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installing and configuring Password Reset Windows Application, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable the Password Reset Windows Application to set the display language for the session

When the Password Reset Windows Application starts, the application passes the Windows language code to the instance. The instance then dynamically sets the language for the guest user session.

## Before you begin

Role required: admin

## Procedure

1.  On the Windows computer: Set the **Welcome screen display language** property to the preferred language.

2.  On the instance:

    1.  Activate the plugin for the preferred language.

    2.  Ensure that no record in the \[sys\_user\_preference\] table specifies a particular **user.language** for **guest** user.

        You clear the setting for a **guest** user to enable the instance to dynamically set the language during the session.


**Parent Topic:**[Installing and configuring Password Reset Windows Application](../concept/install-configure-password-reset-windows-app.md)

