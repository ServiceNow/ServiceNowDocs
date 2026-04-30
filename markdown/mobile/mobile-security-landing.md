---
title: Mobile security
description: Learn about the security features of the ServiceNow mobile platform.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Mobile security

Learn about the security features of the ServiceNow mobile platform.

## ServiceNow mobile architecture

ServiceNow mobile apps consist of ServiceNow server instance and native apps for iOS and Android. The apps use full native code and are not a hybrid approach. The mobile apps transmit and receive data with the server across the wireless network.

![Diagram of ServiceNow mobile architecture.](../image/security-mobile-architecture-1.png "ServiceNow mobile architecture")

## Overview of key features of ServiceNow mobile platform security

-   The mobile apps rely on the secure ServiceNow platform and its APIs to provide a seamless mobile experience to its users.
-   App/server interactions are protected through OAuth authorization framework.
-   Most of the user interface on the ServiceNow app is driven through meta data delivered by the ServiceNow platform.
-   The ServiceNow mobile apps fetch all their data from the ServiceNow platform and store it in a local cache on the app client layer.
-   Data that is transferred to and from ServiceNow instances and data that is stored locally is encrypted.
    -   For iOS apps, ServiceNow uses the OS level FIPS 140-2 validated disk encryption on Core Data, by forcing a device level PIN or Biometrics security. iOS keeps up to date on FIPS-compliant cipher suites with operating system updates.
    -   For Android apps, ServiceNow uses the SQLCipher SDK. This SDK provides encryption using FIPS 140-2 validated crypto module for all the app data stored in Room DB.

        In client version 20.1.0 of Android apps, the TLS\_ECDHE\_RSA\_WITH\_AES\_256\_GCM\_SHA384 cipher suite has been added and support for the below CBC ciphers has been discontinued:

        -   TLS\_ECDHE\_ECDSA\_WITH\_AES\_128\_CBC\_SHA
        -   TLS\_ECDHE\_ECDSA\_WITH\_AES\_128\_CBC\_SHA256
        -   TLS\_ECDHE\_RSA\_WITH\_AES\_128\_CBC\_SHA256
        In case of any SSL handshake issues due to cipher mismatch, review the supported ciphers on your instance and add one more supported cipher.

        Below is the list of supported ciphers on Android:

        -   TLS\_ECDHE\_ECDSA\_WITH\_AES\_256\_GCM\_SHA384
        -   TLS\_ECDHE\_ECDSA\_WITH\_AES\_128\_GCM\_SHA256
        -   TLS\_ECDHE\_RSA\_WITH\_AES\_128\_GCM\_SHA256
        -   TLS\_ECDHE\_RSA\_WITH\_AES\_256\_GCM\_SHA384

## App flow overview

ServiceNow mobile apps start fetching the initial user experience after a successful sign-in. The mobile app fetches the metadata to render the landing home screen from the instance. The app then uses this metadata to render the home screen.

![App flow overview.](../image/security-mobile-architecture-2.png)

## Data retrieval

-   **Read data**

    When a user requests to view information on the mobile app, the following steps occur.

    1.  The mobile app sends a request to access data from the instance. The request includes the token and any relevant data field needed for the request.
    2.  The instance receives the request and checks if the token is valid.
    3.  If the token is valid, the instance directs the request to the relevant API to fetch the information.
    4.  The instance returns the information to the mobile app.
-   **Downloading documents**

    When a user requests to download documents from the app, the following steps occur.

    1.  The mobile app sends a request to access the document. The request includes the token.
    2.  The instance receives the request and checks if the token is valid
    3.  The instance checks the access control list \(ACL\) rules.
    4.  If valid, the document is available to view.
-   **Write-backs for updating fields**

    When a user updates a field in the mobile app, the following steps occur.

    1.  The mobile app sends the token and the action metadata to the instance. For example, the ID, or the field to update.
    2.  The instance directs the action based on the relevant API.
    3.  The instance completes the action and sends a response to the mobile app.
    4.  Based on the response, the mobile app reflects the field changes and action availability in the UI.
-   **Write-backs for attaching files**

    When attaching files, the following steps occur.

    1.  The mobile app prompts the user to attach a file, for example, an image.
    2.  The mobile app sends the file and token to the instance.
    3.  The instance places the file based on the relevant API.
    4.  The instance sends a response back to the mobile app.

## Mobile authentication

ServiceNow mobile apps support platform authentication using OAuth 2.0. Authentication mechanisms include multi provider SSO, MFA, LDAP, Local DB, and Digest. ServiceNow mobile apps use an authentication methodology called AppAuth. AppAuth uses an external mobile browser to log the user in.

-   **Authentication flow**

    When a user signs in to an app on their mobile device, the app uses the user's credentials to negotiate an OAuth Token with the instance. The iOS Keychain stores the token for iOS devices. Android device use KeyStore. The keychain encryption is AES 256 in Galois/Counter Mode \(GCM\).

    At first login, the instance gives the user an access token and a refresh token. These tokens are valid for an amount of time that can be configured on your instance. When a user opens the mobile app, the client checks to see if the access token is valid. If valid, the user can continue with the session. If not valid, the client then checks if the refresh token is valid. If valid, the refresh token is used to fetch a new valid access token for the user, and the session can continue. If the refresh token is not valid, the user must reauthenticate.

