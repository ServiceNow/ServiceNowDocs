---
title: SOAP template post-processing parameters
description: Use these parameters to create a post-processing script.
locale: en-US
release: xanadu
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a SOAP web service activity, Orchestration custom activity templates, Orchestration activity designer, Classic Orchestration, Creating integrations with applications]
---

# SOAP template post-processing parameters

Use these parameters to create a post-processing script.

|Name|Variable|Type|Usage|
|----|--------|----|-----|
|Status code|status\_code|Integer|Contains the status code returned from the web service.|
|Header|header|Hashmap of JavaScript object|Contains the key value paired hashmap associated with the header values passed into the web service. You can access each value with `executionResult.header[keyName]`.|
|Body|body|String|Contains a string value representing the output from the SOAP message|
|Error|error|String|Returns the error string from the SOAP web service, unless there are no errors, in which case it returns**null**.|

**Parent Topic:**[Create a SOAP web service activity](../task/t_CreateASOAPWebServiceActivity.md)

