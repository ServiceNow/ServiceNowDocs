---
title: Configure an agent registration key
description: Configure an agent registration key so that you can deploy MID-less Agent Client Collector. Deploying MID-less Agent Client Collector enables you to use the MID Server for more persistent resources.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Configure an agent registration key

Configure an agent registration key so that you can deploy MID-less Agent Client Collector. Deploying MID-less Agent Client Collector enables you to use the MID Server for more persistent resources.

## Before you begin

Install the plugins necessary for deploying MID-less Agent Client Collector.

Role required: agent\_client\_collector\_admin

## About this task

The Cleanup Agent Registration Keys scheduled job runs daily and deletes expired registration keys. The length of time for which a registration key is valid is controlled by the **sn\_agent.registration\_key\_validity.days** property, based on when the key was created. The amount of time that the customer is notified prior to upcoming key expiration is controlled by the **sn\_agent.registration\_key\_notification.days** property.

If a key's expiration date is approaching, create a new registration key and enter it into any existing automation jobs to prevent registration outage.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **Agent Registration Key**.

2.  Select **New**.

3.  In the **Name** field, enter a descriptive name for the registration key.

4.  To receive notifications when a registration key is soon to expire, select a group with a valid email address in the **Ownership Group** field.

    When keys are deleted via the Cleanup Agent Registration Keys scheduled job, the indicated group receives an email notification.

5.  Select **Submit**.


## Result

The new agent registration key is ready to use for installation.

**Parent Topic:**[Deploying Agent Client Collector on endpoints](../concept/acc-endpoint-deployment.md)

**Related topics**  


[Installing MID-less Agent Client Collector](../concept/acc-itom-cloud-services.md)

[Agent Client Collector Framework configuration properties](../reference/acc-framework-configuration-properties.md)

