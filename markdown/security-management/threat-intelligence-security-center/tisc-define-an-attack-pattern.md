---
title: Define an attack pattern
description: Define an attack pattern to help threat analysts categorize the attacks.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Attack Patterns, Threat Entities, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Define an attack pattern

Define an attack pattern to help threat analysts categorize the attacks.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Threat Intel Library** icon on the workspace.

3.  Go to **Attack Pattern**.

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

Unique ID for an attack pattern.

</td></tr><tr><td>

Name

</td><td>

Enter a name for this attack pattern.

</td></tr><tr><td>

Description

</td><td>

Enter a description for an attack pattern.

</td></tr><tr><td>

Aliases

</td><td>

Alternative names to identify this attack pattern.**Note:** To add new alias which is not existing in the application click on the **Add New Aliases** icon which is available within the Alias field itself.

</td></tr><tr><td>

Attack Phase

</td><td>

Represents attack phase in a kill chain such as LM, MITRE ATT&amp;CK.

</td></tr><tr><td>

Permissions Required

</td><td>

Select the required permissions for this attack pattern.

</td></tr><tr><td>

TLP

</td><td>

TLP is used to ensure that sensitive information is shared with the appropriate audience. It employs four colors \(White, Green, Amber, and Red\) to indicate different degrees of sensitivity.

</td></tr><tr><td>

Confidence

</td><td>

Enter the confidence for this attack pattern mode.The confidence property identifies the confidence that the creator has in the correctness of their data. The confidence value MUST be a number in the range of 0-100.

</td></tr><tr><td>

Source

</td><td>

Specifies the threat source from which this object record is created.

</td></tr><tr><td>

Revoked

</td><td>

Indicates that the revoked objects are no longer considered valid by the object creator.

</td></tr><tr><td>

Prevent System Updates

</td><td>

Setting this flag to true will prevent system from overriding values of fields on record.

</td></tr></tbody>
</table>    **Important:** After you create a new object record, **Prevent System Updates** check box is displayed.

    Select this check box to prevent any updates from the system after the observable or indicator or STIX objects records are created.

    |Field|Description|
    |-----|-----------|
    |Notes|Add any additional notes for an attack pattern.|

<table id="table_qyd_ycy_myb"><thead><tr><th>

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

The version of the STIX specification used to represent this object, attack pattern.The value of this property must be 2.1 for STIX Objects defined according to this specification.

</td></tr><tr><td>

Lang

</td><td>

This property identifies the language of the text content in this object.

</td></tr><tr><td>

Created

</td><td>

Specifies the time when the record is created in the system.

</td></tr><tr><td>

Updated

</td><td>

Specifies the time when the record is modified in the system.

</td></tr><tr><td>

Extensions

</td><td>

Indicates the extensions of attack pattern.

</td></tr><tr><td>

Processing Status

</td><td>

Represents the processing status of this object, attack pattern.

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

You can now click any of the following related lists to view additional information about objects associated with the attack pattern.

|Field|Description|
|-----|-----------|
|External References|Lists external references which refer to non-STIX information. This property is used to provide one or more external object identifiers.|
|Campaigns|Lists campaigns associated with this object.|
|Identities|List of identities associated with this object.|
|Indicators|Lists related Indicators of Compromise \(IoC\) that have been identified by the threat source associated with this object.|
|Intrusion Set|Lists a set of adversarial behaviors and resources with common properties associated with this object.|
|Locations|Lists locations that provide geographic context to this object.|
|Malware|Lists malicious code associated with this object.|
|Threat Actors|Lists individuals, groups, or organizations who act with malicious intent associated with this object.|
|Tools|Lists legitimate software that is used by threat actors to perform attacks associated with this object.|
|Vulnerabilities|Lists a weakness or defect in a software or hardware that attackers exploit which is associated with this object.|

**Note:**

1.  You can link and unlink the related records associated with this object. For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md).
2.  The various SDOs within the TI library also contains the potential relationships. To establish a relationships between any two objects, you use the **Potential Relationships** link from the **Threat Intel Library** to confirm the relationships between the objects. For more information, see [Confirm object-object potential relationships](define-object-object-potential-relationships.md).
3.  Also, use the **Related Records** section from the objects form view to confirm the relationships between two Objects using the **Potential Relationships** section available on the form view. For more information on see, [Confirm Potential Relationships from Related Records](confirm-potential-relationships.md).
4.  You can add objects to cases. For more information, see [Add to Case](add-to-case.md).

**Parent Topic:**[Attack Patterns](../concept/tisc-attack-patterns.md)

