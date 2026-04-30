---
title: Define Data Component
description: Define a data component to identify the properties or values of a data source
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Data Component, Other Objects, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Define Data Component

Define a data component to identify the properties or values of a data source

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Threat Intel Library** icon on the workspace.

3.  Go to **Data Component** object.

4.  Click **New**.

    **Note:** Whenever you create new object records for observables, indicators, entities or objects a source record is created and a prompt message is displayed that the new object record is created and then the user is redirected to the aggregated record.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |ID|Unique ID to identify a Data Component.|
    |Name|A name used to identify the Data Component.|
    |Description|A description that provides more details and context about the vulnerability, potentially including its purpose and its key characteristics.|
    |Data Source|Indicates the normalized degree of severity of this vulnerability|
    |TLP|TLP is used to ensure that sensitive information is shared with the appropriate audience. It employs four colors \(White, Green, Amber, and Red\) to indicate different degrees of sensitivity.|
    |Source|Specifies the threat source from which this object record is created.|
    |Confidence|Indicates the confidence for this object. The confidence must be between 0-100.|
    |Revoked|Indicates that the revoked objects are no longer considered valid by the object creator.|

    |Field|Description|
    |-----|-----------|
    |Notes|Add any additional notes for this Data Component.|

<table id="table_ytw_tcd_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional Context

</td><td>

Add any additional context for this Data Component.

</td></tr><tr><td>

Spec Version

</td><td>

The version of the STIX specification used to represent this object.The value of this property must be 2.1 for STIX Objects defined according to this specification.

</td></tr><tr><td>

Lang

</td><td>

This property identifies the language of the text content in this object.

</td></tr><tr><td>

Created Time In Source

</td><td>

Specifies the time the object is created in the source.

</td></tr><tr><td>

Extensions

</td><td>

Indicates the extensions of Data Component.

</td></tr><tr><td>

Modified Time in Source

</td><td>

Specifies the time the object is modified in the source.

</td></tr><tr><td>

Processing Status

</td><td>

Represents the processing status of this object, course of action.

</td></tr><tr><td>

Created

</td><td>

Specifies the date and time when the object is created in the source.

</td></tr><tr><td>

Updated

</td><td>

Specifies the date and time when the object was updated in the source.

</td></tr><tr><td>

Created By Ref

</td><td>

This property specifies that the identity object that describes the entity had created this object.

</td></tr></tbody>
</table>6.  Click **Save**.

    After you save, a prompt message is displayed indicating that A new observable record is created. Click **Continue** to edit the record and create new relationships.

7.  Click **Continue**.

    **Important:** After you create a new observable record, **Prevent System Updates** check box is displayed.

    Select this check box to prevent any updates from the system after the observable or indicator or STIX objects records are created.

    |Field|Description|
    |-----|-----------|
    |Tags|
    |Select Tags|Select the tags that are associated with the vulnerability.|
    |Add Tags|Add new tags.|
    |Taxonomies|
    |Select Taxonomy|Select a Taxonomy that is associated with this vulnerability.|
    |Add Taxonomy Values|Add Taxonomy values that are associated with this vulnerability.|


## What to do next

Click any of the following related lists to view additional information about objects associated with the Data Component.

|Field|Description|
|-----|-----------|
|Attack Patterns|Lists the attack patterns associated with this object.|

**Note:**

1.  You can link and unlink the related records associated with this object. For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md).
2.  The various SDOs within the TI library also contains the potential relationships. To establish a relationships between any two objects, you use the **Potential Relationships** link from the **Threat Intel Library** to confirm the relationships between the objects. For more information, see [Confirm object-object potential relationships](define-object-object-potential-relationships.md).
3.  Also, use the **Related Records** section from the objects form view to confirm the relationships between two Objects using the **Potential Relationships** section available on the form view. For more information on see, [Confirm Potential Relationships from Related Records](confirm-potential-relationships.md).
4.  You can add objects to cases. For more information, see [Add to Case](add-to-case.md).

**Parent Topic:**[Data Component](../concept/data-component.md)

