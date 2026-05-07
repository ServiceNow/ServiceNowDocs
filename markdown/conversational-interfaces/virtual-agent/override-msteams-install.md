---
title: Override Microsoft Teams integration
description: Override Virtual Agent integration with Microsoft Teams.
locale: en-US
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrate VA with Teams, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Override Microsoft Teams integration

Override Virtual Agent integration with Microsoft Teams.

## Before you begin

Role required: admin or virtual\_agent\_admin

## About this task

Before Tokyo release, an admin was able to override a Microsoft Teams installation that is associated with an instance with a different ServiceNow instance.

Starting from Tokyo release, if you intend to associate your Microsoft Teams tenant with a new ServiceNow instance, contact the administrator to uninstall the tenant from the previously associated instance.![Microsoft Teams integration removal message.](../images/msteams-new-proceed-uninstall.png)

**Important:** The instructions in [Remove Conversational Integration with Microsoft Teams](uninstall_va_msteams.md) are only applicable when both instances are compatible with Tokyo and following releases. If one of your ServiceNow instances is on the Tokyo release and another on a release prior to Tokyo, use the following steps.

## Procedure

1.  In the left navigation filter of your ServiceNow instance, enter `sys_properties.list`.

2.  Search and open the **sn\_va\_teams.enable\_va\_override** system property.

    **Note:** If you don't find this system property, you \(as an admin\) must create one.

3.  Set the system property value to **true** to enable the **Override** button.

    **Note:** By default, the value of the system property is **false**.

4.  Select **Override** to associate the instance with a new tenant.![Microsoft Teams override installation.](../images/msteams-new-override.png)


**Parent Topic:**[Integrate Virtual Agent with Microsoft Teams](va-integ-msteams.md)

