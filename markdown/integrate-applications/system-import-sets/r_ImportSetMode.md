---
title: Web service import set mode
description: When a SOAP message inserts a record into an import set table, and there is no import set for that table in the Loading state, a new import set will be created with the Mode set to Synchronous.
locale: en-US
release: yokohama
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Web service import sets, Import sets, Imports, Data and Automation]
---

# Web service import set mode

When a SOAP message inserts a record into an import set table, and there is no import set for that table in the **Loading** state, a new import set will be created with the **Mode** set to **Synchronous**.

An import set with a Mode of Synchronous will transform the data as soon as it is inserted \(provided that the transform map already exists\). This import set will also have a default State of Loading. By default, all Synchronous import sets will automatically be modified to Processed at midnight. As a result, when a new insert happens to the same table, a new Synchronous import set will be created.

![](../image/WsIsetIset.png "Synchronous import set")

Changing this import set to a mode of Asynchronous and a state of Loading has the effect of not transforming the incoming data as it is inserted, but rather "loading" the import set and deferring the data transformation later, either manually, or with a scheduled script job.

|Mode|State|Function|
|----|-----|--------|
|Asynchronous|Loading|Data transformation is not occurring automatically and immediately. Data added to import set row has a state of "Pending". Transform can be scheduled or executed manually when state is changed to Loaded|
|Asynchronous|Loaded|Marks the completion of data loading. Data transformation can now occur in a scheduled fashion or manually.|
|Synchronous|Loading|Data transformation is occurring automatically and immediately whenever data is inserted into the associated import set row.|
|Synchronous|Loaded|When new data is inserted into this associated import set, a new import set of mode Synchronous and state Loading will be created. Changing the state to Loaded is a way to indicate that a new Synchronous import set should be created for the next import set row insert \(and transformed immediately\)|

## Controlling Insert Behavior

In imports sets that specify one or more coalesce fields, records with a matching coalesce value are transformed from source to target table serially \(one at a time\) to prevent duplicates.

In import sets that do not specify any coalesce field, records are transformed concurrently. You can control this behavior using the **glide.import\_set\_insert\_serialized\_when\_no\_coalesce** property.

The **glide.import\_set\_insert\_serialized.&lt;table name&gt;** system property controls how the instance inserts records from web service calls into a specific import set table. When true, this property prevents identical simultaneous inserts from creating duplicate records by serializing the database insert operations. If a target table does not have any coalesce fields defined in a transform map, set this property to false to improve web service import set performance.

**Note:** Setting this property to **false** can result in the creation of duplicate records.

**Note:** The **glide.soap.import\_set\_insert\_serialized.&lt;table name&gt;** system property provides equivalent functionality to **glide.import\_set\_insert\_serialized.&lt;table name&gt;**, but if both properties are defined, **glide.import\_set\_insert\_serialized.&lt;table name&gt;** supersedes **glide.soap.import\_set\_insert\_serialized.&lt;table name&gt;**.

## Standard SOAP Response

The SOAP response from a web service import set insert call returns the following standard values.

```
<SOAP-ENV:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/" SOAP-ENV:encodingStyle="http://schemas.xmlsoap.org/soap/encoding/"><SOAP-ENV:Body><insertResponse><sys_id>fa648f5f0a0a0b2b0048e7012448b8f1</sys_id><table>incident</table><display_name>number</display_name><display_value>INC10014</display_value><status>inserted</status></insertResponse></SOAP-ENV:Body></SOAP-ENV:Envelope>
```

<table id="table_u2b_4bz_sp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sys\_id

</td><td>

The Sys\_id of the resulting record that was created or modified

</td></tr><tr><td>

table

</td><td>

The table name of the table that was affected. In the case of an Asynchronous call, the table name would be the import set table eg. imp\_notification for the Notifications web service import set table

</td></tr><tr><td>

display\_name

</td><td>

The name of the field that is set as the display field for the record that was created or modified

</td></tr><tr><td>

display\_value

</td><td>

The value of the field designated as the display field. For example, the display field for the Incident table is the Number field and an example value would be INC10001

</td></tr><tr><td>

status

</td><td>

A string value that indicates the action that occurred as a result of the web service invocation, relating to the record defined by the `sys_id` and `table` field values-   inserted - the record was inserted
-   updated - the record was updated
-   ignored - the input was ignored, the record was not updated and no new record was created
-   skipped - the input data was skipped \(similar to ignored\) due to missing coalesce values
-   error - there was an error processing the input

</td></tr><tr><td>

status\_message

</td><td>

This value translates to the value found in the Comment field of the import set row and usually contains information related to the status value eg. "No field values changed" when the status is "ignored' . Setting this value to a customized string value will cause the SOAP response to contain an optional status\_message field to be returned.

</td></tr><tr><td>

error\_message

</td><td>

The message related to a status of error. When an error occurs, setting this value to a customized string value will cause the SOAP response to contain an optional error\_message field to be returned

</td></tr></tbody>
</table>## Tailoring the SOAP Response

It is possible to include information other than the information specified in the WSDL by overwriting the contents of status\_message using the transform script.

**Parent Topic:**[Web service import sets](../concept/c_WebServiceImportSets.md)

