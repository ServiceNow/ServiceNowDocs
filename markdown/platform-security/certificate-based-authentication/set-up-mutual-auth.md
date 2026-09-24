---
title: Set up Certificate-based authentication
description: Set up mutual authentication for either user interface-based logins or inbound web services.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/certificate-based-authentication/set-up-mutual-auth.html
release: brazil
product: Certificate-based Authentication
classification: certificate-based-authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [certificate-based authentication, mutual authentication, PIV, CAC, PEM certificate, inbound web services, REST, SOAP, sso\_config\_admin, ADCv2]
audience: administrator
breadcrumb: [Certificate-based authentication, Authentication, Access Management]
---

# Set up Certificate-based authentication

Set up mutual authentication for either user interface-based logins or inbound web services.

## Before you begin

Role required: sso\_config\_admin

Check that your instance is using an ADCv2 load balancer. For more information, see the[ADCv2 Migration knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0952875). If your instance is not using the ADCv2 load balancer, contact Now Support.

**Note:**

-   Certificate Based Authentication is not supported on the On-Prem and edge encryption enabled instance.
-   To enable Certificate Based Authentication on self-hosted instance, review this [KB article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1272738) and follow the instructions available in the **Native Certificate-Based Authentication** row within the table.

.

## Procedure

1.  Set up Certificate-based authentication to:

    -   Allow end users to securely log in to the ServiceNow AI Platform or Service Portal using PIV or CAC cards. After certificate-based authentication is enabled, you can self-register the PEM certificate or an administrator can map the certificate for you. See [Log in using Certificate-based authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/certificate-based-authentication/ui-login-mutual-auth.md).
    -   Enable mutual authentication for inbound web services. Once Certificate-based authentication is set up, the system uses the provided certificates to mutually authenticate requests to access ServiceNow REST and SOAP APIs.

