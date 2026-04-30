---
title: Define an Indicator
description: Define an Indicator.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Indicators, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Define an Indicator

Define an Indicator.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Threat Intel Library** &gt; **Indicators**.

2.  Select **Indicator**.

3.  Click **New**.

    **Note:** Whenever you create new object records for observables, indicators, entities or objects a source record is created and a prompt message is displayed that the new object record is created and then the user is redirected to the aggregated record.

4.  On the form, fill in the fields.

<table id="table_hmw_qzm_2yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID

</td><td>

Unique ID of the indicator.

</td></tr><tr><td>

Description

</td><td>

Description of the indicator.

</td></tr><tr><td>

Name

</td><td>

Name of the indicator.

</td></tr><tr><td>

Pattern

</td><td>

The detection pattern for this Indicator may be expressed as a STIX Pattern.

</td></tr><tr><td>

Pattern Type

</td><td>

The pattern language used in this indicator.

</td></tr><tr><td>

Pattern Version

</td><td>

The version of the pattern language that is used for the data in the pattern property which must match the type of pattern data included in the pattern property.

</td></tr><tr><td>

Valid From

</td><td>

The time from which this Indicator is considered a valid indicator of the behaviors it is related or represents.

</td></tr><tr><td>

Valid Until

</td><td>

The time after which this Indicator should no longer be considered a valid indicator of the behaviors it is related to or represents.

</td></tr><tr><td>

IOC Classification

</td><td>

The IOC classification of the indicators.

</td></tr><tr><td>

Indicator Types

</td><td>

Indicates the various categories of the indicator.

</td></tr><tr><td>

Status

</td><td>

Indicates the status of the indicators.

</td></tr><tr><td>

Platforms

</td><td>

Defines the platforms for which this indicator is applicable for.

</td></tr><tr><td>

TLP

</td><td>

Unique value that indicates the Data sensitivity setting per TLP.

</td></tr><tr><td>

Attack Phases

</td><td>

Represents attack phase in a kill chain such as LM, MITRE ATT&amp;CK.

</td></tr><tr><td>

Confidence

</td><td>

Enter the confidence for this indicator record.The confidence property identifies the confidence that the creator has in the correctness of their data. The confidence value MUST be a number in the range of 0-100.

</td></tr><tr><td>

Threat Level

</td><td>

Indicates the threat level of the indicator record.

</td></tr><tr><td>

Expiration Time

</td><td>

Specifies the expiration time of the indicator record.

</td></tr><tr><td>

Threat Severity

</td><td>

Indicates the threat severity of the indicator record.

</td></tr><tr><td>

Usage Categories

</td><td>

Categories that the observable falls under, such as botnet or phishing.

</td></tr><tr><td>

First Seen

</td><td>

The time that this indicator record was first seen performing malicious activities.

</td></tr><tr><td>

Last Seen

</td><td>

The time that this indicator record was last seen performing malicious activities.

</td></tr><tr><td>

Source

</td><td>

Specifies the threat source from which this record is created.

</td></tr><tr><td>

Revoked

</td><td>

Indicates that the revoked objects are no longer considered valid by the object creator.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Notes|Add any additional notes for an indicator.|

<table id="table_qyd_ycy_myb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional Context

</td><td>

Add any additional context for this indicator.

</td></tr><tr><td>

Spec Version

</td><td>

The version of the STIX specification used to represent the indicator.The value of this property must be 2.1 for STIX Objects defined according to this specification.

</td></tr><tr><td>

Lang

</td><td>

This property identifies the language of the text content in this object.

</td></tr><tr><td>

Created

</td><td>

Specifies the time when the indicator is created in system.

</td></tr><tr><td>

Updated

</td><td>

Specifies the time when the indicator is updated in system.

</td></tr><tr><td>

Extensions

</td><td>

Indicates the extensions of indicator.

</td></tr><tr><td>

Processing Status

</td><td>

Represents the processing status of this indicator.

</td></tr></tbody>
</table>5.  Click **Save**.

    After you save, a prompt message is displayed indicating that A new observable record is created. Click **Continue** to edit the record and create new relationships.

6.  Click **Continue**.

    **Important:** After you create a new observable record, **Prevent System Updates** check box is displayed.

    Select this check box to prevent any updates from the system after the observable or indicator or STIX objects records are created.

    |Field|Description|
    |-----|-----------|
    |Tags|
    |Select Tags|Select the tags that are associated with an indicator.|
    |Add Tags|Add new tags.|
    |Taxonomies|
    |Select Taxonomy|Select the Taxonomy that is associated with an indicator.|
    |Add Taxonomy Values|Add the Taxonomy values that are associated with an indicator.|

    |Field|Description|
    |-----|-----------|
    |The source records details for an indicator are displayed, if any.|


