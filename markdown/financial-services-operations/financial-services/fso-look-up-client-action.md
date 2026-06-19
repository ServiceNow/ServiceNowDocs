---
title: FSO Look Up Client action
description: Look up a record from any table based on defined conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/financial-services/fso-look-up-client-action.html
release: zurich
product: Financial Services
classification: financial-services
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Remote Tables, Data Models, Explore, Financial Services Operations \(FSO\)]
---

# FSO Look Up Client action

Look up a record from any table based on defined conditions.

## Roles and availability

Role required: admin

## Fields

When you select the **Action Payload Definition** in the field decorator, it activates a set of **Action Attributes** that you can configure for the **UXF Client**. Following are the list of attributes available for configuration in field decorators.

|Field|Description|
|-----|-----------|
|popupTitle|Sets the title for the pop-up modal.|
|remoteTable|Identifies which remote table to query for the lookup.|
|remoteColumnsToShow|Displays the columns on the list when queried.|
|setFieldNameOnRecordPage|Assigns the selected value to a specified field after selection.|
|localTable|Specifies where to copy the selected record.|
|localRemoteFieldMapping|Maps fields between the remote and local tables for data copying.|
|searchField|Enables you to search the remote table using specified fields in the pop-up.|
|listTitle|Titles the list within the pop-up modal.|

## Output Example

|Field|Description|
|-----|-----------|
|popupTitle|Select account|
|remoteTable|sn\_bom\_remote\_saving\_account|
|localTable|sn\_bom\_saving\_account|
|remoteColumnsToShow|name, product, consumer|
|setFieldNameOnRecordPage|sold\_product|
|localRemoteFieldMapping|\["local":"product","remote":"product","unique":true,"local":"name","remote":"name","unique":true,"local":"consumer","remote":"consumer","unique":true,"local":"status","remote":"status","unique":false,"local":"balance","remote":"balance","unique":false\]|
|searchFields|\["field":"consumer","name":"Consumer","filter":"LIKE","val":"","field":"name","name":"Name","filter":"LIKE","val":""\]|
|listTitle|Select an account|

\[Omitted image "fso-look-up-client-action.png"\] Alt text: Example FSO Look Up Client action.

**Parent Topic:**[Financial Services Remote Tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/financialservices-remote-tables.md)

