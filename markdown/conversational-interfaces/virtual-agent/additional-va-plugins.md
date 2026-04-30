---
title: Additional plugins for Virtual Agent
description: After activating Virtual Agent, you can activate additional plugins to enable other features for conversation design.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Activate Virtual Agent, Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Additional plugins for Virtual Agent

After activating Virtual Agent, you can activate additional plugins to enable other features for conversation design.

You must have the admin role to activate these additional plugins. For details, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

<table id="table_jwv_ct2_qhb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

-   Human Resources Service Delivery: HR Service Delivery Virtual Agent Conversations \[sn\_hr\_va\] available through the [ServiceNow](https://store.servicenow.com/sn_appstore_store.do#!/store/application/c8c5545573d8130000e588e54cf6a71a/) Store
-   ITSM Virtual Agent conversations \[sn\_itsm\_va\] available through the [ServiceNow](https://store.servicenow.com/sn_appstore_store.do#!/store/application/134450a0b3781300787162ac16a8dc1e/) Store
-   CSM Virtual Agent conversations \[com.sn\_csm.virtualagent\]

</td><td>

Enables [predefined Virtual Agent conversations, reusable topic blocks, and prebuilt ServiceNow NLU models](prebuilt-topics-ITSM.md) for the Customer Service Management, HR Service Delivery, and IT Service Management applications.

 -   Requires the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin to be activated.
-   Automatically activates the NLU Workbench \(com.snc.nlu\_studio\) plugin.
-   Automatically activates the Service Management Virtual Agent Topic Blocks \(com.glideapp.cs.sm\_topic\_blocks\) plugin. Includes common topic blocks such as contextual search.

</td></tr><tr><td>

NLU Workbench \[com.snc.nlu\_studio\]

</td><td>

Enables the creation of custom ServiceNow Natural Language Understanding \(NLU\) models used by Virtual Agent.

</td></tr><tr><td>

NLU Workbench - Advanced Features \[com.snc.nlu.workbench.advanced\]

</td><td>

Expands the functionality of NLU Workbench by providing conflict review, batch testing, and model performance features. Available from the ServiceNow® Store.

</td></tr><tr><td>

Conversational Analytics Dashboard\[com.sn.conversational.analytics\]

</td><td>

Provides insights into user interactions so you can see how well Virtual Agent understood and resolved user issues.

</td></tr></tbody>
</table>**Parent Topic:**[Activate Virtual Agent](../task/activate-virtual-agent.md)

