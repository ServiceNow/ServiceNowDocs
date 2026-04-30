---
title: Customize password reset processes and integrate third-party credential services
description: To customize password reset processes or to integrate them with third-party credential services such as Okta or Microsoft Entra ID, use Integration Hub capabilities. Use Workflow Studio to create or modify actions like user unlock, change password, and get user status. Use Workflow Studio to create or modify subflows that perform the actions.
locale: en-US
release: yokohama
product: Password Reset
classification: password-reset
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Customizing Password Reset processes, Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Customize password reset processes and integrate third-party credential services

To customize password reset processes or to integrate them with third-party credential services such as Okta or Microsoft Entra ID, use Integration Hub capabilities. Use Workflow Studio to create or modify actions like user unlock, change password, and get user status. Use Workflow Studio to create or modify subflows that perform the actions.

## Before you begin

Role required: admin, password\_reset\_admin, or password\_reset\_credential\_manager

## About this task

-   The base system provides actions, subflows, and credential store types for the "Local ServiceNow Instance" identity provider.
-   For Microsoft Active Directory, the subflows are available when you activate the Microsoft AD Spoke for Password Reset app.
-   To use any other identity provider such as Okta, you must use Integration Hub to create the required actions, subflows, and custom credential store types.
-   For Microsoft Entra ID, the subflows are available when you activate the Microsoft Entra ID Integration for Password Reset app.

## Procedure

1.  Use Workflow Studio to create password reset actions like user unlock, change password, and get user status.

    For more information about Workflow Studio, see [Action Designer](https://www.servicenow.com/docs/access?context=actions&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

2.  Use Workflow Studio to create the following subflows.

    Use the specified names, inputs, and outputs for the subflows. For more information about the subflows, see [Subflows](https://www.servicenow.com/docs/access?context=subflows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

<table id="table_en2_pll_b3b"><thead><tr><th>

Subflow name

</th><th>

Input

</th><th>

Input type

</th><th>

Output

</th><th>

Output type

</th></tr></thead><tbody><tr><td rowspan="2">

&lt;Provider Name&gt; Password Unlock

</td><td rowspan="2">

Password Reset Request

</td><td rowspan="2">

Record.Password Reset Request

</td><td>

Error Message

</td><td>

String

</td></tr><tr><td>

Status

</td><td>

Choice

</td></tr><tr><td rowspan="2">

&lt;Provider Name&gt; Password Reset

</td><td>

Password

</td><td>

Password \(2 Way Encrypted\)

</td><td>

Status

</td><td>

Choice

</td></tr><tr><td>

Password Reset Request

</td><td>

Record.Password Reset Request

</td><td>

Error Message

</td><td>

String

</td></tr><tr><td rowspan="3">

&lt;Provider Name&gt; Password Change

</td><td>

Password Reset Request

</td><td>

Record.Password Reset Request

</td><td>

Status

</td><td>

Choice

</td></tr><tr><td>

Current Password

</td><td>

Password \(2 Way Encrypted\)**Note:** **Name** under **Advanced options** is `old_password`.

</td><td rowspan="2">

Error Message

</td><td rowspan="2">

String

</td></tr><tr><td>

New Password

</td><td>

Password \(2 Way Encrypted\)**Note:** **Name** under **Advanced options** is `new_password`.

</td></tr><tr><td rowspan="3">

&lt;Provider Name&gt; Password Lock State

</td><td rowspan="3">

Password Reset Request

</td><td rowspan="3">

Record.Password Reset Request

</td><td>

Error Message

</td><td>

String

</td></tr><tr><td>

Locked

</td><td>

Choice

</td></tr><tr><td>

Status

</td><td>

Choice

</td></tr><tr><td rowspan="2">

&lt;Provider Name&gt; Password Connection Test

</td><td rowspan="2">

Not Applicable

</td><td rowspan="2">

Not Applicable

</td><td>

Error Message

</td><td>

String

</td></tr><tr><td>

Status

</td><td>

Choice

</td></tr></tbody>
</table>3.  For third party providers, [create a credential store type](t_CreateACredentialStoreType.md).

    1.  Select the **Use Flow** check box.

    2.  Select the password reset subflows that you created for the provider.

    See [Password Reset application](../reference/password-reset-landing-page.md) for more information.

4.  [Create password reset credential store](../concept/c_CredentialStores.md).

5.  [Create a password reset process](t_CreateAPasswordResetProcess.md).

6.  Select the credential store type created for the provider.


## Result

The password reset mechanism for the required third-party application is set up.

**Parent Topic:**[Customizing Password Reset processes](../concept/customizing-password-reset.md)

