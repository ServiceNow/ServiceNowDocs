---
title: Authentication policy contexts
description: Use authentication policy contexts to determine how and when your instance enforces authentication policies.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Adaptive authentication, Authentication, Access Management]
---

# Authentication policy contexts

Use authentication policy contexts to determine how and when your instance enforces authentication policies.

Authentication contexts define how and when a policy is enforced during the login process. Assign a policy to a policy context to define inputs and conditions regarding how your instance handles authentication.

## Pre-authentication context

Policies in the pre-authorization context execute when a user first accesses the instance, before the they see a login screen. You can use the pre-authorization context to allow or deny access before your users are prompted for login credentials based on your selected policy. Because these policies evaluate before a user enters any information, those policies cannot take criteria such as a user's roles or groups into account.

For more detail on this context, see [Pre authentication context](pre-auth-context.md).

## Post-authentication context

Policies in the post-authorization context execute after your users enter their credentials or SSO response. Your instance allows or denies access based on your selected policy. Because your users have identified themselves via their login credentials, the policy can use user information to determine whether to grant access.

For more detail on this context, see [Post-authentication context](post-auth-context.md).

## MFA \(Multi-Factor Authentication\) context

Policies assigned to the MFA context define whether to enforce MFA during the login process. Whether your instance enforces MFA is determined by the configuration of policies in this context. For more detail on this context, see [Multi-factor Authentication context](mfa-auth-context.md).

## Account recovery context

Administrators can configure account recovery \(ACR\) to perform recovery activities such as addressing SSO misconfiguration or expired certificates. To use account recovery, you must register at least one admin account as an account recovery user. Single sign-on can’t be activated on your instance until there is at least one account configured. For more information about the context that can be set, see [Account recovery context](../../single-sign-on/concept/account-recovery-context.md).

## Session Validation context

The Session Validation context can be used with the Adaptive authentication policy framework. The framework uses authentication policies to evaluate authentication requests \(session\) and then either deny or allow access based on policy conditions. For more information, see [Session validation context](session-context.md).

## Default policy

Within the policy context, you can define a default policy in the **Default Policy** field. This default defines how your instance responds to the result of your policy. The available default policy options are determined by which context you are using. Detail on these options can be found in the docs describing these individual contexts.

