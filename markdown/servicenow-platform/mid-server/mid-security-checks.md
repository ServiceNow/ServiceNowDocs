---
title: MID Server certificate check policies
description: MID Server uses four kinds of security checks to secure external traffic. The security checks use TLS/SSL certificate validation, hostname validation, Certificate Revocation List \(CRL\), and Online Certificate Status Protocol \(OCSP\) validation to improve security. Control these security checks with the MID Server certificate check policies table.
locale: en-US
release: australia
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server certificate check policies

MID Server uses four kinds of security checks to secure external traffic. The security checks use TLS/SSL certificate validation, hostname validation, Certificate Revocation List \(CRL\), and Online Certificate Status Protocol \(OCSP\) validation to improve security. Control these security checks with the MID Server certificate check policies table.

<table id="table_m2t_cv4_nhb"><tbody><tr><td>

![Set-up indicator for security phase](../image/ProgressBarSecure.png)

</td></tr></tbody>
</table>## TLS/SSL certificate validation

TLS/SSL encryption security uses asymmetric encryption, also called public-key encryption. This encryption uses two cryptographic keys: the public key and the private key. The public key is used for encryption of data and is publicly visible. The private key is used for decryption of data and its security is essential to verifying authenticity. For more information about preparing your network, see [MID Server TLS/SSL certificate check policy Quebec upgrade information \[KB0867397\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867397).

In TLS/SSL certificate validation, the MID Server attempts to connect to a web server secured with a TLS or SSL certificate. The web server sends a copy of its TLS/SSL certificate to the MID Server. The MID Server checks the authenticity of the certificate and sends a message to the webserver. The webserver responds with a digitally signed acceptance for initiating an TLS/SSL encrypted session. After which the MID Server can begin encrypted communication with the web server.

## Hostname validation

Hostname verification is a part of HTTPS that involves a server identity check to ensure that the client is talking to the correct server. This check prevents sending information to a server after being redirected by a man in the middle attack.

The check involves verifying that the `dnsName` of the certificate sent by the server matches the URL used to make the request. According to RFC 6125, hostname verification should be done against the certificate's subjectAlternativeName's dNSName field. In some legacy implementations, the check is done against the certificate's commonName field. If the names don't match, the connection is terminated.

**Note:** Hostname validation derives the hostname from the validated certificate presented by the server. Therefore, TLS certificate validation is a pre-requisite for hostname validation.

## Online Certificate Status Protocol \(OCSP\)

OCSP involves contacting the remote certificate authority server and verifying the certificate before the MID Server communicates further with the target server. Compromised certificates can be a security vulnerability, especially if those certificates have the ability to sign other certificates. If certificates have been broken or forged, then a certificate authority can inform a client which certificates are invalid and should not be used.

An OCSP responder \(a server typically run by the certificate issuer\) returns a signed response that the certificate is 'good', 'revoked', or 'unknown'. If it cannot process the request, it may return an error code.

The certificate's issuer may delegate another authority to be the OCSP responder. This creates a chain of certificates that must be verified. The responder's certificate must be issued by the issuer of the certificate in question. The responder’s certificate must include a certain extension that marks it as an OCSP signing authority.

**Note:** OCSP checks are secondary HTTP calls made to an OCSP responder. The primary call may discontinue the connection based on the response from the OCSP responder.

## Certificate Revocation List \(CRL\)

CRL checking provides an alternative to OCSP for verifying certificate revocation status. Rather than querying a live OCSP responder, the MID Server downloads and caches Certificate Revocation Lists \(CRLs\) from URLs provided by the Certificate Authority \(CA\). The MID Server then checks the revocation status of certificates against the locally cached CRL during the SSL/TLS handshake. If a certificate appears on the CRL, the MID Server rejects the connection and logs the event.

CRLs are cached locally and updated periodically based on the CA's update schedule. If a CRL download fails, the system retries according to a configurable retry policy.

**Note:** As of May 7, 2025, Let's Encrypt no longer includes OCSP URLs in issued certificates and has deprecated its OCSP responders in favor of CRLs, following the CA/Browser Forum ballot SC-063, which made OCSP optional for Certificate Authorities and mandated CRL support. CRL checking ensures continued certificate revocation validation for certificates issued by CAs that no longer support OCSP.

## MID Server security policy

MID Server security policies control all HTTPS traffic originating from the MID Server. This includes HTTPS connections from the MID Server to an internet endpoint, ServiceNow URLs, intranet endpoints, as well as cloud endpoints.

![Certificate Check Policies](../image/mid-cert-check.png)

These connections can be further classified into 4 security policies:

-   **ServiceNow endpoint policy**

    This policy is the system default exclusively for ServiceNow URLs. On the MID Server `config.xml`, there are bootstrap properties which are only used to make first connection to the instance and will get updated with the system\_default policy.

-   **Internet policy**

    These policies cover all HTTPS connections initiated from MID Server to any endpoint on the internet.

-   **Intranet policy**

    These policies cover the reserved IP subnets, such as self-hosted networks.

-   **Overridden policy**

    You can override specific endpoints or URLs with this policy definition. Overridden policies take the highest order of precedence during operation.


Both tables are editable to include or exclude IP ranges, as well as control what kind of certificate validation checks need to be done. Enable all certificate validation checks to maximize security. The Quebec version has all policies and checks turned on by default for fresh installations.

For upgrading customers, the intranet policy has the certificate validation checks disabled by default. To improve security, configure and enable the policy for endpoints within the internal network.

**Note:** Internal endpoints or URLs need to possess a valid CA signed certificate for a successful connection.

For endpoints that host a self-signed certificate, either import the certificate to the MID Server trust store or disable the policy checks which validate that host. For more information about adding certificates, see [Add SSL certificates for the MID Server](../task/add-ssl-certificates.md#).

After upgrading to Quebec, go to the certificate check policies table and make changes to policy configuration if necessary. Once the MID Server starts up and connects to the instance, any subsequent HTTPS connection originating from the MID server will start applying these certificate checks at runtime. Insecure connections are broken with appropriate error messages.

## Use Instance Security Policy

The MID Server configuration parameter **mid.ssl.use.instance.security.policy** controls whether the MID Server uses its bootstrap parameters rather than the security policy from the instance. By default, **mid.ssl.use.instance.security.policy** is set to false in the **config.xml** so the bootstrap policies are not overwritten by the instance's.

This default setting can prevent some problems during MID Server setup. For example if the host is unable to reach the OCSP responder, then a new MID Server installation is not disrupted by an instance's policy of requiring OCSP connection.

The configuration parameter **mid.ssl.use.instance.security.policy** can be set for each MID Server. When set to true, the MID Server syncs all policies with the instance and the bootstrap configuration parameters are overwritten by the **\*.servicenow.com** policy on the instance **mid\_cert\_check\_policy** table. The final policies update the policy map in the MID Server memory as well as the **config.xml**.

The default parameters in the **config.xml** are:

-   `<parameter name="mid.ssl.bootstrap.default.check_cert_hostname" value="true"/>`
-   `<parameter name="mid.ssl.bootstrap.default.check_cert_chain" value="true"/>`
-   `<parameter name="mid.ssl.bootstrap.default.check_cert_revocation" value="false"/>`
-   `<parameter name="mid.ssl.use.instance.security.policy" value="false"/>`

Self-hosted or on-prem instances must add the following parameter for the **config.xml**: `<parameter name="mid.ssl.bootstrap.default.target_endpoint" value="FQDN_OF_THE_INSTANCE"/>`

**Parent Topic:**[Securing and encrypting MID Server data](mid-server-security-encryption.md)

**Related topics**  


[Encrypt or decrypt MID Server configuration file values](../task/mid-server-manual-encryption.md)

[MID Server configuration file security](../reference/mid-server-encrypter-api.md)

[MID Server authentication credentials and SOAP requests](mid-authentication-soap-requests.md#)

[MID Server unified key store](mid-unified-keystore.md#)

[Enable MID Server mutual authentication](../task/install-mid-mutual-auth.md)

[MID Server Azure Key Vault integration](../task/mid-azure-key-vault-integration.md#)

[MID Server command audit log](mid-audit-log.md)

[Rekey a MID Server](../task/t_RekeyAMIDServer.md)

[Add SSL certificates for the MID Server](../task/add-ssl-certificates.md#)

[MID Server SSH cryptographic algorithms](../reference/mid-ssh-algorithms.md)

[Attach a script file to a file synchronized MID Server](../task/mid-server-script-attach.md#)

[MID Server FIPS Enforced Mode](mid-fips-enforced.md#)

[MID Server Governance](mid-timeout.md)

