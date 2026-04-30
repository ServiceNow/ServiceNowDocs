---
title: Adaptive authentication
description: Use the Adaptive authentication policy framework to enforce contextual authentication controls to the right users at the right time. Adaptive authentication uses authentication policies to evaluate authentication requests and then either deny or allow access to your instance based on the specified policy conditions.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Authentication, Access Management]
---

# Adaptive authentication

Use the Adaptive authentication policy framework to enforce contextual authentication controls to the right users at the right time. Adaptive authentication uses authentication policies to evaluate authentication requests and then either deny or allow access to your instance based on the specified policy conditions.

Use adaptive authentication policies and contexts to restrict the access to your instance for users and APIs based on criteria like IP address, user role, and user group. You can configure the built-in authentication policies according to your security requirements.

For example, an administrator can configure the **Allow Access Policy** to allow logins from users only within a trusted range of IP addresses and who are members of a specific role. When assigned to the **Post-authentication context**, the access policy denies access from untrusted IP addresses.

To set a custom message in the language of your instance you need to add key, value pair in `sys_ui_message.list` and update the `sys_ui_message` record. When you login with an incorrect password, the custom message in the preferred language is displayed.

![Adaptive authentication flow](../images/adaptive-auth-graphic.png)

## Adaptive authentication components

-   **Authentication policies**

    Authentication policies evaluate authentication requests based on the specified policy conditions and either allow or deny access depending on the output of policy conditions evaluation. For example, access is allowed only if all the policy conditions specified in **Allow Access Policy** evaluate to true.

    Authentication policies use information provided by filter criteria to compare against the policy's conditions to determine whether to grant access to the instance. For example, a filter criteria provides a user's IP address, and a policy condition determines whether this address is within the specific range before granting access. Learn more about authentication policies in [Authentication policies](authentication-policies.md).

-   **Authentication policy contexts**

    Authentication policy contexts define how and when policies are enforced during the login process. The pre-authentication context executes before the user is shown a login screen. The post-authentication context executes after the user enters their credentials. To use a policy, it must be assigned to a policy context. For details on these contexts, see [Authentication policy contexts](auth-policy-contexts.md).

-   **Filter Criteria**

    Filter criteria \(also called policy inputs\) are used as inputs for policy conditions. Policy conditions use these inputs to verify and meet the requirements of authentication requests. These inputs provide information like user role, IP range, and identity provider. For more detail on filter criteria, see [Filter criteria](adaptive-auth-filter-criteria.md).

-   **Authentication properties**

    Use authentication properties to control whether adaptive authentication is active on your instance. You can also use properties to enabled debugging, and define the messaging users see when access is blocked. For details on these properties, see [Configure adaptive authentication properties](../task/configure-adaptive-auth-properties.md).


## REST API access policies

You can use the filter criteria of adaptive authentication framework to restrict access to inbound ServiceNow REST APIs. For more information, see [REST API access policies](inbound-authentication-profile.md).

## Domain separation and adaptive authentication

Adaptive authentication is supported on domain separated instances on the authentication policy condition level. Policy conditions affect the domain in the records **Domain** \[sys\_domain\] field. Policy conditions in the global domain affect all domains.

## Adaptive Authentication Events

You can use the adaptive authentication events table to know about the events that have occurred specific to the adaptive authentication feature. For more information, see [Adaptive Authentication Events](adaptive-authentication-events.md).

