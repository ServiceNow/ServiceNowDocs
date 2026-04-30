---
title: External credential storage
description: An instance can store credentials used by Discovery, Orchestration, and Service Mapping in an external credential repository rather than directly in a ServiceNow credentials record.
locale: en-US
release: zurich
product: Connections and Credentials
classification: connections-and-credentials
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Get started with credentials, Connections and Credentials, Access Management]
---

# External credential storage

An instance can store credentials used by Discovery, Orchestration, and Service Mapping in an external credential repository rather than directly in a ServiceNow credentials record.

The instance maintains a unique identifier for each credential, the credential type \(such as SSH, SNMP, or Windows\), and any credential affinities. The MID Server obtains the credential identifier from the instance, and then uses a customer-provided JAR file to resolve the identifier from the repository into a usable credential. Currently, the ServiceNow® platform supports the use of the [CyberArk vault](c_CyberArkCredStorageIntegrate.md) or BeyondTrust for external credential storage.

## External credential storage architecture

![ServiceNow external credential storage architecture](../image/ExternalCredentialStorageArchitecture.png "External credential storage architecture")

## Credential process flow

The MID Server retrieves credentials from an external store using this process:

1.  MID Server downloads credential objects from the ServiceNow Credentials \[discovery\_credentials\] table that contain the corresponding credential ID from the target vault.
2.  As each probe or pattern runs from Discovery or Orchestration jobs, the MID Server requests the credential by passing information such as credential ID, target IP address, and credential type to the Credential Resolver Java Jar file. The details about the correct credential object to retrieve from the vault are determined by the Credential Resolver.

    Many Credential Resolvers such CyberArk call an application supplied by the third-party vault vendor running on same machine as the MID Server. That application can often be configured to cache credentials and knows to update the cache when a credential changes in the vault, which is very important to avoid unnecessary network calls to the vault each time MID Server requests a credential. The Credential Resolver \(using optional vendor application if present\) makes a call to the vault to get the actual user name, password, etc.

    For Credential Resolvers supplied out-of-box \(only CyberArk today\), the MID Server only caches a credential for up to several seconds using encryption in MID Server process memory. This means the MID Server can make multiple requests to the Credential Resolver for the same credential even when discovering a single device. Contact third party vendors for information about caching implementations for other Credential Resolvers.

3.  MID Server executes the probe with the appropriate credential.

**Note:** Credential affinity still applies. The mechanism remains the same, since the only real difference from the MID Server's perspective is that the real credential details \(user name and password\) come from the third party vault.

## External credential storage logging

The MID Server posts log messages about external credential storage.

If the repository encounters an error while attempting to resolve a credentials request, the MID Server posts log messages with this prefix: `Problem with client's CredentialResolver:`

## Components installed with External Credential Storage

-   **Business rule**

    The External Credential Storage business rule performs the following tasks when an administrator makes any change to the Enable External Credential Storage property:

    -   Changes the view for the Credentials record list and form to the External Storage view. This view enables users to see the **Credential ID** column in the list.
    -   Instructs the MID Server to refresh its credentials cache in preparation for a change in the way credentials are obtained.
-   **Property**

    A property called Enable External Credential Storage \[com.snc.use\_external\_credentials\] enables or disables the External Credential Storage plugin after it’s activated. The property is located in **Discovery Definition** &gt; **Properties** and **Orchestration** &gt; **MID Server Properties**, and is enabled when you activate the plugin.

    If you disable external credential storage with the system property, the system automatically sets all the external credentials to inactive in the instance. If you re-enable the feature with this property, the system doesn’t reset the external credential records to active. You must reactivate each [credential record](../reference/r_WindowsCredentialsForm.md#) manually.


-   **[Request external credential storage for Discovery and Orchestration](../task/t_ActivateExtrnlCredStoragePlugIn.md)**  
The External Credential Storage plugin is available by request.
-   **[External credential storage configuration](external_cred_storage_configuration.md#)**  
Configure your instance to obtain credentials from a remote repository.
-   **[CyberArk credential storage integration](c_CyberArkCredStorageIntegrate.md)**  
The MID Server integration with the CyberArk vault enables ServiceNow® Orchestration, ServiceNow® Discovery, and ServiceNow® Service Mapping to run without storing any credentials on the instance.
-   **[OAuth 2.0 authentication via MID Server using external credential storage](oauth-2-0-support-in-external-credential.md)**  
Store OAuth 2.0 credentials-client ID and client secret-in the CyberArk vault instead of the ServiceNow instance. The MID Server gets the credentials from the CyberArk vault, when required to get the OAuth token. The token is stored in the MID Server and refreshed automatically upon expiry.

**Parent Topic:**[Get started with credentials](../reference/credentials-getting-started.md)

