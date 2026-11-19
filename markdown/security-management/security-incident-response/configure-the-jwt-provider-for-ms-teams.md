---
title: Configure the JWT provider for MS Teams
description: Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/configure-the-jwt-provider-for-ms-teams.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Certificates for authentication, Establish MS Teams Graph connection on ServiceNow AI Platform, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure the JWT provider for MS Teams

Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.

## Before you begin

-   Copy and record the value of **Application \(client\) ID** and **Directory \(tenant\) ID** of the application you had registered in the Azure portal.

    \[Omitted image "ms-sharept-clientid.png"\] Alt text: Copy the values of Client ID and Tenant ID.

-   Role required: admin

## Procedure

1.  Navigate to **System OAuth** &gt; **JWT Providers**.

2.  Open the record **MS Teams Connector JWT Provider**.

3.  Enter values for **iss**, **sub**, and **aud** in the Standard Claims related list.

    |Field|Value|
    |-----|-----|
    |aud|Microsoft Online URL in this format: `https://login.microsoftonline.com/<tenant-id>/oauth2/token`. Replace `<tenant-id>` with **Directory \(tenant\) ID** value of your application had registered in the Azure portal.|
    |iss|**Application \(client\) ID** of the application you had registered in Azure portal.|
    |sub|**Application \(client\) ID** of the application you had registered in Azure portal.|

4.  Click **Update**.


**Parent Topic:**[Using Certificates for authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/using-certificates-for-authentication.md)

