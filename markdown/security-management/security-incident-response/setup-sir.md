---
title: Security Incident Response setup
description: Setup for Security Incident Response involves some mandatory steps and several optional steps, depending on your specific requirements. After you have downloaded Security Incident Response from the ServiceNow Store and installed it, you are ready to run the Setup Assistant to perform basic configuration for Security Incident Response and third-party integrations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/setup-sir.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response setup

Setup for Security Incident Response involves some mandatory steps and several optional steps, depending on your specific requirements. After you have downloaded Security Incident Response from the ServiceNow Store and installed it, you are ready to run the Setup Assistant to perform basic configuration for Security Incident Response and third-party integrations.

## The Security Incident Response setup process

The following diagram illustrates the setup process. It is separated into two sub-processes, downloading and configuring the Security Incident Response application.

\[Omitted image "sir-setup.png"\] Alt text: Security Incident Response setup process

The first setup step is to [download the Security Incident Response application from the ServiceNow Store](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/install-and-configure-sir.md). When the download is complete, several dependent applications, including the Setup Assistant, are loaded and ready for use to configure Security Incident Response.

## Setup Assistant

The Security Incident Response Setup Assistant is a wizard-like application that guides you, step-by-step, through the setup of your base Security Incident Response instance.

The Setup Assistant requires the sn\_secops\_setup.admin role. Users with the sn\_si.admin role automatically inherit this role.

\[Omitted image "playbook-setup-assist.png"\] Alt text: Setup assistant

The setup steps are fairly self-explanatory; however, if you require additional explanation, you can find additional assistance in the [Setup Assistant reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/setup-assistant-reference.md). After you have completed the setup using the Setup Assistant, you can perform [other optional setup procedures](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/t_ConfigureSIM.md), as needed. These procedures include options for:

-   Setting up the request life cycle
-   Creating catalogs and requests
-   Configuring notifications
-   Setting up manual and auto-assignment
-   Enabling the knowledge base, managed documents, and task activities

A new and improved Security Incident Response Workspace is available. For more information, see [Security Incident Response Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/sir-workspace-landing-page.md).

