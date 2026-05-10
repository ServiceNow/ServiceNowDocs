---
title: Activate and configure third-party integrations
description: You can activate the plugins for third-party integrations and configure them for use from the same screen.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 1
breadcrumb: [Security Operations Integration Configurations, ServiceNow Security Operations integration development guidelines, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Activate and configure third-party integrations

You can activate the plugins for third-party integrations and configure them for use from the same screen.

## Before you begin

Role required: sn\_sec\_cmn.admin

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Integration Configuration**.

    The available security integrations appear as a series of cards, similar to the following group of cards. You can point to any card to get a description of the integration.

    ![Sample third-party integrations](../image/tiles.png)

2.  To install the plugin for a given integration, select **Install Plugin**.

    1.  On the System Plugin form, review the plugin details and select the **Activate/Upgrade** related link.

    2.  Select **Activate**.

        When the activation is complete, the Security Integration screen reopens and the button for the integration you activated is labeled **Configure**.

3.  Select **Configure**.

    **Note:** If you are configuring the Qualys Vulnerability Integration, see [Installation of Vulnerability Response and supported applications](../../vulnerability-response/concept/cj-vr-setup.md).

4.  Enter the **API Key**.

5.  Select **Submit**.


**Parent Topic:**[Security Operations Integration Configurations](../concept/third-party-integrations.md)

**Related topics**  


[Create an integration](../../security-operations-integrations/task/create-integrations.md)

