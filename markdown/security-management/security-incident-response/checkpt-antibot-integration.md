---
title: Check Point Anti-bot - Email Parser integration
description: Check Point Anti-bot - Email Parser integration is supported using an email parser that consumes email notifications from Check Point Anti-bot to create security incidents and drive enrichment and response workflows.The Check Point Anti-bot - Email Parser integration uses email notifications to drive enrichment, and response workflows.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Check Point Anti-bot - Email Parser integration

Check Point Anti-bot - Email Parser integration is supported using an email parser that consumes email notifications from Check Point Anti-bot to create security incidents and drive enrichment and response workflows.

## Configure the Check Point Anti-bot - Email Parser integration

The Check Point Anti-bot - Email Parser integration uses email notifications to drive enrichment, and response workflows.

### Before you begin

Role required: sn\_si\_admin

### About this task

A Check Point Anti-bot email parser template is provided to use for the integration. It must be configured and activated before the integration takes place. Updating the parser activates it.

### Procedure

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


