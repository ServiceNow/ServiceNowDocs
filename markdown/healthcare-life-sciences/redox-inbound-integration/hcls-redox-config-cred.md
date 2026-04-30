---
title: Configuring credentials in the Redox engine for sending requests to a ServiceNow instance
description: You configure your ServiceNow instance credentials in the Redox engine for sending requests to a ServiceNow instance.
locale: en-US
release: yokohama
product: Redox Inbound Integration
classification: redox-inbound-integration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Redox Inbound Integration, Redox Inbound Integration, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Configuring credentials in the Redox engine for sending requests to a ServiceNow instance

You configure your ServiceNow instance credentials in the Redox engine for sending requests to a ServiceNow instance.

**Important:**

Starting with the Yokohama release, Redox Inbound Integration is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

As a Redox administrator, configure your ServiceNow instance credentials in the Redox engine to send requests to a ServiceNow instance. For more information, see the [Redox documentation](https://docs.redoxengine.com/).

**Note:** To send requests to a ServiceNow instance from the Redox engine, ensure that you enter the REST API URL in the following format: `https://<instance name>/api/sn_redox/v1/redox_webhook_callbacks`.

In the Redox engine, a request is determined by the event type and workflow setup for your integration. For more information, see [Supported data models and event types for Redox Inbound Integration](../reference/hcls-redox-supported-dm.md).

