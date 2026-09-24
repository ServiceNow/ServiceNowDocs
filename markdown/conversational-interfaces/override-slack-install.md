---
title: Associate a Slack integration with a different instance
description: Override a Virtual Agent integration with Slack.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/override-slack-install.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Integrate Virtual Agent with Slack, Slack, Integrate VA with messaging apps, Conversational Integration apps for Virtual Agent, Conversational Interfaces]
---

# Associate a Slack integration with a different instance

Override a Virtual Agent integration with Slack.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

Prior to the Utah release, an admin was able to associate a Slack installation that was already associated with an instance with a different ServiceNow instance.

Beginning with the Utah release, if your Slack workspace is already associated with a ServiceNow instance, but you want to associate it with a new instance, you must reach out to the administrator to first uninstall it from the previously associated instance.

\[Omitted image "slack-new-proceed-install.png"\] Alt text: A message appears when the Slack workspace is already associated with a ServiceNow instance.

**Important:** The instructions in [Remove Virtual Agent integration with Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/uninstall-virtual-agent-slack.md) are only applicable when both instances are compatible with Utah or more recent releases. If one of your ServiceNow instances is on the Utah release, and another is on a release prior to Utah, follow the steps below.

## Procedure

1.  Navigate to **All**, and enter `sys_properties_list` in the filter.

2.  Search for and open the **sn\_va\_slack.enable\_slack\_override** system property.

    **Note:** If you don't find this system property, you \(as an admin\) must create one.

3.  Set the system property value to **true** to enable the **Override** button.

    By default, the value of the system property is **false**.

4.  Select **Override** to associate the instance with a new tenant.

    \[Omitted image "slack-override.png"\] Alt text: Slack installation window with the Override button enabled.


**Parent Topic:**[Integrating Virtual Agent with Slack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/va-integ-slack.md)

