---
title: Define Object Sighting
description: Define object sighting that describes that an object \(malware, tool, threat actor, and so on\) was seen.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Object Sighting, Threat Entities, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Define Object Sighting

Define object sighting that describes that an object \(malware, tool, threat actor, and so on\) was seen.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Threat Intel Library** icon on the workspace.

3.  Go to **Object Sighting** object.

4.  Click **New**.

    **Note:** Whenever you create new object records for observables, indicators, entities or objects a source record is created and a prompt message is displayed that the new object record is created and then the user is redirected to the aggregated record.

5.  On the form, fill in the fields.

<table id="table_y11_b5m_2bc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Entity

</td><td>

Select the entity object sighting record.**Note:** During any new object sighting record creation, an associated relationship record is required for aggregation.

</td></tr><tr><td>

Sighting of

</td><td>

Indicates the that a particular entity or indicator was observed in an environment which can be an indication to a potential threat.**Note:** Select the sighting related record which is associated to the object selected in the Entity field so that related records can now be created and aggregate the sighting records.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |ID|Unique ID for a course of action to prevent an attack.|
    |Description|A description that provides more details and context about the Sighting.|
    |First Seen|The beginning of the time window during which the SDO referenced by which the property was sighted.|
    |Last Seen|The end of the time window during which the SDO referenced by which the property was sighted.|
    |Count|If present, this must be an integer between 0 and 999,999,999 inclusive and represents the number of times the SDO referenced by which the property was sighted.|
    |Is Summary|Indicates whether the Sighting should be considered the summary data. Summary data is an aggregation of previous Sightings reports and should not be considered primary source data.|
    |Is Internal|Indicates whether the Sighting is internal.|
    |TLP|TLP is used to ensure that sensitive information is shared with the appropriate audience. It employs four colors \(White, Green, Amber, and Red\) to indicate different degrees of sensitivity.|
    |Confidence|Enter the confidence for this course of action.|
    |Source|Specifies the threat source from which this object record is created.|
    |Revoked|Indicates that the revoked objects are no longer considered valid by the object creator.|

    |Field|Description|
    |-----|-----------|
    |Notes|Add any additional notes for this intrusion set.|

<table id="table_ytw_tcd_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional Context

</td><td>

Add any additional context for this attack pattern.

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

Indicates the extensions of attack pattern.

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
    |Select Tags|Select the tags that are associated with the identity.|
    |Add Tags|Add new tags.|
    |Taxonomies|
    |Select Taxonomy|Select a Taxonomy that is associated with this infrastructure.|
    |Add Taxonomy Values|Add Taxonomy values that are associated with this infrastructure.|


## What to do next

Click any of the following related lists to view additional information about objects associated with the object sighting.

|Field|Description|
|-----|-----------|
|External References|Lists the external references which refer to non-STIX information. This property is used to provide one or more external object identifiers.|
|Objects|Lists the objects associated with the sightings.|
|Indicators|Lists the related Indicators of Compromise \(IoC\) that have been identified by the threat source associated with this object.|

**Note:**

1.  You can link and unlink the related records associated with this object. For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md).
2.  The various SDOs within the TI library also contains the potential relationships. To establish a relationships between any two objects, you use the **Potential Relationships** link from the **Threat Intel Library** to confirm the relationships between the objects. For more information, see [Confirm object-object potential relationships](define-object-object-potential-relationships.md).
3.  Also, use the **Related Records** section from the objects form view to confirm the relationships between two Objects using the **Potential Relationships** section available on the form view. For more information on see, [Confirm Potential Relationships from Related Records](confirm-potential-relationships.md).
4.  You can add objects to cases. For more information, see [Add to Case](add-to-case.md).

**Parent Topic:**[Object Sighting](../concept/object-sighting.md)

