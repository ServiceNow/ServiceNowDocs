---
title: RESTMessageV2 - saveResponseBodyAsAttachment\(String tableName, String recordSysId, String fileName, String encryptContext\)
description: Configures the REST message to save the returned response body as an encrypted attachment record.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# RESTMessageV2 - saveResponseBodyAsAttachment\(String tableName, String recordSysId, String fileName, String encryptContext\)

Configures the REST message to save the returned response body as an encrypted attachment record.

When you use this function with a REST message that is sent through a MID server, the MID server user must have any roles required to read and write attachment records, as well as any roles required to read and write records on the table specified in the **tableName** parameter.

The response body does not need to be a binary file to be saved as an attachment. Response bodies using text formats, such as JSON or XML can also be saved. If the instance fails to save the attachment, call getErrorMessage\(\) on the related RESTResponseV2 object for error details.

|Name|Type|Description|
|----|----|-----------|
|tableName|String|Specify the table that contains the record you want to attach the saved file to.|
|recordSysId|String|Specify the sys\_id of the record you want to attach the saved file to.|
|fileName|String|Specify the file name to give to the saved file.|
|encryptContext|String|Specify the sys\_id of an encryption context. The saved file is encrypted using this context.|

|Type|Description|
|----|-----------|
|void| |

