---
title: Define Marking Definition
description: Define marking definitions to handle and share the requirements for the data.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Marking Definition, Threat Entities, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Define Marking Definition

Define marking definitions to handle and share the requirements for the data.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Threat Intel Library** icon on the workspace.

3.  Go to **Marking Definition** object.

4.  Click **New**.

    **Note:** Whenever you create new object records for observables, indicators, entities or objects a source record is created and a prompt message is displayed that the new object record is created and then the user is redirected to the aggregated record.

5.  On the form, fill in the fields.

<table id="table_h2f_q5q_myb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID

</td><td>

Unique ID to identify a Marking Definition.

</td></tr><tr><td>

Name

</td><td>

A name used to identify the Marking Definition.

</td></tr><tr><td>

Definition Type

</td><td>

The type property identifies the type of object. The definition\_type property identifies the type of Marking Definition.

</td></tr><tr><td>

Definition

</td><td>

The definition property contains the marking object itself, for example TLP.

</td></tr><tr><td>

TLP

</td><td>

TLP is used to ensure that sensitive information is shared with the appropriate audience. It employs four colors \(White, Green, Amber, and Red\) to indicate different degrees of sensitivity.

</td></tr><tr><td>

Confidence

</td><td>

Enter the confidence for this object.The confidence property identifies the confidence that the creator has in the correctness of their data. The confidence value MUST be a number in the range of 0-100.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Notes|Add any additional notes for this Marking Definition.|

<table id="table_ytw_tcd_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional Context

</td><td>

Add any additional context for this Marking Definition.

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
    |Select Tags|Select the tags that are associated with the vulnerability.|
    |Add Tags|Add new tags.|
    |Taxonomies|
    |Select Taxonomy|Select a Taxonomy that is associated with this vulnerability.|
    |Add Taxonomy Values|Add Taxonomy values that are associated with this vulnerability.|


## What to do next

Click any of the following related lists to view additional information about objects associated with the vulnerability.

|Field|Description|
|-----|-----------|
|External References|Lists the external references which refer to non-STIX information. This property is used to provide one or more external object identifiers.|
|Attack Patterns|Lists the attack patterns associated with this object.|
|Campaigns|Lists the campaigns associated with this object.|
|Detections and Mitigations|Lists the detections and mitigations associated with this object.|
|Identities|Lists the identities associated with this object.|
|Indicators|Lists the related Indicators of Compromise \(IoC\) that have been identified by the threat source associated with this object.|
|Infrastructure|Lists systems, software services, and any associated physical or virtual resources that are associated with this object.|
|Intrusion Sets|Lists a set of adversarial behaviors and resources with common properties associated with this object.|
|Locations|Lists the locations that provide geographic context to this object.|
|Malware|Lists the malicious code associated with this object.|
|Malware Analysis|Lists the malicious analysis associated with this object.|
|Observables|Lists the observables associated with this object.|
|Observed Data|Lists the observed data associated with this object.|
|Threat Actors|Lists the individuals, groups, or organizations who act with malicious intent associated with this object.|
|Threat Events|Lists the Threat Events associated with this object.|
|Threat Groupings|Lists the Threat Groupings associated with this object.|
|Threat Notes|Lists the Threat Notes associated with this object.|
|Threat Opinions|Lists the Threat Opinions associated with this object.|
|Tools|Lists the Tools associated with this object.|
|Vulnerabilities|Lists the Vulnerabilities associated with this object.|

**Note:**

1.  You can link and unlink the related records associated with this object. For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md).
2.  The various SDOs within the TI library also contains the potential relationships. To establish a relationships between any two objects, you use the **Potential Relationships** link from the **Threat Intel Library** to confirm the relationships between the objects. For more information, see [Confirm object-object potential relationships](define-object-object-potential-relationships.md).
3.  Also, use the **Related Records** section from the objects form view to confirm the relationships between two Objects using the **Potential Relationships** section available on the form view. For more information on see, [Confirm Potential Relationships from Related Records](confirm-potential-relationships.md).
4.  You can add objects to cases. For more information, see [Add to Case](add-to-case.md).

**Parent Topic:**[Marking Definition](../concept/marking-definition.md)

