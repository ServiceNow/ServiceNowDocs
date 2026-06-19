---
title: Configuring Financial Services Operations Integration with Verifi
description: Configure the connection between ServiceNow FSO Dispute Management application to the Verifi Cardholder Dispute Resolution Network \(CDRN\) API to enable end-to-end dispute case submission and resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/financial-services/configure-financial-services-integration-with-verifi-cdrn.html
release: australia
product: Financial Services
classification: financial-services
topic_type: task
last_updated: "2026-04-02"
reading_time_minutes: 1
breadcrumb: [Verifi, Integrate, Financial Services Operations \(FSO\)]
---

# Configuring Financial Services Operations Integration with Verifi

Configure the connection between ServiceNow FSO Dispute Management application to the Verifi Cardholder Dispute Resolution Network \(CDRN\) API to enable end-to-end dispute case submission and resolution.

## Before you begin

Role required: admin

Contact the Verifi Issuer Integration Team to obtain the following information before you start.

**Note:** These values are environment-specific and must not be shared across UAT and Production.

|Item|Description|
|----|-----------|
|Issuer ID|Numeric identifier assigned to your organization within the CDRN platform. Included in every request header and JWT payload.|
|Shared Secret|32-character string used to sign the HMAC SHA-256 JWT. Treat as a password — store in ServiceNow Credential Store, never in plain text.|
|UAT Base URL|https://verifiapitest.visa.com|
|Production Base URL|https://verifiapi.visa.com|

## About this task

Obtain the following information from the Verifi team.

## Procedure

1.  [Configure the REST End Point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services/configure-rest-end-point.md)

2.  

3.  [Configure the Authentication Profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services/configure-the-authentication-profile.md)


-   **[Configure the REST End Point](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services/configure-rest-end-point.md)**  
The REST Endpoint record in ServiceNow® stores the base URL, API version header, and connection properties for the Verifi API. Create two endpoint records: one for UAT testing and one for Production.
-   **[Configure the Authentication Profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services/configure-the-authentication-profile.md)**  
The Verifi Issuer API uses JSON Web Tokens \(JWT\) for authentication. A fresh JWT must be generated for every API call. This section explains how to store credentials securely and how the ServiceNow® script generates and attaches the JWT.

**Parent Topic:**[Financial Services Operations Integration with Verifi](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/financial-services/financial-services-operations-verifi-cdrn-integration-app-landing-page.md)

