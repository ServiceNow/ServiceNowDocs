---
title: Define Courses of Action
description: Define courses of action to prevent an attack or to respond to an attack that is in progress.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Courses of Action, Threat Entities, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Define Courses of Action

Define courses of action to prevent an attack or to respond to an attack that is in progress.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Threat Intel Library** icon on the workspace.

3.  Go to **Courses of Action** object.

4.  Click **New**.

    **Note:** Whenever you create new object records for observables, indicators, entities or objects a source record is created and a prompt message is displayed that the new object record is created and then the user is redirected to the aggregated record.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |ID|Unique ID for a courses of action to prevent an attack.|
    |Name|Enter a descriptive name for this courses of action.|
    |Description|A description that provides more details and context about the courses of action, potentially including its purpose and its key characteristics.|
    |Action|To capture structured or automated courses of action.|
    |TLP|Traffic Light Protocol \(TLP\) indicates the sensitive information shared with the correct audience. It employs four colors \(White, Green, Amber, and Red\) to indicate different degrees of sensitivity for this attack pattern.|
    |Confidence|Enter the confidence for this courses of action.|
    |Source|Specifies the threat source from which this object record is created.|
    |Revoked|Indicates that the revoked objects are no longer considered valid by the object creator.|

    |Field|Description|
    |-----|-----------|
    |Notes|Add any additional notes for a courses of action.|

<table id="table_ztw_yfb_nyb"><thead><tr><th>

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

Represents the processing status of this object, courses of action.

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

 

</td></tr></tbody>
</table>6.  Click **Save**.

    After you save, a prompt message is displayed indicating that A new observable record is created. Click **Continue** to edit the record and create new relationships.

7.  Click **Continue**.

    **Important:** After you create a new observable record, **Prevent System Updates** check box is displayed.

    Select this check box to prevent any updates from the system after the observable or indicator or STIX objects records are created.

    |Field|Description|
    |-----|-----------|
    |Tags|
    |Select Tags|Select the tags that are associated with an observable.|
    |Add Tags|Add new tags.|
    |Taxonomies|
    |Select Taxonomy|Select a Taxonomy that is associated with an attack pattern.|
    |Add Taxonomy Values|Add Taxonomy values that are associated with an attack pattern.|


## What to do next

Click any of the following related lists to view additional information about objects associated with the courses of action.

|Field|Description|
|-----|-----------|
|External References|Lists external references which refer to non-STIX information. This property is used to provide one or more external object identifiers.|
|Attack Patterns|Lists the attack patterns that help categorize attacks that are associated with this object.|
|Indicators|Lists related Indicators of Compromise \(IoC\) that have been identified by the threat source associated with this object.|
|Malware|Lists malicious code associated with this object.|
|Marketing Definitions|Lists the marketing definitions associated with this object.|
|Observables|Lists the observables associated with this object.|
|Sightings|Lists the sightings associated with this object.|
|Tools|Lists legitimate software that is used by threat actors to perform attacks associated with this object.|
|Vulnerabilities|Lists a weakness or defect in a software or hardware that attackers exploit which is associated with this object.|

**Note:**

1.  You can link and unlink the related records associated with this object. For more information, see [Link Threat Intel Related Records](../task/link-threat-intel-releated-records.md).
2.  The various SDOs within the TI library also contains the potential relationships. To establish a relationships between any two objects, you use the **Potential Relationships** link from the **Threat Intel Library** to confirm the relationships between the objects. For more information, see [Confirm object-object potential relationships](../task/define-object-object-potential-relationships.md).
3.  Also, use the **Related Records** section from the objects form view to confirm the relationships between two Objects using the **Potential Relationships** section available on the form view. For more information on see, [Confirm Potential Relationships from Related Records](../task/confirm-potential-relationships.md).
4.  You can add objects to cases. For more information, see [Add to Case](../task/add-to-case.md).

**Parent Topic:**[Courses of Action](course-of-action.md)

