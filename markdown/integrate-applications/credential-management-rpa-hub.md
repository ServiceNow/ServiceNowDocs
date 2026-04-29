---
title: Credential Management in RPA Hub
description: Streamline the credentials that robots use to perform the automation that you defined in the bot process. Instead of creating the same set of credentials for each bot process, you can create a credential group that includes a robot credential, application credentials, and external credentials. You can then associate the credential group to multiple bot processes.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Use, RPA Hub, Workflow Data Fabric]
---

# Credential Management in RPA Hub

Streamline the credentials that robots use to perform the automation that you defined in the bot process. Instead of creating the same set of credentials for each bot process, you can create a credential group that includes a robot credential, application credentials, and external credentials. You can then associate the credential group to multiple bot processes.

## Credential management overview

If you're an RPA release manager, RPA administrator, or RPA developer, you can create and associate credential groups to an unattended bot process. You can also set up an external credential vault to retrieve the robot credentials, application credentials, or a Time-based One-time Password \(TOTP\) seed from an external source. The seed is the secret key of the authenticator that is used to generate the TOTP. An external credential vault is a secure storage system often used to store and manage sensitive information such as user names, passwords, and other access credentials for various applications, services, or systems.

## Benefits of credential management

With credential management, you can do the following tasks:

-   Define the credentials once and reuse them in multiple bot processes to improve the overall productivity of your resources.
-   Reduce the number of errors that occur when you're configuring the same credential groups for different bot processes.
-   Improve how credentials are accessed with centralized credential management.
-   Securely retrieve the credentials from an external storage system by configuring the external credential vault.

## Robot credentials

By creating robot credentials, you can enable robots to log in to a Windows machine and perform the automation. For more information, see [Create a robot credential in RPA Hub](../task/create-credential-set-botprocess.md).

In the following table, learn what users with different roles can do or can't do.

<table id="table_ilf_qc4_1cc"><thead><tr><th>

Role

</th><th>

Can do

</th><th>

Can't do

</th></tr></thead><tbody><tr><td>

RPA release manager and RPA administrator

</td><td>

Create, view, update, or delete the robot credentials.

</td><td>

-

</td></tr><tr><td>

RPA developer

</td><td>

-   Create the robot credentials.
-   View the robot credentials that are created by them or the robot credentials that are mapped to the bot processes that they’re assigned to.
-   Update or delete the robot credentials that are created by them.

</td><td>

Can't view, update, or delete the robot credentials of the bot process that they aren’t assigned to or robot credentials that aren’t created by them.

</td></tr><tr><td>

RPA robot user

</td><td>

View all robot credentials.

</td><td>

Can't create, update, and delete the robot credentials.

</td></tr><tr><td>

RPA support user

</td><td>

View the robot credentials that are mapped to the bot processes that they’re assigned to.

</td><td>

Can't create, update, or delete the robot credentials.

</td></tr></tbody>
</table>## Application credentials

By creating application credentials, you can add the user name and password that the robot can use to log in to a specific application at the time of the automation execution. For more information, see [Create an application credential in RPA Hub](../task/create-application-credential.md).

In the following table, learn what users with different roles can do or can't do.

<table id="table_rqt_yd4_1cc"><thead><tr><th>

Role

</th><th>

Can do

</th><th>

Can't do

</th></tr></thead><tbody><tr><td>

RPA release manager and RPA administrator

</td><td>

Create, view, update, or delete the application credentials.

</td><td>

-

</td></tr><tr><td>

RPA developer

</td><td>

-   Create or view the application credentials.
-   Update or delete the application credentials that are created by them.

</td><td>

Can't view the application credentials that aren’t created by them.

</td></tr><tr><td>

RPA business user

</td><td>

-   Create the application credentials.
-   View the application credentials that are created by them or the application credentials that are mapped to the bot processes that they’re assigned to.
-   Update or delete the application credentials that are created by them.

</td><td>

Can't add the external credentials.

