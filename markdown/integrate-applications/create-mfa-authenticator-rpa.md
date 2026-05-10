---
title: Create an MFA authenticator in RPA Hub
description: Define the authenticator and token length that acts as an enabler for the Time-based One-time Password \(TOTP\) authentication in RPA Hub so that the unattended robots can seamlessly authenticate against multi-factor authentication \(MFA\)-enabled applications.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [authenticate unattended robot rpa hub, authenticate bot rpa hub, unattended robot authentication rpa hub, bot authentication rpa hub]
breadcrumb: [Credential Management, Use, RPA Hub, Workflow Data Fabric]
---

# Create an MFA authenticator in RPA Hub

Define the authenticator and token length that acts as an enabler for the Time-based One-time Password \(TOTP\) authentication in RPA Hub so that the unattended robots can seamlessly authenticate against multi-factor authentication \(MFA\)-enabled applications.

## Before you begin

Familiarize yourself with multi-factor authentication \(MFA\) concepts. For more information, see [Multi-factor authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/mfa-landing.md).

Familiarize yourself with the TOTP authentication in RPA Hub. For more information, see [TOTP authentication in RPA Hub](../concept/totp-authentication-rpa.md).

You must do this task in the classic environment.

Role required: sn\_rpa\_fdn.rpa\_release\_manager or sn\_rpa\_fdn.rpa\_admin

## About this task

An authenticator application is a third-party software that generates temporary passcodes. Users can use these passcodes along with their password to log in to an instance that requires multi-factor authentication \(MFA\). For example, the following applications support Time-based One-time Passwords \(TOTP\):

-   Google Authenticator
-   Microsoft Authenticator
-   Okta Verify

For more detail on these applications, see [Authenticator Applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/mfa-auth-app.md).

The MFA authenticator record acts as an input to the Time-based One-time Password \(TOTP\) authenticator.

After you create an MFA authenticator record, all the fields are read-only.

You can't edit an MFA authenticator record. If changes are required to an existing MFA record, you must retire an existing record and then create an MFA authenticator record.

## Procedure

1.  Navigate to **All** &gt; **Robotic Process Automation** &gt; **Administration** &gt; **Authenticators**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_pyx_mhd_4qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name of the MFA authenticator.For example, Google Authenticator.

</td></tr><tr><td>

Token Length

</td><td>

Length of the generated Time-based One-time Password \(TOTP\) that depends on the authenticator you have selected:-   **6**- The minimum length of the TOTP that is generated.
-   7
-   8
-   **9**- The maximum length of the TOTP that is generated.


</td></tr><tr><td>

Life Cycle Stage Status

</td><td>

Status of the life-cycle stage of the MFA authenticator:-   **In Use**- This value is the default.
-   **Retired**


</td></tr></tbody>
</table>4.  Select **Submit**.


## What to do next

Create a TOTP authenticator. For more information, see [Create a TOTP authenticator in RPA Hub](map-totp-credential-set-rpa.md).

**Related topics**  


[Retire an MFA authenticator in RPA Hub](retire-mfa-authenticator.md)

[Delete a TOTP authenticator in RPA Hub](delete-mfa-authenticator-rpa.md)

