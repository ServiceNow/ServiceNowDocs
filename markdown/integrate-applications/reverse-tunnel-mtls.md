---
title: Reverse Tunnel mTLS authentication
description: Reverse Tunnel uses mutual TLS \(mTLS\) to authenticate private relays before any data is exchanged. Both the gateway and the relay verify each other's identity using X.509 certificates issued by the ServiceNow iPKI service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/reverse-tunnel-mtls.html
release: zurich
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [mTLS, mutual TLS, gateway authentication, Reverse Tunnel, iPKI]
breadcrumb: [Configure, Reverse Tunnel, Workflow Data Fabric]
---

# Reverse Tunnel mTLS authentication

Reverse Tunnel uses mutual TLS \(mTLS\) to authenticate private relays before any data is exchanged. Both the gateway and the relay verify each other's identity using X.509 certificates issued by the ServiceNow iPKI service.

## Why mTLS is required

Only relays that present a valid iPKI-issued certificate can register with the gateway, which helps prevent unauthorized data access.

## Certificate issuance

When a private relay starts up for the first time, a certificate signing request \(CSR\) is generated and submitted to the instance. The instance processes the request and returns a signed certificate. The certificate is stored locally and used to authenticate with the gateway on every subsequent connection.

ServiceNow iPKI issues and renews relay certificates automatically; you don't manage them.

Certificate expiration is checked on startup and daily. If the certificate expires within 30 days, a new CSR is generated, submitted to the instance, and the connection is re-established using the renewed certificate.

