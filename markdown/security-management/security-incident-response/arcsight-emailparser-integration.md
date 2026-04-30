---
title: HPE Security ArcSight ESM - Email Parser integration
description: The HPE Security ArcSight ESM - Email Parser integration is supported using an email parser that consumes email notifications from ESM to create security incidents.HPE Security ArcSight ESM - Email Parser integration uses email notifications from ESM to drive enrichment, and response workflows.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# HPE Security ArcSight ESM - Email Parser integration

The HPE Security ArcSight ESM - Email Parser integration is supported using an email parser that consumes email notifications from ESM to create security incidents.

## Configure HPE Security ArcSight ESM - Email Parser integration

HPE Security ArcSight ESM - Email Parser integration uses email notifications from ESM to drive enrichment, and response workflows.

### Before you begin

Role required: sn\_si\_admin

### About this task

An HPE Security ArcSight ESM - Email Parser template is provided to use for the integration. It must be configured and activated before the integration takes place. Updating the parser activates it.

### Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

    The available security integrations appear as a series of cards.

    ![HPE Security Arcsight ESM - Email Parser card](../image/arcsight-emailparser-plugin-card.png)

2.  In the HPE Security ArcSight ESM - Email Parser card, click **Configure**.

3.  In the **HPE Security ArcSight ESM - Email Parser Configuration** dialog box, click the **Configure Email Parser** link.

4.  Click the **ArcSight ESM** link to edit the settings in the template email parser provided.

    At a minimum, fill in the `Email is from` field. To create you own email parser, see [Create email parsers in Security Operations](../../../security-operations-common/task/parsing-emails.md).

5.  Check the **Active** box.

6.  Click **Update** in the **Email Parser** form.

    The email parser is active. You do not need to return to **Integration Configurations**.


