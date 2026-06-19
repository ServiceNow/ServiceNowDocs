---
title: Basic email setup
description: All production instances can send and receive email using ServiceNow - provided resources. The instance has an email address of instance@service-now.com.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/c\_StandardEmailConfiguration.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Email Administration, Notifications, Configure core features, Administer]
---

# Basic email setup

All production instances can send and receive email using ServiceNow - provided resources. The instance has an email address of instance@service-now.com.

## Network layout for standard email configuration

Below is an example of a basic email network with ServiceNow as the domain.

\[Omitted image "StandardEmailConfiguration.png"\] Alt text: Network layout of basic email

## Basic email services and features

-   Mail servers maintained by ServiceNow.
    -   Encrypt mail with opportunistic TLS \(Transport Layer Security\) if supported by your mail servers.

        If your internal mail servers send and receive messages via a TLS-encrypted channel, ServiceNow mail servers support that communication.

    -   Provide a dedicated mailbox for your instance.
-   Pre-configured email accounts to connect to ServiceNow mail servers.
    -   An SMTP account sends email to your primary Mail Exchange \(MX\) server from your instance email address of instance@service-now.com.
    -   A POP3 account receives email sent to your instance email address of instance@service-now.com.
-   High availability features from ServiceNow datacenters.
-   Spam detection for incoming email.

Administrators who want to use basic email services can do so by enabling the email properties for sending and receiving email.

-   **[Enable basic email](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/t_ConfiguringStandardEmail.md)**  
Enable basic email to use ServiceNow - provided email servers and accounts.

**Parent Topic:**[Configure email administration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/configuring-email-admin.md)

