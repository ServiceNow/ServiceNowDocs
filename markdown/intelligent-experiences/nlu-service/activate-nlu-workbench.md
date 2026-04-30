---
title: Activate the NLU Workbench
description: Activate the following plugins to activate the NLU Workbench.
locale: en-US
release: zurich
product: NLU Service
classification: nlu-service
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Exploring Natural Language Understanding, Natural Language Understanding, Enable AI experiences]
---

# Activate the NLU Workbench

Activate the following plugins to activate the NLU Workbench.

## Before you begin

Role required: admin

## About this task

Activate the following plugins if they aren't already active in your instance.

<table id="table_xln_51m_2nb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

NLU Workbench - Corecom.glide.nlu

</td><td>

Installs the required tables for persisting NLU models that are created using the NLU Workbench.

</td></tr><tr><td>

NLU Workbench com.snc.nlu\_studio

</td><td>

Enables the creation of Natural Language Understanding \(NLU\) models. These models can understand the intent \(action\) and entities \(details about the action\) for a given user utterance. Any ServiceNow application can invoke an NLU model.Requires the NLU Workbench - Core plugin and the NLU Common Model plugin.

</td></tr><tr><td>

Predictive Intelligence com.glide.platform\_ml

</td><td>

Enables the NLU Service APIs used for model creation and inference. Enables the creation of machine learning solutions that are trained on data in your instance. Provides frameworks for classification, similarity, and clustering. A trained solution can be invoked by any application by using a prediction API.

</td></tr><tr><td>

NLU Common Modelcom.glide.nlu.model

</td><td>

Packages all language NLU common models. Also includes commonly used pattern entities that can be imported and used in any NLU model in the NLU Workbench. Commonly used patterns like email, phone, and ServiceNow specific pattern entities such as INT, RITM are made available. Requires the NLU Workbench - Core plugin.

</td></tr><tr><td>

NLU Active Learning-Propertiescom.glide.nlu.active\_learning\_properties

</td><td>

Enables the nlu\_admin to configure the system properties for the Expert Feedback Loop application. If you don't use the Expert Feedback Loop application, this plugin is not used and can safely be ignored. For more information about the system properties for the Expert Feedback Loop, see the [NLU Expert Feedback Loop](../concept/nlu-expert-feedback-loop.md) documentation.

</td></tr></tbody>
</table>The following two plugins are for apps associated with a for-fee subscription and are available on the ServiceNow Store. Installing these apps adds additional features to the NLU Workbench. Contact your account manager if you are interested in these apps.

<table id="table_k5b_jsk_ktb"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Intent Discovery](../concept/intent-discovery.md) sn\_nlu\_discovery

</td><td>

Delivers the Intent Discovery feature, which identifies user intents by analyzing incident/case data. Use this application to help identify which intents to model and build for Virtual Agent conversations to attain maximum deflection. For more information, see [Install Intent Discovery](install-intent-discovery.md).

</td></tr><tr><td>

[NLU Workbench - Advanced Features](../concept/nlu-workbench-advanced-features.md) sn\_nlu\_workbench

</td><td>

Delivers the Model Performance, Multi-model Batch Testing, Cross-model Conflict Review, and Expert Feedback Loop features.For more information, see [Install NLU Workbench - Advanced Features](install-nlu-workbench-adv-features.md).

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the following plugins using the filter criteria and search bar: NLU Workbench - Core \(com.glide.nlu\), NLU Workbench \(com.snc.nlu\_studio\), Predictive Intelligence \(com.glide.platform\_ml\), and NLU Common Model \(com.glide.nlu.model\).

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Exploring Natural Language Understanding](../concept/nlu-explore.md)

