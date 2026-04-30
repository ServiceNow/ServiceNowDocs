---
title: Define Intrusion Set
description: Define an intrusion set that is a grouped set of adversarial behaviors and resources with common properties.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Intrusion Set, Threat Entities, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Define Intrusion Set

Define an intrusion set that is a grouped set of adversarial behaviors and resources with common properties.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Threat Intel Library** icon on the workspace.

3.  Go to **Intrusion Set**.

4.  Click **New**.

    **Note:** Whenever you create new object records for observables, indicators, entities or objects a source record is created and a prompt message is displayed that the new object record is created and then the user is redirected to the aggregated record.

5.  On the form, fill in the fields.

<table id="table_wtw_tcd_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID

</td><td>

Unique ID for an intrusion set.

</td></tr><tr><td>

Name

</td><td>

Enter a descriptive name for this intrusion set.When referring to a specific entity \(an individual or organization\), this property must contain the canonical name of the specific entity.

</td></tr><tr><td>

Description

</td><td>

A description that provides more details and context about the intrusion set, potentially including its purpose and its key characteristics.

</td></tr><tr><td>

Aliases

</td><td>

Alternative names to identify this intrusion set.**Note:** To add new alias which is not existing in the application click on the **Add New Aliases** icon which is available within the Alias field itself.

</td></tr><tr><td>

Goals

</td><td>

The high-level goals of this Intrusion Set, namely, what are they trying to do.For example, they may be motivated by personal gain, but their goal is to steal credit card numbers. To do this, they may execute specific Campaigns that have detailed objectives like compromising point of sale systems at a large retailer.

</td></tr><tr><td>

First Seen

</td><td>

The time that this intrusion set was first seen performing malicious activities.

</td></tr><tr><td>

Last Seen

</td><td>

The time that this intrusion set was last seen performing malicious activities.

</td></tr><tr><td>

Primary Motivation

</td><td>

The primary reason, motivation, or purpose behind this Intrusion Set. The motivation is why the Intrusion Set wishes to achieve the goal \(what they are trying to achieve\).

</td></tr><tr><td>

Secondary Motivations

</td><td>

The secondary reasons, motivations, or purposes behind this Intrusion Set. These motivations can exist as an equal or near-equal cause to the primary motivation. However, it does not replace or necessarily magnify the primary motivation, but it might indicate additional context. The position in the list has no significance.

</td></tr><tr><td>

Resource Level

</td><td>

This property specifies the organizational level at which this Intrusion Set typically works, which in turn determines the resources available to this Intrusion Set for use in an attack.

</td></tr><tr><td>

TLP

</td><td>

TLP is used to ensure that sensitive information is shared with the appropriate audience. It employs four colors \(White, Green, Amber, and Red\) to indicate different degrees of sensitivity.

</td></tr><tr><td>

Confidence

</td><td>

Enter the confidence for this intrusion set.

</td></tr><tr><td>

Source

</td><td>

Specifies the threat source from which this object record is created.

</td></tr><tr><td>

Revoked

</td><td>

Indicates that the revoked objects are no longer considered valid by the object creator.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Notes|Add any additional notes for this intrusion set.|

<table id="table_ytw_tcd_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional Context

</td><td>

Add any additional context for this intrusion set.

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

Specifies the time when the record is created in the source.

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

Specifies the time when the record is created in the source.

</td></tr><tr><td>

Updated

</td><td>

Specifies the time when the record is modified in the source.

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
    |Select Tags|Select the tags that are associated with the intrusion set.|
    |Add Tags|Add new tags.|
    |Taxonomies|
    |Select Taxonomy|Select a Taxonomy that is associated with this intrusion set.|
    |Add Taxonomy Values|Add Taxonomy values that are associated with this intrusion set.|


## What to do next

Click any of the following related lists to view additional information about objects associated with the intrusion set.

|Field|Description|
|-----|-----------|
|External References|Lists the external references which refer to non-STIX information. This property is used to provide one or more external object identifiers.|
|Attack Patterns|Lists the attack patterns that help categorize attacks that are associated with this object.|
|Campaigns|Lists the campaigns associated with this object.|
|Identities|List of identities associated with this object.|
|Indicators|Lists the related Indicators of Compromise \(IoC\) that have been identified by the threat source associated with this object.|
|Infrastructure|Lists systems, software services, and any associated physical or virtual resources that are associated with this object.|
|Locations|Lists the locations that provide geographic context to this object.|
|Malware|Lists the malicious code associated with this object.|
|Marketing Definitions|Lists the marketing definitions associated with this object.|
|Sightings|Lists the sightings associated with this object.|
|Threat Actors|Lists the individuals, groups, or organizations who act with malicious intent associated with this object.|
|Tools|Lists legitimate software that is used by threat actors to perform attacks associated with this object.|
|Vulnerabilities|Lists a weakness or defect in a software or hardware that attackers exploit which is associated with this object.|

**Note:**

1.  You can link and unlink the related records associated with this object. For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md).
2.  The various SDOs within the TI library also contains the potential relationships. To establish a relationships between any two objects, you use the **Potential Relationships** link from the **Threat Intel Library** to confirm the relationships between the objects. For more information, see [Confirm object-object potential relationships](define-object-object-potential-relationships.md).
3.  Also, use the **Related Records** section from the objects form view to confirm the relationships between two Objects using the **Potential Relationships** section available on the form view. For more information on see, [Confirm Potential Relationships from Related Records](confirm-potential-relationships.md).
4.  You can add objects to cases. For more information, see [Add to Case](add-to-case.md).

**Parent Topic:**[Intrusion Set](../concept/intrusion-set.md)

