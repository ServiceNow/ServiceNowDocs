---
title: Remote request definition table
description: The Remote Request Definition \[sn\_ind\_rmt\_help\_request\_defn\] table stores the record producer and task type.
locale: en-US
release: yokohama
product: EMR Help
classification: emr-help
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [EMR Help data model tables, EMR Help reference, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Remote request definition table

The Remote Request Definition \[sn\_ind\_rmt\_help\_request\_defn\] table stores the record producer and task type.

## Remote Request Definition table

The Remote Request Definition \[sn\_ind\_rmt\_help\_request\_defn\] table has the following features:

-   Extends the Application File \[sys\_metadata\] table that uses the update\_synch dictionary attribute to enable customizations. For more information, see [Customizations tracked by update sets](https://www.servicenow.com/docs/access?context=customizations-tracked-update-sets&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).
-   Models a request parameter originating from an EMR system.

Role required to configure the table: sn\_ind\_rmt\_help.admin.

<table id="table_k4j_nvy_11c"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Record Producer

</td><td>

Reference

</td><td>

Represents the record producer associated with the remote request definition.

 For more information, see [Create a record producer](https://www.servicenow.com/docs/access?context=t_DefRecProdInSCat&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

</td></tr><tr><td>

Request data table

</td><td>

Table name

</td><td>

The table that stores the values of the EMR session information that was captured when creating the task by the record producer.

</td></tr><tr><td>

Rest API Task Parameters

</td><td>

Field list

</td><td>

Provides the ability to choose fields that you want to make available to the listed API actions. The fields chosen will be available to the rest API operations for the following associated request definition:

1.  Task create
2.  Task list
3.  Task detail
4.  Task update

</td></tr></tbody>
</table>**Parent Topic:**[EMR Help data model tables](tables-installed-with-emr-help.md)

