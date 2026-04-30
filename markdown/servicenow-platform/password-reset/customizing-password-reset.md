---
title: Customizing Password Reset processes
description: Password Reset scripts enable you to customize Password Reset by creating your own credential store, verification, and identification types, and extend them by defining extension scripts. You can also create a custom credential store type, custom verification type, or verification.
locale: en-US
release: xanadu
product: Password Reset
classification: password-reset
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configure, Password Reset, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Customizing Password Reset processes

Password Reset scripts enable you to customize Password Reset by creating your own credential store, verification, and identification types, and extend them by defining extension scripts. You can also create a custom credential store type, custom verification type, or verification.

## Legacy

Password Reset scripting is available to users with the password\_reset\_admin role. The easiest way to customize Password Reset is:

1.  Create custom types and scripts as described in [Password Reset extension script categories](pw-reset-extension-script.md).

    Extension scripts are example script includes that enable you to extend functionality in a password reset process. The [extension script category](pw-reset-extension-script.md) refers to the specific types of behavior for an extension script \(for example, credential store, verification, identification type, or as a post-processor\).

2.  Follow the configuration steps described in [Configure your Password Reset process](../task/t_CreateAPasswordResetProcess.md).
3.  Select the new types that you created. You can customize the following components:
    -   Credential store types: Define new types for how to connect to your credential stores by creating custom workflows for connection and testing. See [Create a credential store type for Password Reset](../task/t_CreateACredentialStoreType.md).
    -   Verification types: Define new types for how users are verified. See [Create a custom Password Reset verification type](../task/create-verification-type.md).
    -   Identification types: Define new types for how users can identify themselves. See [Create a custom identification type for Password Reset](../task/t_CreateAnIdentificationType.md).

## Advanced password reset configuration

You can customize the Password Reset and Password Change applications to meet your organization's needs. See [Password Reset and Password Change applications](password-reset-admin-guide.md) for more information. Also see [Configuring Password Reset properties](../task/t_SetPwdResetProps.md) for a list of properties that control several aspects of password reset.

-   **[Customize password reset processes and integrate third-party credential services](../task/setup-pwd-reset-ihub.md)**  
To customize password reset processes or to integrate them with third-party credential services such as Okta or Microsoft Entra ID, use Integration Hub capabilities. Use Workflow Studio to create or modify actions like user unlock, change password, and get user status. Use Workflow Studio to create or modify subflows that perform the actions.
-   **[Add a custom question to the Security Questions verification](../task/t_CreateQAVerificationQs.md)**  
To enroll for the 'Security Questions' verification, the user selects several questions and supplies confidential answers that only the user knows. You can add a custom question to the set of questions that are included with the base system.
-   **[Add a custom header or footer to the user pages for Password Reset](../task/customize-user-reset-pages.md)**  
 You can specify UI macros that add a header or footer to the pages that end users work in while resetting a password \(the Identify, Verify, and Reset pages\).
-   **[Create a Password Reset verification from an existing verification](../task/t_CreatePWRVerFromBaseVer.md)**  
The Password Reset application includes several example verifications that you can use as they are or as the basis for a custom verification. If the verification types in the base system do not meet your needs, you can create a custom verification type.
-   **[Create a custom Password Reset verification type](../task/create-verification-type.md)**  
Each verification in Password Reset is based on the settings for a verification type. If the verification types in the base system do not meet your needs, you can create a custom verification type.
-   **[Create a custom Password Reset verification](../task/t_CreatePWRVerFromVerType.md)**  
Use a verification type in the base system as a template to design a custom verification. The Password Reset Windows Application does not support custom verifications.
-   **[Create a custom identification type for Password Reset](../task/t_CreateAnIdentificationType.md)**  
A custom identification type enables the user to enter alternative verification information such as an employee ID while resetting the password.
-   **[Configure a credential store type to support third-party password auto-generation](../task/rpa-configure-credential-store-type-support.md)**  
Enable the subflows in credential store type to support third-party password auto-generation.
-   **[Asynchronous password reset subflow](../task/async-password-reset-subflow.md)**  
When a user requests a password reset, based on the application for which the password reset is requested, the process works either synchronously or asynchronously.
-   **[Create a credential store type for Password Reset](../task/t_CreateACredentialStoreType.md)**  
Create a custom credential store type when the base-system types do not meet your needs.

**Parent Topic:**[Configuring Password Reset](password-reset-admin-guide.md)

