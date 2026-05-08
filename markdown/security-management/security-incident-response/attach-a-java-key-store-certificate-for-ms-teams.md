---
title: Attach a Java Key Store certificate for MS Teams
description: Enable the JWT Bearer Grant token authentication by attaching a valid Java Key Store \(JKS\) certificate.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using Certificates for authentication, Establish MS Teams Graph connection on ServiceNow AI Platform, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Attach a Java Key Store certificate for MS Teams

Enable the JWT Bearer Grant token authentication by attaching a valid Java Key Store \(JKS\) certificate.

## Before you begin

Login to your ServiceNow instance to perform the following procedure.

-   Valid Java Key Store certificate
-   Role required: admin

## Procedure

1.  Navigate to **System Definition** &gt; **Certificates**.

2.  Open the record **Microsoft Teams Connector Certificate**.

    Ensure to use the default record **Microsoft Teams Connector Certificate** only.

3.  Enter the password associated with the JKS file in **Key store password**.

4.  Select the attachments icon \(![Attachments icon](../../../administer/integrationhub-store-spokes/image/attachments-icon.png)\) and attach the JKS certificate you had generated.

    For more information, see Configure OAuth application in Microsoft Azure.

5.  Click **Validate Stores/Certificates**.

6.  Click **Update**.


**Parent Topic:**[Using Certificates for authentication](using-certificates-for-authentication.md)

