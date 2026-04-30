---
title: Configure an agent registration key
description: Configure an agent registration key so that you can deploy MID-less Agent Client Collector. Deploying MID-less Agent Client Collector enables you to use the MID Server for more persistent resources.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Configure an agent registration key

Configure an agent registration key so that you can deploy MID-less Agent Client Collector. Deploying MID-less Agent Client Collector enables you to use the MID Server for more persistent resources.

## Before you begin

Install the plugins necessary for deploying MID-less Agent Client Collector, as described in [Agent Client Collector installation](../concept/acc-installation.md).

Role required: agent\_client\_collector\_admin

## About this task

The Cleanup Agent Registration Keys scheduled job runs daily and deletes expired registration keys. The length of time for which a registration key is valid is controlled by the **sn\_agent.registration\_key\_validity.days** property, based on when the key was created. The amount of time that the customer is notified prior to upcoming key expiration is controlled by the **sn\_agent.registration\_key\_notification.days** property. For details on these properties, see [Agent Client Collector Framework configuration properties](../reference/acc-framework-configuration-properties.md).

If a key's expiration date is approaching, create a new registration key and enter it into any existing automation jobs to prevent registration outage.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Registration Key**.

2.  Select **New**.

3.  In the **Name** field, enter a descriptive name for the registration key.

4.  To receive notifications when a registration key is soon to expire, select a group with a valid email address in the **Ownership Group** field.

5.  Select **Submit**.


## Result

The new agent registration key is ready to use for installation.

