---
title: Configure McAfee ESM - Email Parser integration
description: McAfee ESM - Email Parser integration uses email notifications from ESM to drive enrichment, and response workflows.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [McAfee ESM - Email Parser integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure McAfee ESM - Email Parser integration

McAfee ESM - Email Parser integration uses email notifications from ESM to drive enrichment, and response workflows.

## Before you begin

Role required: sn\_si\_admin

## About this task

A McAfee ESM email parser template is provided to use for the integration. It must be configured and activated before the integration takes place. Updating the parser activates it.

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

    The available security integrations appear as a series of cards.

    ![McAfee ESM - Email Parser integration card](../image/intel-mcafee-esm-emailparser-plugin-card.png)

2.  In the McAfee ESM - Email Parser card, click **Configure**.

3.  In the **McAfee ESM - Email Parser Configuration** dialog box, click the **Configure Email Parser** link.

4.  Click the **McAfee ESM** link to edit the settings in the template email parser provided.

    At a minimum, fill in the `Email is from` field. To create you own email parser, see [Create email parsers in Security Operations](../../../security-operations-common/task/parsing-emails.md).

5.  Check the **Active** box.

6.  Click **Update** in the **Email Parser** form.

    The email parser is active. You do not need to return to **Integration Configurations**.


