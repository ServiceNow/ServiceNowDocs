---
title: Retire an MFA authenticator in RPA Hub
description: Retire a multi-factor authentication \(MFA\) authenticator in RPA Hub so that you can turn off the authentication. After you retire an MFA authenticator, it can’t be used again.
locale: en-US
release: yokohama
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing RPA Hub, RPA Hub, Robotic Process Automation \(RPA\) Hub, Data and Automation]
---

# Retire an MFA authenticator in RPA Hub

Retire a multi-factor authentication \(MFA\) authenticator in RPA Hub so that you can turn off the authentication. After you retire an MFA authenticator, it can’t be used again.

## Before you begin

Familiarize yourself with multi-factor authentication \(MFA\) concepts. For more information, see [Multi-factor authentication](https://www.servicenow.com/docs/access?context=mfa-landing&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

Familiarize yourself with the TOTP authentication in RPA Hub. For more information, see [TOTP authentication in RPA Hub](../concept/totp-authentication-rpa.md).

You must do this task in the classic environment.

Create an MFA authenticator record. For more information, see [Create an MFA authenticator in RPA Hub](create-mfa-authenticator-rpa.md).

Verify that the MFA authenticator record isn’t associated to a bot process whose life-cycle stage status is **Build**, **Published**, or **Retired**. If it's not associated to one of those statuses, dissociate it to retire the MFA authenticator.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Administration** &gt; **Authenticators**.

2.  Open the MFA authenticator that you want to retire.

3.  In the form header, select **Retire**.

4.  In the Confirmation dialog box, select **Retire**.


**Parent Topic:**[Managing RPA Hub](../concept/managing-rpa-hub.md)

**Related topics**  


[Retire an RPA Hub bot process](retire-bot-process.md)

