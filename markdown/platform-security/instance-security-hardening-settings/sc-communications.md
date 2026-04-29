---
title: Communications
description: This control ensures proper encryption using strong algorithms and ciphers. This includes ensuring the recommended version of TLS is used for client connectivity, use of strong cipher suites, use of trusted and signed certificates, ensuring connections are encrypted between components and logging of connection failures.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Hardening settings, Platform Security]
---

# Communications

This control ensures proper encryption using strong algorithms and ciphers. This includes ensuring the recommended version of TLS is used for client connectivity, use of strong cipher suites, use of trusted and signed certificates, ensuring connections are encrypted between components and logging of connection failures.

-   **[Enforce certificate trust \[Updated in Security Center 1.3, removed in 2.0, added in 7.0\]](sc-certificate-trust.md)**  
Use system properties to ensure that certificate expiration and trust are checked for certificates received from outbound HTTPS call endpoints when host verification is not performed.
-   **[Disable outbound SSLv2/SSLv3 connections](sc-disabling-sslv2-sslv3.md)**  
Use the **glide.outbound.sslv3.disabled** property to force the MID Server to use TLS when making outbound connections, such as REST and SOAP requests. Normally, outbound connections from an instance are forced to use TLS instead of SSL.
-   **[Do not use demo certificates for active SAML configurations](sc-do-not-use-demo-certificates-active-saml-configurations-plugin.md)**  
Control whether demo certificates are used in production SAML configurations.
-   **[Disable deprecated TLS versions](sc-disable-deprecated-tls-versions.md)**  
Avoid loss or leakage of sensitive data by disabling deprecated TLS versions.
-   **[Enforce OCSP check on network error](sc-enforce-ocsp-check-on-network-error.md)**  
Learn how to configure the **com.glide.communications.httpclient.ocsp\_allow\_network\_error** property to prevent bad actors from bypassing Online Certificate Status Protocol \(OCSP\) checks.
-   **[Verify certificate chain and hostname](sc-verify-certificate-chain-and-hostname.md)**  
Configure the **com.glide.communications.httpclient.verify\_hostname** property to prevent man-in-the-middle-attacks by ensuring that the certification verification process is executed.
-   **[Verify certificate revocation](sc-verify-certificate-revocation.md)**  
The **com.glide.communications.httpclient.verify\_revoked\_certificate** property checks certificate revocation during the Transport Layer Security \(TLS\) handshake to ensure that security checks are not bypassed.

**Parent Topic:**[Hardening settings](security-hardening-settings.md)

