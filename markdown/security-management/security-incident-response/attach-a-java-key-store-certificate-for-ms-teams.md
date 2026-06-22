---
title: Attach a Java Key Store certificate for MS Teams
description: Enable the JWT Bearer Grant token authentication by attaching a valid Java Key Store \(JKS\) certificate.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/attach-a-java-key-store-certificate-for-ms-teams.html
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

4.  Select the attachments icon \(\[Omitted image "attachments-icon.png"\] Alt text: Attachments icon\) and attach the JKS certificate you had generated.

    For more information, see [Configure OAuth application in Microsoft Azure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/configure-oauth-application-in-microsoft-azure.md).

5.  Click **Validate Stores/Certificates**.

6.  Click **Update**.


**Parent Topic:**[Using Certificates for authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/using-certificates-for-authentication.md)

