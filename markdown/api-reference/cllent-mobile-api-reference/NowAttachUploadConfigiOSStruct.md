---
title: NowAttachmentUploadConfiguration structure - iOS
description: The NowAttachmentUploadConfiguration structure enables you to define the configuration information for an attachment that you are uploading to your ServiceNow instance.Sets the upload configuration values for the specified attachment.
locale: en-US
release: australia
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Mobile SDK - iOS, Mobile SDK API reference, API reference, API implementation and reference]
---

# NowAttachmentUploadConfiguration structure- iOS

The NowAttachmentUploadConfiguration structure enables you to define the configuration information for an attachment that you are uploading to your ServiceNow instance.

<table id="table_vx2_klw_5pb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

contentType

</td><td>

String

</td><td>

HTTP data content type.

</td></tr><tr><td>

encryptionContext

</td><td>

String

</td><td>

Optional. Sys\_id of an encryption context record. Specify this parameter to allow only users with the specified encryption context to access the attachment. Default: Attached file is not encrypted with any encryption context.

</td></tr><tr><td>

fileName

</td><td>

String

</td><td>

Name of the attachment file.

</td></tr><tr><td>

recordSysId

</td><td>

String

</td><td>

Sys\_id of the record on the ServiceNow instance to associate the attachment with.

</td></tr><tr><td>

tableName

</td><td>

String

</td><td>

Name of the table on the ServiceNow instance that contains the record specified in the **recordSysid** parameter.

</td></tr></tbody>
</table>**Parent Topic:**[Mobile SDK - iOS](../../concept/MobileSDKiOSAPI.md)

## NowAttachmentUploadConfiguration - init\(tableName: String, recordSysId: SysID, fileName: String, contentType: String, encryptionContext: String?\)

Sets the upload configuration values for the specified attachment.

<table id="table_shs_cgn_mqb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

tableName

</td><td>

String

</td><td>

Name of the table on the ServiceNow instance that contains the record specified in the **recordSysid** parameter.

</td></tr><tr><td>

recordSysId

</td><td>

String

</td><td>

Sys\_id of the record on the ServiceNow instance to associate the attachment with.

</td></tr><tr><td>

fileName

</td><td>

String

</td><td>

Name of the attachment file.

</td></tr><tr><td>

contentType

</td><td>

String

</td><td>

HTTP data content type.

</td></tr><tr><td>

encryptionContext

</td><td>

String

</td><td>

Optional. Sys\_id of an encryption context record. Specify this parameter to allow only users with the specified encryption context to access the attachment. Default: Attached file is not encrypted with any encryption context.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

The following code example shows how to call this function.

```
let recordSysId = "" // Sys_id of the record on the SN instance

let config = NowAttachmentUploadConfiguration(
  tableName: "tableName", 
  recordSysId: recordSysId, 
  fileName: "photo.png",
  contentType: "image/png", 
  encryptionContext: nil)
```

