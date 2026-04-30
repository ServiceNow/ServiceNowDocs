---
title: Override Slack integration
description: Override Virtual Agent integration with Slack.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating ServiceNow Virtual Agent with Slack, Conversational Integration with Slack, Integrating Virtual Agent with enterprise messaging apps, Virtual Agent integration with messaging apps, Integrating Virtual Agent with other channels, Virtual Agent, Conversational Interfaces]
---

# Override Slack integration

Override Virtual Agent integration with Slack.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Before Utah release, an admin was able to override a Slack installation that is associated with a particular instance with a different ServiceNow instance.

Starting from Utah release, if your Slack workspace is already associated with another ServiceNow instance, but you intend to associate it with a new instance, then you must reach out to the administrator to first uninstall it from the previously associated instance.

![A message appears when the Slack workspace is already associated with a ServiceNow instance.](../images/slack-new-proceed-install.png)

**Important:** The instructions in [Remove ServiceNow Virtual Agent integration with Slack](uninstall-virtual-agent-slack.md) are only applicable when both instances are compatible with Utah and the above releases. If one of your ServiceNow instances is on the Utah release and another on a release prior to Utah, follow the steps below.

## Procedure

1.  In the left navigation filter of your ServiceNow instance, enter `sys_properties_list`.

2.  Search and open the **sn\_va\_slack.enable\_slack\_override** system property.

    **Note:** If you don't find this system property, you \(as an admin\) must create one.

3.  Set the system property value to **true** to enable the **Override** button.

    By default, the value of the system property is **false**.

4.  Select **Override** to associate the instance with a new tenant.

    ![Slack installation window with the Override button enabled.](../images/slack-override.png)


