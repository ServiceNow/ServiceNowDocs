---
title: Components installed with voice
description: Information about the roles, tables, and scheduled jobs that are installed with Voice Agents.
locale: en-US
release: zurich
product: Now Assist for HRSD
classification: now-assist-for-hrsd
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Now Assist for HR Service Delivery \(HRSD\), HR Service Delivery, Employee Service Management]
---

# Components installed with voice

Information about the roles, tables, and scheduled jobs that are installed with Voice Agents.

## AI voice agent roles

The following table lists the roles installed with the Voice for Now Assist plugin.

|Roles|Description|
|-----|-----------|
|sn\_voice\_aia.admin|Provides access to agents configuration flow|
|sn\_hr\_voice\_aia.admin|Provides access to HR Voice AI agents configuration|
|sn\_voice\_aia.guest|Enables employees to use AI voice agents without authentication|
|sn\_voice\_aia.integration|Enables access to integrations such as Oracle|

## AI voice agent attributes

The AI voice agent attributes enable you to configure the authentication functionality for AI voice agents. Navigate to **All** &gt; **System Definition** &gt; **Tables** and search for Now Assist Deployment Config Attributes table to view the attributes.

The following table lists the attributes related to AI voice agent configuration.

|Attribute|Description|
|---------|-----------|
|voice\_max\_retries|The maximum number of retries allowed for successful authentication before the user account is locked. The default value is 3.|
|voice\_minutes\_account\_is\_locked|The number of minutes the user account is locked for, following maximum retries. The default value is 1440 minutes.|

## AI voice agent system properties

The following table consists of system properties to set up AI voice agents.

|Property|Description|
|--------|-----------|
|sn\_aia.enable\_voice\_agent\_setup|The system property to enable AI voice agents. Set the value of the property to true to enable AI voice agents on the instance.|

**Parent Topic:**[Reference for Now Assist for HR Service Delivery \(HRSD\)](reference-now-assist-hrsd.md)

