---
title: TOTP authentication in RPA Hub
description: You can configure the Time-based One-time Password \(TOTP\) fields in RPA Hub that enable the unattended robots to seamlessly authenticate against multi-factor authentication \(MFA\)-enabled applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Credential Management, Use, RPA Hub, Workflow Data Fabric]
---

# TOTP authentication in RPA Hub

You can configure the Time-based One-time Password \(TOTP\) fields in RPA Hub that enable the unattended robots to seamlessly authenticate against multi-factor authentication \(MFA\)-enabled applications.

## Overview of TOTP authentication

An authenticator application is third-party software that generates temporary passcodes. Users can use these passcodes with their password to log in into an instance that requires multi-factor authentication \(MFA\).

TOTP authentication secures the seed storage of the authenticator at the instance level. The seed is the secret key of the authenticator that is used to generate the TOTP.

Familiarize yourself with multi-factor authentication \(MFA\) concepts. For more information, see [Multi-factor authentication](https://www.servicenow.com/docs/access?context=mfa-landing&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## TOTP authentication architecture

The secret key \(**Seed**\) resides in the RPA Hub server.

The decrypted TOTP is passed to the Unattended Robot and RPA Desktop Design Studio through a secure channel.

The following diagram shows the architecture of the TOTP authentication in RPA Hub.

![Architecture of the TOTP authentication in RPA Hub.](../image/totp-architecture-rpa.png "Architecture of the TOTP authentication in RPA Hub")

## New fields and tables configuration

To enable TOTP authentication in the RPA Hub, do the following actions:

-   Create a multi-factor authentication \(MFA\) authenticator record in the classic environment. For more information, see [Create an MFA authenticator in RPA Hub](../task/create-mfa-authenticator-rpa.md).
-   Associate a TOTP authenticator to a robot credential with the secret key \(Seed\). You can do this task in the workspace and classic environment. For more information, see [Create a TOTP authenticator in RPA Hub](../task/map-totp-credential-set-rpa.md).

In the RPA Desktop Design Studio, as an RPA developer, you can define the GetTOTP component \(previously known as the getOKTAtoken component\) with AuthenticatorName as an input parameter. The authenticator name that you provide from the component is compared against the unique authenticator name in the TOTP record. If the comparison is successful, the TOTP password is generated. For more information, see [Use the GetTOTP component](../../rpa-studio/task/use-utilities-token-getoktatoken.md).

**Related topics**  


[Delete a TOTP authenticator in RPA Hub](../task/delete-mfa-authenticator-rpa.md)

[Retire an MFA authenticator in RPA Hub](../task/retire-mfa-authenticator.md)

