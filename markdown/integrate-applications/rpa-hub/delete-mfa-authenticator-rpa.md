---
title: Delete a TOTP authenticator in RPA Hub
description: Delete a Time-based One-time Password \(TOTP\) authenticator record in RPA Hub so that you can dissociate it from a bot process.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, RPA Hub, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Delete a TOTP authenticator in RPA Hub

Delete a Time-based One-time Password \(TOTP\) authenticator record in RPA Hub so that you can dissociate it from a bot process.

## Before you begin

Familiarize yourself with multi-factor authentication \(MFA\) concepts. For more information, see [Multi-factor authentication](https://www.servicenow.com/docs/access?context=mfa-landing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

Familiarize yourself with the TOTP authentication in RPA Hub. For more information, see [TOTP authentication in RPA Hub](../concept/totp-authentication-rpa.md).

Create a multi-factor authentication \(MFA\) authenticator record. For more information, see [Create an MFA authenticator in RPA Hub](create-mfa-authenticator-rpa.md).

Map a TOTP authenticator to a robot credential in RPA Hub. For more information, see [Create a TOTP authenticator in RPA Hub](map-totp-credential-set-rpa.md).

Verify if the life-cycle stage status of the associated bot process is either set to **Build** or **In Maintenance**.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **RPA Hub Workspace**.

2.  Select the list icon \(![List icon.](../image/rpahublist-icon.png)\).

3.  On the **Lists** tab, under **Credential Management**, select **Robot Credentials**.

4.  Open the robot credential record that you want to dissociate the TOTP authenticator record from.

5.  On the **TOTP Authenticators** tab, select the TOTP authenticator that you want to delete.

6.  Select **Delete**.


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

**Related topics**  


[Retire an MFA authenticator in RPA Hub](retire-mfa-authenticator.md)

