---
title: Exploring Certificates
description: Your instance requires certificates to establish secure connections and validate signatures.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Certificates, Encryption]
---

# Exploring Certificates

Your instance requires certificates to establish secure connections and validate signatures.

Certificates are used for features such as:

-   [LDAPS](../../../integrate/ldap/reference/r_LDAPIntegrationFAQs.md)
-   Outbound web service mutual authentication
-   [Web service security](../../security/concept/c_WebServiceSecurity.md)
-   MID Server

In order to use a certificate, you must generate or purchase a certificate for the secured server, or client and upload it to an instance.

## LDAP certificates

An SSL certificate is required for the instance to establish an LDAP over SSL \(LDAPS protocol\) connection with an LDAP server.

The instance accepts two types of LDAP certificates:

|Certificate|Type|Required for|
|-----------|----|------------|
|LDAP server certificate|Any supported type|All LDAP configurations|
|LDAP client certificate|Java keystore type|Mutual authentication|

If there are multiple server certificates, the instance tries each server certificate in turn until the LDAP server allows the connection. If you use multiple LDAP servers, be sure to include the SSL certificate for each LDAP server.

Mutual authentication requires the client to present a certificate in addition to the server. If your LDAP server requires mutual authentication, you must also provide your LDAP server's client certificate in a Java keystore type certificate.

## Certificate criteria

A valid certificate must meet these criteria:

-   The certificate can have a key size up to 2048 bits.
-   The certificate must have one of these file extensions:

    |Extension|Description|
    |---------|-----------|
    |DER|The Distinguished Encoding Rules format is a binary message transfer syntax. This format also supports the .CER and .CRT file extensions.|
    |CER|Certificate file extensions for certificates using the Distinguished Encoding Rules format.|
    |CRT|Certificate file extensions for certificates using the Distinguished Encoding Rules format.|
    |PEM|The Privacy Enhanced Mail format is a base-64 encoded DER certificate enclosed between "-----BEGIN CERTIFICATE-----" and "-----END CERTIFICATE-----" text strings.|


## Certificate trust

By default, your instance trusts only certificates from a Certificate Authority \(CA\) recognized in the Java Virtual Machine \(JVM\). Self-signed and enterprise-signed certificates aren’t trusted.

**Note:** To learn more about the properties that affect the use of certificates, see  in Instance Security Hardening Settings.

**Parent Topic:**[Certificates](c_Certificates.md)

**Related topics**  


[Generating an LDAP client certificate](../task/t_GenerateAnLDAPClientCertificate.md)

[Uploading a certificate to an instance](../task/t_UploadACertificateToAnInstance.md)