-   **Access and refresh tokens**
    -   The mobile apps never stores the user password.
    -   The mobile apps do store the client ID, which is necessary for getting the OAuth token as part of the authentication flow.
-   **User termination**

    When an administrator deletes or removes a user from the instance, the access token is no longer valid, and any operation logs the user out.

    ![Mobile authentication workflow.](../image/security-mobile-architecture-3.png "Mobile authentication workflow")

-   **Multi-provider SSO**

    The multi-providers SSO plugin \[com.snc.integration.sso.multi.installer\] provides SAML authentication support. The login process \(AppAuth\) uses this plugin to redirect the user to the IDP \(SAML provider\) login page when using SAML.

-   **Multifactor authentication**

    Users can access the instance via Multifactor Authentication using the MFA plugin \[com.snc.integration.multifactor.authentication\]. The mobile app directs users to their login page after selecting their instance in the mobile app.

-   **LDAP**

    Use LDAP authentication to access using LDAP credentials. The user sees the same login page as the local login \(DB based\), but the back end to the LDAP server deletes the authentication.


## Data security

ServiceNow mobile apps use SSL/TLS over-the-air \(OTA\) communication encryption for data security. The OAuth authorization endpoints are HTTPS.

-   **Data at rest**

    Application preference data such as favorites, home screen, and the mobile navigator items are stored and cached locally on the device. The mobile apps do not store record data such as incidents and problems on the device unless your organization has specifically enabled offline syncing for field service. Record data stored during offline mode is encrypted with FIPS 140-2 validated modules. \(iOS cryptographic modules and SQL Cipher for Android which uses this cryptographic module for encryption\).

    ![Data at rest.](../image/security-mobile-architecture-4.png "Data at rest")

-   **Data in motion**

    Data in motion is over a secure SSL/TLS channel and encrypted with FIPS 140-2 validated modules.

-   **Data loss prevention**

    ServiceNow provides data loss prevention features without the need for the device and application be managed by an enterprise mobility management \(EMM\) suite. These features includes restrict copy/paste, enforce PIN, block attachment, and/or blur functionality.

-   **Restrict copy/paste**

    Copy/paste restrictions are defined by a property in the system properties table.

    |System property field|Value|
    |---------------------|-----|
    |Name|glide.sg.clear\_pasteboard\_when\_background|
    |Type|true \| false|
    |Value|true|

-   **Require an app PIN**

    Require users to enter a six-digit PIN each time they sign in from their mobile device, or when the application has been inactive for five minutes. Requiring an app PIN is controlled a property in the system properties table.

    |System property field|Value|
    |---------------------|-----|
    |Name|glide.sg.require\_mobile\_application\_pin|
    |Type|true \| false|
    |Value|true|

-   **Disabling attachments on a mobile device**

    You can configure ACL rule to block attachments specifically on mobile devices. Use the `isMobile` method to check if a request comes from a mobile device. For example, you could add an ACL rule for the attachment \[sys\_attachment\] table where the read and write scripted ACLs includes the following check.

    ```
    if( gs.isMobile() ){
         answer = false;
    }
    
    ```

    You can also add this code to any existing ACL rules you have for the attachment table. If you have multiple attachment ACL rules, all will need to have the **Admin override** option unchecked.

-   **Enable the blur app option**

    Blur the mobile app when not in focus on a mobile device using the following system property in the system properties table.

    |System property field|Value|
    |---------------------|-----|
    |Name|glide.sg.blur\_ui\_when\_backgrounded|
    |Type|true \| false|
    |Value|true|

    **Important:**

    -   The **glide.sg.blur\_ui\_when\_backgrounded** system property is supported on both iOS and Android devices.
    -   By default, the value for this property is set to `false`, which turns it off.
    -   For Android devices, when this property is enabled by setting the value to `true`, the following restrictions apply:

        -   The screen share feature isn't supported and the shared app screen appears black.
        -   Users are prevented from taking screenshots.
        These restrictions don't apply to iOS devices when the **glide.sg.blur\_ui\_when\_backgrounded** property is enabled.

-   **Penetration testing**

    ServiceNow engages a third party to perform penetration testing of the mobile app. This typically happens annually but sometimes occurs more frequently. The results of these tests are available to customers. For more detail on security testing, see [KB0538598: Customer Instance Security Testing \| Policy and Procedure](https://support.servicenow.com/kb_view.do?sysparm_article=KB0538598).

-   **Security patching**

    In the event a security patch is needed, the mobile development team aligns with standard SDLC properties in order to patch.

-   **User data collection**

    The mobile app does not specifically collect any user data.

    User transactions or usage within the app is tracked on the ServiceNow instance just as it is on the web. For user credentials, after a user logs in, the mobile app negotiates an OAuth Token that is stored in the Apple Keychain or the Android Keystore. User credentials are never saved. If the user opts in, the following information is collected:

    -   Location
    -   Access to camera
    -   Notifications

