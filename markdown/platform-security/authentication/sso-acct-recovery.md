---
title: Account recovery \(ACR\)
description: Administrators can configure account recovery \(ACR\) to perform recovery activities such as addressing SSO misconfiguration or expired certificates.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Multi-Provider SSO configurations, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Account recovery \(ACR\)

Administrators can configure account recovery \(ACR\) to perform recovery activities such as addressing SSO misconfiguration or expired certificates.

**Note:** Enabling ACR disables the local interactive log-ins \(username or password based\) when SSO is enabled to your instances.

ACR provides the following capabilities:

-   Bypass your single sign-on \(SSO\) login to address issues with SSO configuration as an administrator.
-   Log in with using SSO to perform tasks with an administrator account configured as an account recovery.
-   ACR flows enable the administrators to use self-service capabilities to address account recovery when there’s a need for recovery, for example, SSO miss-configuration, expired certificates.
-   Reduce unauthorized access to the instance and provide a strong foundation to use ACR outside SSO use cases.

## Fresh Instance

For a fresh instance to use ACR, you must do the following:

-   Activate Mutli-SSO plugin \(`com.snc.integration.sso.multi.installer`\)
-   Enable ACR \(`glide.sso.acr.enabled`\) - This is enabled by default in case of a fresh instance.
-   Before enabling SSO property \(`glide.authenticate.multisso.enabled`\), the administrator must enroll as an ACR user.

    **Note:** Setting this property to false will not disable multi-provider SSO if Account Recovery \(ACR\) is also enabled on the instance. To log in with a username and password ACR must also be disabled using the **glide.sso.acr.enabled** property. For details on this property see [Account recovery properties](../reference/acr-properties.md).

-   Administrator must set a password for local login and register MFA before enrolling as an ACR user.

## Upgraded Instance

For an upgraded instance to use ACR, you must do the following:

-   Activate Mutli-SSO plugin \(`com.snc.integration.sso.multi.installer`\)
-   Enable ACR \(`glide.sso.acr.enabled`\)

    **Note:** In case of upgraded instance, the administrator must enable ACR.

-   Before enabling SSO property \(`glide.authenticate.multisso.enabled`\), the administrator must enroll as an ACR user.
-   Administrator must set a password for local login and register MFA before enrolling as an ACR user.

## Configure account recovery users

To use account recovery, you must register at least one admin account as an account recovery user. Single sign-on can’t be activated on your instance until there is at least one account configured. For details on this process, see [Configure an account recovery user from the Account Recovery Properties page](config-acr.md#).

**Note:** If you’re upgrading an instance already using single sign-on to Rome or a later release, single-sign on will continue to function without a recovery user configured.

## Account recovery configuration

The account recovery feature is included with the **Integration - Multiple Provider Single Sign-On Installer \(com.snc.integration.sso.multi.installer\) plugins**. The feature is enabled by default. You can change this and other account recovery settings using system properties. For details on these properties, see [Account recovery properties](../reference/acr-properties.md).

## Account recovery policy context

After you’ve registered an account recovery user and enabled single sign-on \(SSO\), your instance restricts all local logins. This restriction is defined in the **SSO - ACR Context** auth policy context. For more information about the context, see [Account recovery context](account-recovery-context.md).

For details on how authentication policies and policy contexts, and how they work on your instance, see [Adaptive authentication](../../authentication/concept/adaptive-authentication.md).

