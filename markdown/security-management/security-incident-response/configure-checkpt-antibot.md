---
title: Configure the Check Point Anti-bot - Email Parser integration
description: The Check Point Anti-bot - Email Parser integration uses email notifications to drive enrichment, and response workflows.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Check Point Anti-bot - Email Parser integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure the Check Point Anti-bot - Email Parser integration

The Check Point Anti-bot - Email Parser integration uses email notifications to drive enrichment, and response workflows.

## Before you begin

Role required: sn\_si\_admin

## About this task

A Check Point Anti-bot email parser template is provided to use for the integration. It must be configured and activated before the integration takes place. Updating the parser activates it.

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

    The available security integrations appear as a series of cards.

    ![Check Point Anti-bot integration card](../image/checkpt-antibot-plugin-card.png)

2.  In the Check Point Anti-bot - Email Parser card, click **Configure**.

3.  In the **Check Point Anti-bot - Email Parser Configuration** dialog box, click the **Configure Email Parser** link.

4.  Click the **Check Point Anti-bot** link to edit the settings in the template email parser provided.

    At a minimum, fill in the `Email is from` field. To create an email parser, see [Create email parsers in Security Operations](../../../security-operations-common/task/parsing-emails.md).

5.  Check the **Active** box.

6.  Click **Update** in the **Email Parser** form.

    The email parser is active. You do not need to return to **Integration Configurations**.


