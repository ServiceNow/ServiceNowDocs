---
title: Create cross-scope access privileges for topic blocks and custom controls
description: Enable topic authors and developers to access Virtual Agent topic blocks and custom controls from other scoped applications.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
keywords: [Virtual Agent, Cross-scope, privileges, topic block, custom control]
breadcrumb: [Configuring Virtual Agent, Virtual Agent, Conversational Interfaces]
---

# Create cross-scope access privileges for topic blocks and custom controls

Enable topic authors and developers to access Virtual Agent topic blocks and custom controls from other scoped applications.

## Before you begin

Role required: admin

## About this task

Developers and topic authors may need to access [topic blocks](../concept/topic-blocks-overview.md) and [custom controls](../concept/custom-controls.md) created in other application scopes. To give them access, define cross-scope privilege records for the appropriate applications. For more information on cross-scope privileges, see [Cross-scope privilege record](https://www.servicenow.com/docs/access?context=c_CrossScopePrivilegeRecord&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

## Procedure

1.  Activate the Virtual Agent conversation plugins for the applications that are the source and target scopes, for example the CSM \(com.sn\_csm.virtualagent\) or ITSM Virtual Agent \(com.snc.itsm.virtualagent\) plugins.

2.  Set your application scope \(the Source scope requesting access\) using the [application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

3.  Navigate to **All** &gt; **System Applications** &gt; **Application Cross-Scope Access** and select **New**.

4.  On the Cross scope privilege form, complete the following fields.

    |Field|Value|
    |-----|-----|
    |Source scope|Application requesting access to another application's resources.|
    |Target Scope|Application whose resources are being requested \(the scope with the topic blocks or custom controls\).|
    |Target Name|Name of the asset being requested: sys\_cs\_topic|
    |Target Type|Table|
    |Operation|Read|
    |Status|Authorization for this record: Allowed|

5.  Select **Submit**.


## Result

The cross-scope privilege is listed in the Cross scope privileges \[sys\_scope\_privilege\] table. Topic authors or developers can access the topic blocks or custom controls from the target scope.

**Parent Topic:**[Configuring Virtual Agent](../concept/configure-virtual-agent.md)