## What to do next

You can now click any of the following related lists to view additional information about objects associated with the indicators.

<table id="table_svf_lcn_2yb"><thead><tr><th>

Related List

</th><th>

Description

</th></tr></thead><tbody><tr><td>

MITRE Techniques

</td><td>

Lists the MITRE techniques related to this indicator.

</td></tr><tr><td>

Attack Patterns

</td><td>

Lists the Attack Patterns source that describe the methods that adversaries attempt to compromise targets that are related to this indicator.

</td></tr><tr><td>

Campaigns

</td><td>

Lists the Campaigns Source that describe a set of malicious activities or attacks that occur over time against a specific set of targets that are related to this indicator.

</td></tr><tr><td>

Courses of Action

</td><td>

Lists the courses of action related to this indicator.

</td></tr><tr><td>

Data Sources

</td><td>

Lists the data sources related to this indicator.

</td></tr><tr><td>

Data Components

</td><td>

Lists the data components related to this indicator.

</td></tr><tr><td>

Identities

</td><td>

Lists the identities that are related to this indicator.

</td></tr><tr><td>

Indicators

</td><td>

Lists the indicators that are related to this indicator.**Note:** This section also contains the potential relationships between two indicators. For more information, see [Confirm indicator-indicator potential relationships](define-indicator-indicator-potential-relationships.md)and see [Define indicator-indicator relationships](define-indicator-indicator-relationships.md) for the confirmed relationships between the two observables.

</td></tr><tr><td>

Infrastructure

</td><td>

Lists the Infrastructure Source that describe any systems, software services, and any associated physical or virtual resources intended to support some purpose of an attack that are related to this indicator.

</td></tr><tr><td>

Intrusion Sets

</td><td>

Lists a set of adversarial behaviors and resources with common properties that are related to this indicator.

</td></tr><tr><td>

Locations

</td><td>

Lists the geographical locations associated with the object.

</td></tr><tr><td>

Malware

</td><td>

Lists malware source records that are related to this indicator.

</td></tr><tr><td>

Marking Definitions

</td><td>

Lists the marking definitions associated with this object.

</td></tr><tr><td>

Malware Analysis

</td><td>

Lists the metadata and results of a particular static or dynamic analysis performed on a malware instance associated to this indicator.

</td></tr><tr><td>

Observables

</td><td>

Lists the related observable records that are related to this indicator.

</td></tr><tr><td>

Observed Data

</td><td>

Lists the observed data that are cyber security related entities such as files, systems, and networks and associated with this indicator.

</td></tr><tr><td>

Sightings

</td><td>

Lists sightings source records associated with this object.

</td></tr><tr><td>

Threat Actors

</td><td>

Lists changes associated with the observable.

</td></tr><tr><td>

Threat Events

</td><td>

Lists the event or situation that has the potential for causing undesirable consequences or impact that are associated with the indicator.

</td></tr><tr><td>

Threat Groupings

</td><td>

Lists the threat groupings as objects that have a shared context.

</td></tr><tr><td>

Threat Notes

</td><td>

Lists the threat notes that convey information to provide further context or analysis that are associated with the indicator.

</td></tr><tr><td>

Threat Opinions

</td><td>

Lists the threat opinions as an assessment of the accuracy of the information that are associated with the indicator.

</td></tr><tr><td>

Threat Reports

</td><td>

Lists the threat reports associated with this indicator.

</td></tr><tr><td>

Tools

</td><td>

Lists the tool associated with this object.

</td></tr><tr><td>

Vulnerabilities

</td><td>

If the observable is an IP address, this list shows any resources \(configuration items\) that have a matching IP address.

</td></tr><tr><td>

Related Cases

</td><td>

Lists the related cases that are associated with this indicator.

</td></tr><tr><td>

Related Case Tasks

</td><td>

Lists the related case tasks that are associated with this indicator.

</td></tr><tr><td>

Related Canvases

</td><td>

Lists the related canvases that are associated with this indicator.

</td></tr><tr><td>

Indicators References

</td><td>

List of external references that describes this indicator.

</td></tr></tbody>
</table>**Note:**

1.  You can link and unlink the related records associated with this object. For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md).
2.  Also, from the **Related Records** section, you can confirm the relationships between two Observables using the **Potential Relationships** section available on the **Indicators** form view. For more information on see, [Confirm Potential Relationships from Related Records](confirm-potential-relationships.md).
3.  You can add indicators to cases. For more information, see [Add to Case](add-to-case.md).

**Parent Topic:**[Indicators](../concept/indicator.md)

