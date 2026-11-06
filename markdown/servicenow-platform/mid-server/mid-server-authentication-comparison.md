---
title: MID Server authentication methods comparison
description: The MID Server can authenticate to your instance using basic authentication, mTLS, or IPKI methods. The methods differ in what the MID Server presents, who issues and manages the certificate, and how access is revoked.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/mid-server/mid-server-authentication-comparison.html
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-10-29"
reading_time_minutes: 7
keywords: [MID Server authentication, basic authentication, mTLS, mutual authentication, IPKI]
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server authentication methods comparison

The MID Server can authenticate to your instance using basic authentication, mTLS, or IPKI methods. The methods differ in what the MID Server presents, who issues and manages the certificate, and how access is revoked.

A MID Server can authenticate to its instance in one of three ways. All three identify the MID Server to the instance. They differ in the credential the MID Server presents and in who issues and manages it.

-   Basic authentication: the MID Server sends a user name and password.
-   mTLS \(mutual authentication\): the MID Server presents a client certificate that you obtain from your own certificate authority \(CA\). The instance and the MID Server authenticate each other during the TLS handshake.
-   IPKI \(instance PKI\): the instance issues a certificate to the MID Server. The MID Server uses that certificate's private key to sign a JSON Web Token \(JWT\) that it sends with each request.

IPKI authenticates the MID Server to the instance. It doesn't change the service account that runs the MID Server process, and it doesn't affect Active Directory or LDAP accounts.

## Differences at a glance

|Characteristic|Basic authentication|mTLS|IPKI|
|--------------|--------------------|----|----|
|Requirements and limits|No certificates to manage.|The instance must use ADCv2 load balancers. A MID Server that uses mutual authentication can't be re-keyed or validated from the instance UI.|Certificates must be valid. An IPKI enabled MID Server with an expired or invalid certificate fails to authenticate until you fix the certificate or reregister the MID Server.|
|Who issues the credential|You create the user and set the password.|Your certificate authority. Commercially signed certificates and certificates signed by a private CA are supported. Self-signed certificates aren't supported.|Your instance.|
|MID Server user account|You create a user for the MID Server and set its password.|The MID Server needs a user with the mid\_server role on the instance. You must map the client certificate to that user on the instance.|The MID Server needs a user with the mid\_server role on the instance. When you create a registration key, you map it to a user, and the MID Server logs in as that user. A migrated MID Server keeps its existing user.|
|How you set it up|Set the user name and password for the MID Server.|See [Enable MID Server mutual authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/install-mid-mutual-auth.md).|See [Set up a MID Server to use IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-set-up-ipki-authentication.md).|
|Per MID Server setting|The **mid.instance.username** and **mid.instance.password** parameters.|The **mid.instance.username** parameter is removed when mutual authentication is set up.|The **mid.ipki.enabled** parameter is set to `true`. The username and password are removed from `config.xml`. See, [MID Server IPKI reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-ipki-reference.md)|
|Where the credential is stored|The user name and password in `config.xml`, or in the keystore.|The key and certificate are in the MID Server keystore. The instance stores the CA chain in \[sys\_ca\_certificate\] and the client certificate in \[sys\_user\_certificate\].|The keypair is in the agent keystore. The instance stores the issued certificates in \[sys\_kmf\_certificate\].|
|What the MID Server presents|A user name and password.|A client certificate during the TLS handshake.|A JWT, signed with the private key of its certificate, sent as a bearer token in the Authorization header.|
|Certificate renewal and rotation|Not applicable.|You obtain and install a new certificate.|The MID Server requests a new certificate before the current one expires. Certificates are valid for 60 days, and rotation starts 15 days before expiration by default. To change this, set the **mid.ipki.rotation\_trigger\_threshold** parameter to a value from 8 to 59 days. You can rotate a certificate on demand by forcing rotation.|
|Revocation|Change or disable the user or password.|Controlled by your CA. The instance must be able to reach the OCSP and CRL endpoints of the certificate for revocation checks.|The instance tracks certificate activation and revocation continuously. A revoked MID Server is rejected even if its signature is still valid.|

**Parent Topic:**[Securing and encrypting MID Server data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-security-encryption.md)

**Related topics**  


[MID Server certificate check policies]()

[Encrypt or decrypt MID Server configuration file values]()

[MID Server configuration file security]()

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

[MID Server IPKI authentication]()

[Enable MID Server mutual authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/install-mid-mutual-auth.md)

[MID Server IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-ipki-authentication.md)

[Set up a MID Server to use IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-set-up-ipki-authentication.md)

[Migrate MID Servers to IPKI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-migrate-basic-to-ipki.md)

