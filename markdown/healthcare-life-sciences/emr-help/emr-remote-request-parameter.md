---
title: Remote request parameter table
description: The Remote Request Parameter \[sn\_ind\_rmt\_help\_request\_param\] table stores all parameters that can be used across all remote request definitions.
locale: en-US
release: xanadu
product: EMR Help
classification: emr-help
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [EMR Help data model tables, EMR Help reference, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Remote request parameter table

The Remote Request Parameter \[sn\_ind\_rmt\_help\_request\_param\] table stores all parameters that can be used across all remote request definitions.

## Remote Request Parameter table

The Remote Request Parameter \[sn\_ind\_rmt\_help\_request\_param\] table has the following features:

-   Extends the Application File \[sys\_metadata\] table that uses the update\_synch dictionary attribute to enable customizations. For more information, see [Customizations tracked by update sets](https://www.servicenow.com/docs/access?context=customizations-tracked-update-sets&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).
-   Models a request parameter originating from an EMR system.

Role required to configure the table: sn\_ind\_rmt\_help.admin.

<table id="table_k4j_nvy_11c"><thead><tr><th>

Field

</th><th>

Data type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

True/False

</td><td>

Sets the parameter as active to be used in a request definition.

</td></tr><tr><td>

Domain

</td><td>

Domain ID

</td><td>

The domain associated with this record.

</td></tr><tr><td>

ID

</td><td>

String

</td><td>

Unique identifier for this parameter that is utilized in a request definition.

</td></tr><tr><td>

Name

</td><td>

String

</td><td>

Name of this remote request parameter.

</td></tr><tr><td>

Sensitive Data

</td><td>

True/False

</td><td>

Used to classify whether the information received by this parameter is sensitive or not.

 **Note:** Fields marked as true should only be mapped to data columns that have column level encryption enabled. To learn more bout column level encryption, see:

</td></tr><tr><td>

Source system

</td><td>

String

</td><td>

Represents the EMR system that this parameter supports. To support all EMR systems, set this field to **any**.

</td></tr></tbody>
</table>**Parent Topic:**[EMR Help data model tables](tables-installed-with-emr-help.md)

