---
title: Configure System Properties for automatic certificate renewal
description: Enable the auto-renewal options in your System Properties to configure your system to renew automatically Transport Layer Security \(TLS\) certificates before they expire.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery/config-sys-props-for-auto-cert-renewal.html
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-08-19"
reading_time_minutes: 1
breadcrumb: [Configuring automated certificate renewal, Automated Certificate Renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Configure System Properties for automatic certificate renewal

Enable the auto-renewal options in your System Properties to configure your system to renew automatically Transport Layer Security \(TLS\) certificates before they expire.

## Before you begin

Check that you have completed the tasks, [Configure your MID Server for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.md), and [Add the required applications and capabilities to your MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md).

Role required: pki\_admin or admin

## About this task

Configuring your system properties to enable automatic certificate renewal is required for using the automatic renewal workflow and the Now Assist AI certificate renewal agent.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Search for **auto\_renew**.

3.  Select **sn\_disco\_certmgmt.enable\_auto\_renewal\_options\_in\_service\_catalog**

4.  Set the **Value** field to **true**.


## Result

Your system is configured to renew automatically certificates before they expire.

## What to do next

You can [Set a certificate to renew automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/set-certificate-to-renew-automatically.md) or use the [Now Assist certificate renewal AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-cert-renewal-ai-agent.md).

