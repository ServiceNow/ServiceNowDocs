---
title: MID Server IPKI authentication
description: Instance PKI \(IPKI\) lets a MID Server authenticate to its instance using a JSON Web Token \(JWT\) signed by an instance-issued certificate. Use IPKI when you want to authenticate MID Servers with certificates that the instance issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/mid-server/mid-server-ipki-authentication.html
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-10-29"
reading_time_minutes: 7
keywords: [iPKI, MID Server authentication, DefaultSecurityKeyPairHandle]
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server IPKI authentication

Instance PKI \(IPKI\) lets a MID Server authenticate to its instance using a JSON Web Token \(JWT\) signed by an instance-issued certificate. Use IPKI when you want to authenticate MID Servers with certificates that the instance issues.

## How IPKI authentication works

The MID Server creates a JWT and signs it with the private key associated with its certificate. It then sends that JWT as a bearer token in the Authorization header of an HTTPS request. The certificate's role is to back the JWT's signature and identify the MID Server.

When the instance receives a request, it reads the JWT as a bearer token. It resolves the acting user from the token's `sub` claim rather than from the certificate. It then evaluates an IPKI authorization policy for that user through the sn\_ipki\_auth policy API. A DBListener tracks certificate activation and revocation continuously, so a revoked MID Server is rejected even if its signature is still valid.

## Certificate rotation

The MID Server rotates its IPKI certificate automatically, starting 15 days before the certificate expires. After it receives the new certificate, the MID Server restarts.

## Force rotation

By default, MID Servers that use IPKI rotate certificates automatically within the rotation window. To rotate a certificate early, use the force rotation feature in the MID Admin workspace.

## Known limitations

If the IPKI certificate expires, the MID Server can't authenticate to the instance. As a result, it can't rotate the certificate automatically. To restore authentication, fix the certificate or reregister the MID Server. For the steps, see [Reregister MID Servers to restore IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-reregister-ipki-authentication.md).

If automatic rotation fails, the MID Server raises the `Mid-CertificateRotationRequired` issue when the certificate has 7 days or less before it expires. Before the certificate expires, force a rotation or reregister the MID Server. For the messages that the MID Server logs, see [MID Server IPKI reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-ipki-reference.md).

## Next steps

To compare IPKI with basic authentication and mTLS, see [MID Server authentication methods comparison](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-authentication-comparison.md). To provision a new MID Server with IPKI, see [Set up a MID Server to use IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-set-up-ipki-authentication.md). To move an existing MID Server from basic authentication, see [Migrate MID Servers to IPKI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-migrate-basic-to-ipki.md). To restore authentication for a MID Server whose certificate has expired or been revoked, see [Reregister MID Servers to restore IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-reregister-ipki-authentication.md). To move a MID Server back to basic authentication, see [Revert MID Servers from IPKI to basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-revert-ipki-to-basic-authentication.md).

-   **[Set up a MID Server to use IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-set-up-ipki-authentication.md)**  
Set up a new MID Server to authenticate to your instance with instance PKI \(IPKI\), where the instance issues the certificate that the MID Server uses. Use this procedure for a new MID Server.
-   **[Reregister MID Servers to restore IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-reregister-ipki-authentication.md)**  
Generate a registration key and use it to get a new IPKI certificate for an existing MID Server.
-   **[Migrate MID Servers to IPKI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-migrate-basic-to-ipki.md)**  
Move an existing MID Server that uses basic authentication to ServiceNow certificate-based IPKI authentication. Migrating a MID Server to IPKI preserves the user previously set on that MID Server.
-   **[Revert MID Servers from IPKI to basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-revert-ipki-to-basic-authentication.md)**  
Move a MID Server that uses IPKI authentication back to basic authentication by changing its configuration and restarting the service.
-   **[MID Server IPKI reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-ipki-reference.md)**  
Learn about configuration parameters, keystore aliases, instance-side tables, and log messages for MID Server IPKI authentication.

**Parent Topic:**[Securing and encrypting MID Server data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies]()

[Encrypt or decrypt MID Server configuration file values]()

[MID Server configuration file security]()

[MID Server authentication methods comparison]()

[MID Server authentication credentials and SOAP requests]()

[MID Server unified key store]()

[Enable MID Server mutual authentication]()

[MID Server Azure Key Vault integration]()

[MID Server command audit log]()

[Rekey a MID Server]()

[Add SSL certificates for the MID Server]()

[MID Server SSH cryptographic algorithms]()

[Attach a script file to a file synchronized MID Server]()

[MID Server FIPS Enforced Mode]()

[MID Server Governance]()

