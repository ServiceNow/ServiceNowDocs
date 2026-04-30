---
title: Configure MFA with Biometrics
description: Administrators can use the User Public Credentials list to view and manager user created credentials.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Web Authentication - MFA, Configuring MFA, supported methods, and workflow, Multi-factor authentication \(MFA\), Authentication, Access Management]
---

# Configure MFA with Biometrics

Administrators can use the User Public Credentials list to view and manager user created credentials.

When a user registers an authenticator application, biometric authentication, or hardware key, you instance creates a record on the **User Public Credentials**\[sys\_user\_public\_credential\] table. Use this table to see which users have registered an authenticator, as well as what types, and when they were registered and used. You can also mark these records as inactive to prevent the credentials to prevent users from using these credentials.

|Field|Description|
|-----|-----------|
|Credential Nickname|Nickname for the credential. This nickname is chosen by the user when they register an authenticator.|
|User|User associated with the credential|
|Active|Whether the credential is active. Administrators can set a record to inactive to prevent a user from authenticating with this credential.|
|Authenticator|The type of authenticator registered by the user.|
|Registration Time|The date and time the user-created this credential|
|Last Used Time|The last date and time the user logged in with this credential.|

## Restricted authenticator types

If you have restricted an authentication method, such as biometric authenticators, users will not be able to create new credentials of that type. However, any credentials created before you made this restriction will continue to work. You can disable records on the **User Public Credentials** table to prevent these credentials from being used after they have been created.