</td></tr><tr><td>

RPA robot user

</td><td>

View or edit all the application credentials.

</td><td>

Can't create or delete the application credentials.

</td></tr><tr><td>

RPA support user

</td><td>

View the application credentials that are mapped to the bot processes that they’re assigned to.

</td><td>

Can't create, update, or delete the robot credentials.

</td></tr></tbody>
</table>## TOTP authentication

By setting up Time-based One-time Password \(TOTP\) seeds, you can enable the unattended robots to authenticate seamlessly against multi-factor authentication \(MFA\)-enabled applications. MFA-enabled applications provide additional security for users and their accounts.

You can't edit a TOTP authenticator record. If changes are required to an existing TOTP authenticator record, you must retire an existing record and then create a TOTP authenticator record. For more information, see [TOTP authentication in RPA Hub](totp-authentication-rpa.md) and [Create a TOTP authenticator in RPA Hub](../task/map-totp-credential-set-rpa.md).

In the following table, learn what users with different roles can do or can't do.

<table id="table_th2_3l4_1cc"><thead><tr><th>

Roles

</th><th>

Can do

</th><th>

Can't do

</th></tr></thead><tbody><tr><td>

RPA release manager and RPA administrator

</td><td>

Create, view, or delete the TOTP authenticators.

</td><td>

Can't update the TOTP authenticators.

</td></tr><tr><td>

RPA developer

</td><td>

-   Create the TOTP authenticators.
-   View the TOTP authenticators that are created by them or TOTP authenticators that are mapped to the bot processes that they’re assigned to.

</td><td>

Can't update or delete the TOTP authenticators.

</td></tr><tr><td>

RPA robot user

</td><td>

View all TOTP authenticators.

</td><td>

Can't create, update, or delete the TOTP authenticators.

</td></tr></tbody>
</table>## Credential groups

By configuring the credential groups, you can map the application credentials and a robot credential to one or more bot processes. For more information, see [Create a credential group in RPA Hub](../task/create-credential-group.md#).

In the following table, learn what users with different roles can do or can't do.

<table id="table_cvp_hm4_1cc"><thead><tr><th>

Roles

</th><th>

Can do

</th><th>

Can't do

</th></tr></thead><tbody><tr><td>

RPA release manager and RPA administrator

</td><td>

Create, view, update, or delete the credential groups.

</td><td>

-

</td></tr><tr><td>

RPA developer

</td><td>

-   Create the credential groups.
-   View the credential groups that are created by them or the credential groups that are mapped to the bot processes that they’re assigned to.
-   Update or delete the credential groups that are created by them.

</td><td>

Can't view, update, or delete the credential groups of the bot process that they aren’t assigned to or the credential groups that aren’t created by them.

</td></tr><tr><td>

RPA robot user

</td><td>

View all the credential groups.

</td><td>

Can't create, update, or delete the credential groups.

</td></tr><tr><td>

RPA support user

</td><td>

View the credential groups that are mapped to the bot processes that they’re assigned to.

</td><td>

Can't create, update, or delete the credential groups.

</td></tr></tbody>
</table>## External credential vault

By configuring an external credential vault, you can retrieve a robot credential, application credentials, or Time-based One-time Password \(TOTP\) seed from an external source instead of a ServiceNow credentials record. For more information, see [External credential vault in RPA Hub](external-credentials-rpa.md) and [Create an external credential vault record in RPA Hub](../task/create-ext-cred-rpa.md).

In the following table, learn what users with different roles can do or can't do.

|Roles|Can do|Can't do|
|-----|------|--------|
|RPA release manager and RPA administrator|Create, view, or update the external credentials.|Can't delete external credentials.|
|RPA developers|View the external credentials.|Can't create, update, or delete the external credentials.|
|RPA support user|View the external credentials.|Can't create, update, or delete the external credentials.|
|RPA business user|View the external credentials.|Can't create, update, or delete the external credentials.|

