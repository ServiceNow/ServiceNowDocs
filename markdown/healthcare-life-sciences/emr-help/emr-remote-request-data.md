---
title: Remote request data table
description: The Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table stores the captured parameter data associated with a task record.
locale: en-US
release: xanadu
product: EMR Help
classification: emr-help
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [EMR Help data model tables, EMR Help reference, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Remote request data table

The Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table stores the captured parameter data associated with a task record.

The Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table has the following features:

-   Stores additional data from an EMR system.
-   Extensible and used for creating data tables based on a task type.

Role required to configure the table: sn\_ind\_rmt\_help.admin.

**Note:** Storing data from the EMR system in the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table or its extended child data table provides a layer of security. As an administrator, you can extend the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table for a particular task type to store additional information from an EMR system. For example, the EMR Help application provides the EMR Request Data \[sn\_ind\_rmt\_help\_incident\_data\] table that extends the Remote Request Data \[sn\_ind\_rmt\_help\_request\_data\] table and associates incidents with service requests.

<table id="table_k4j_nvy_11c"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional info

</td><td>

String

</td><td>

This field is used to store any additional sensitive information when submitting a request from the EMR.

 This field has column-level encryption.

</td></tr><tr><td>

Created

</td><td>

Date/Time

</td><td>

Date and timestamp this record was created.

</td></tr><tr><td>

Created by

</td><td>

String

</td><td>

The name of the user who created this record.

</td></tr><tr><td>

Domain

</td><td>

Domain ID

</td><td>

The domain associated with this record.

</td></tr><tr><td>

Patient ID

</td><td>

String

</td><td>

Represents the unique patient identifier \(ie MRN\) for this patient in the EMR system.

</td></tr><tr><td>

Request Definition

</td><td>

Reference

</td><td>

References the remote request definition.

</td></tr><tr><td>

Source system

</td><td>

String

</td><td>

Represents the EMR system that this request came from. IE, Epic.

 **Note:** If this value is unknown, it means that no source system was provided when the record was created.

</td></tr><tr><td>

Sys ID

</td><td>

Sys ID \(GUID\)

</td><td>

Unique sys\_id every table has.

</td></tr><tr><td>

Tags

</td><td>

Related Tags

</td><td>

Tags related to this record.

</td></tr><tr><td>

Task

</td><td>

Reference

</td><td>

References the associated task.

</td></tr><tr><td>

Task type

</td><td>

Table name

</td><td>

The task type that is configured on the remote request definition that was used to generate this record.

</td></tr><tr><td>

Updated

</td><td>

Date/Time

</td><td>

Stamp of date and time last updated.

</td></tr><tr><td>

Updated by

</td><td>

String

</td><td>

Name of person to last update record.

</td></tr><tr><td>

Updates

</td><td>

Integer

</td><td>

Number of updates that have occurred.

</td></tr></tbody>
</table>**Parent Topic:**[EMR Help data model tables](tables-installed-with-emr-help.md)

