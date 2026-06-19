---
title: Components installed with voice
description: Information about the roles, tables, and scheduled jobs that are installed with Voice Agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/now-assist-for-csm/components-installed-with-voice.html
release: zurich
product: Now Assist for CSM
classification: now-assist-for-csm
topic_type: reference
last_updated: "2026-05-18"
reading_time_minutes: 1
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [AI voice agent, Use agentic AI in CSM, Now Assist for CSM, Customer Service Management]
---

# Components installed with voice

Information about the roles, tables, and scheduled jobs that are installed with Voice Agents.

## AI voice agent roles

The following table lists the roles installed with the Voice for Now Assist plugin.

|Role|Description|
|----|-----------|
|`sn_voice_aia.admin`|Provides access to agents configuration flow.|
|`sn_voice_aia.guest`|Enables employees to use AI voice agents without authentication.|
|`sn_voice_aia.integration`|Enables access to integrations such as Genesys.|

## AI voice agent attributes

The AI voice agent attributes enable you to configure the authentication functionality for AI voice agents. Navigate to **All** &gt; **System Definition** &gt; **Tables** and search for the **Now Assist Deployment Config Attributes** table to view the attributes.

The following table lists the attributes related to AI voice agent configuration.

|Attribute|Description|
|---------|-----------|
|`voice_max_retries`|The maximum number of retries allowed for successful authentication before the user account is locked. The default value is `3`.|
|`voice_minutes_account_is_locked`|The number of minutes the user account is locked for, following maximum retries. The default value is `1440` minutes.|

## AI voice agent system properties

The following table consists of system properties to set up AI voice agents.

|Property|Description|
|--------|-----------|
|`sn_aia.enable_voice_agent_setup`|The system property to enable AI voice agents. Set the value of the property to `true` to enable AI voice agents on the instance.|

