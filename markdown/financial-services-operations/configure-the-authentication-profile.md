---
title: Configure the Authentication Profile
description: The Verifi Issuer API uses JSON Web Tokens \(JWT\) for authentication. A fresh JWT must be generated for every API call. This section explains how to store credentials securely and how the ServiceNow script generates and attaches the JWT.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 1
breadcrumb: [Verifi, Integrate, Financial Services Operations \(FSO\)]
---

# Configure the Authentication Profile

The Verifi Issuer API uses JSON Web Tokens \(JWT\) for authentication. A fresh JWT must be generated for every API call. This section explains how to store credentials securely and how the ServiceNow® script generates and attaches the JWT.

## Before you begin

Role required: admin

## Procedure

1.  Create a new JSON Web Tokens \(JWT\) key with the signing key \(secret\) and the signing algorithm shared by Verifi.

2.  Create a new JWT provider with the JWT key created in previous step, update the **Expiry Interval** \(sec\) as mentioned by Verifi and update the iss standard claim value to the Issuer ID provided by Verifi.

3.  Create a new connection in sn\_verifi\_spoke.

    Configure the Verifi connection alias with the correct URL, the Issuer ID \(shared by Verifi\) and the JWT provider created in previous step, make sure that API version provided here is correct. See [../reference/jwt-authentication.md](../reference/jwt-authentication.md) for more information.

4.  Attach the required headers at call time.


-   **[Storing credentials for Verifi CDRN](../reference/store-credentials-for-verifi-cdrn.md)**  
Credential storage information for securely managing Issuer ID and Shared Secret values for Financial Services Operations Integration with Verifi.

**Parent Topic:**[configure-financial-services-integration-with-verifi-cdrn.md](configure-financial-services-integration-with-verifi-cdrn.md)

