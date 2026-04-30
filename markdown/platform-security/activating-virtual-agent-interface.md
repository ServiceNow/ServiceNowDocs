---
title: Activate the ISC Virtual Agent interface
description: If you have the admin role, you can activate the ISC Virtual Agent Conversations plugin \(com.glide.isc\_virtualagent\). Activating this plugin installs the Virtual Agent and Natural Language Understanding \(NLU content packs, providing Virtual Agent access from the Instance Security Center.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Instance Security Center, Platform Security]
---

# Activate the ISC Virtual Agent interface

If you have the admin role, you can activate the ISC Virtual Agent Conversations plugin \(com.glide.isc\_virtualagent\). Activating this plugin installs the Virtual Agent and Natural Language Understanding \(NLU content packs, providing Virtual Agent access from the Instance Security Center.

## Before you begin

**Important:**

Instance Security Center \(ISC\) has reached the end of sales as of September 2024, and is no longer supported or available for new activation.

ServiceNow Security Center \(SSC\) is the recommended solution going forward. For more information, see [Instance Security Center to ServiceNow Security Center migration](../../security-center/concept/instance-security-center-to-security-center-migration.md).

The Virtual Agent interface in the Instance Security Center is only available for users with paid Virtual Agent subscriptions, and who have activated the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin. To learn more, see [Activate Virtual Agent](https://www.servicenow.com/docs/access?context=activate-virtual-agent&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US).

Role required: admin.

## About this task

The ISC Virtual Agent interface enables you to perform the following tasks:

-   Ask security-related questions, then get quick summary answers and reference links to learn more.
-   Get answers related to the Instance Security Center, Platform Security, ServiceNow security policies, trust, governance, risk, and other processes.
-   Search for security-related resources, such as Knowledge Base topics in the Now Support Security Portal.

<table id="table_afh_nxh_5gb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ISC Virtual Agent Conversations\[com.glide.isc\_virtualagent\]

</td><td>

Activates the ISC Virtual Agent Conversations content pack for the Instance Security Center.

</td></tr><tr><td>

ISC NLU Model for Virtual Agent Conversations\[com.glide.isc\_nlu\]

</td><td>

Activates the Natural Language Understanding \(NLU\) content pack for the Instance Security Center.

</td></tr></tbody>
</table>**Note:** Activating the com.glide.isc\_virtualagent plugin automatically activates com.glide.isc\_nlu. However, if you activate the com.glide.isc\_nlu plugin first, you must manually activate com.glide.isc\_virtualagent as well.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Instance Security Center](../concept/instance-security-center.md)

**Related topics**  


[Instance Security Center to ServiceNow Security Center migration](../../security-center/concept/instance-security-center-to-security-center-migration.md)

[Monitor security events](../concept/instance-sec-center-event-ribbon.md)

[Check the daily compliance score and configure security property settings](../concept/instance-sec-center-hardening.md)

[Scan for incorrect security definitions](../concept/scan-for-incorrect-security-definitions.md)

[Monitor instance metrics](../concept/monitoring-user-email-antivirus-metrics.md)

