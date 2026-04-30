---
title: ProcessMiningForExternalData - Scoped, Global
description: The ProcessMiningForExternalData API contains a method that marks an external audit record for processing.Marks the specified record in the External dataset \[sn\_po\_extdata\_dataset\] table for processing. Use this method to automate the processing of external audit data.
locale: en-US
release: xanadu
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# ProcessMiningForExternalData - Scoped, Global

The ProcessMiningForExternalData API contains a method that marks an external audit record for processing.

This external audit data may come for external systems such as SAP, SmartRecruiters, or Jira.

To access this API, the Process Mining for external data \(sn\_po\_extdata\) plugin must be installed and the calling entity must have the sn\_process\_optimization\_admin role.

For additional information on external audit records and Process Mining, see [Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## ProcessMiningForExternalData - scheduleCaseGeneration\(String externalDataSysId\)

Marks the specified record in the External dataset \[sn\_po\_extdata\_dataset\] table for processing. Use this method to automate the processing of external audit data.

Before calling this method, the external audit data must have already been imported into the External dataset table.

You can choose your desired method of importing this data, such as by Integration Hub or Workflow Studio. You can schedule this import on some fixed interval such as weekly, monthly, or quarterly. For additional information, see [Working with external datasets](https://www.servicenow.com/docs/access?context=external-dataset&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

After the data is imported, you call this method to set the state field in the specified External dataset record to "Scheduled." This setting indicates that the specified external dataset record is ready for processing. When processed, the data within the external dataset record is used to create audit and case records. The names of these audit and case records appear in the associated External dataset record.

**Note:** When the call returns, it has only marked the record for processing. The actual processing of the record is done in the background.

This API is available in both global and scoped. Use the following syntax when calling this method:

-   Global: `SNC.ProcessMiningForExternalData.scheduleCaseGeneration(String externalDataSysId);`
-   Scoped: `ProcessMiningForExternalData.scheduleCaseGeneration(String externalDataSysId);`

|Name|Type|Description|
|----|----|-----------|
|externalDataSysId|String|Sys\_id of the dataset record in the External dataset \[sn\_po\_extdata\_dataset\] table to mark as ready to be processed.|

<table id="table_ynz_k1w_hzb" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

Status of the method call.When successful, the message is always: `External dataset is scheduled for processing`.

When an error occurs, the message describes why the call failed.

</td></tr><tr><td>

status

</td><td>

Status of the method call.Possible values:

-   error
-   success

</td></tr></tbody>
</table>The following code example shows how to call this method.

```
ProcessMiningForExternalData.scheduleCaseGeneration("o83ehu2yv918ehbu23eg928dg7jbcf52");
```

Output:

```
{
  "status": "success",
  "message": "External dataset is scheduled for processing"
}
```

