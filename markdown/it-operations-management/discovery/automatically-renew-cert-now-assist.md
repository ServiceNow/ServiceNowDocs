---
title: Automatically renew certificates using the AI agent
description: Automatically renew a certificate using the certificate renewal AI agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/automatically-renew-cert-now-assist.html
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Certificate renewal AI agent, Automated certificate renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Automatically renew certificates using the AI agent

Automatically renew a certificate using the certificate renewal AI agent.

## Before you begin

Complete the following steps to configure your system for the certificate renewal AI agent:

1.  [Configure MID Server for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.md)
2.  [Add the required applications and capabilities to your MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md)

Role required: sn\_disco\_certmgmt.pki\_admin

## About this task

Navigate to the certificate that you want to renew and use the certificate renewal AI agent to renew the certificate.

## Procedure

1.  Navigate to **All** &gt; **Unique Certificates**.

2.  Select the certificate that you want to renew.

3.  Select the ServiceNow Otto icon.

    **Warning:** Make sure that you are on the unique certificate page of the certificate that you want to renew.

4.  Enter the prompt `Renew this certificate.`

5.  Respond to the AI prompts.


## Result

Progress updates are displayed during certificate renewal. The certificate renewal AI agent gives you a link to the task record that displays the status of the renewed certificate.

