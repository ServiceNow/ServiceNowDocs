---
title: Define Location
description: Define a geographic location to provide more context to other TISC entities.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Location, Threat Entities, TISC Library Repository, Threat Intelligence Security Center Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Define Location

Define a geographic location to provide more context to other TISC entities.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Threat Intel Library** icon on the workspace.

3.  Go to **Location** object.

4.  Click **New**.

    **Note:** Whenever you create new object records for observables, indicators, entities or objects a source record is created and a prompt message is displayed that the new object record is created and then the user is redirected to the aggregated record.

5.  On the form, fill in the fields

<table id="table_wtw_tcd_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ID

</td><td>

Unique ID for the location.

</td></tr><tr><td>

Name

</td><td>

Enter a descriptive name to identify the location.

</td></tr><tr><td>

Description

</td><td>

A description that provides more details and context about the intrusion set, potentially including its purpose and its key characteristics.

</td></tr><tr><td>

Latitude

</td><td>

The latitude of the Location in decimal degrees. Positive numbers describe latitudes north of the equator, and negative numbers describe latitudes south of the equator.The value of this property must be from -90.0 through 90.0 respectively.

</td></tr><tr><td>

Longitude

</td><td>

The longitude of the location in decimal degrees. Positive numbers describe longitudes east of the prime meridian and negative numbers describe longitudes west of the prime meridian.The value of this property must be from -180.0 through 180.0, inclusive.

</td></tr><tr><td>

Precision

</td><td>

Defines the precision of the coordinates specified by the latitude and longitude properties. This is measured in meters. The actual location may be anywhere up to precision meters from the defined point.If this property is not present, then the precision is unspecified.

If this property is present, the latitude and longitude properties must be present.

</td></tr><tr><td>

Region

</td><td>

The region that this location is in.

</td></tr><tr><td>

Country

</td><td>

The country that this location is in.

</td></tr><tr><td>

Administrative Area

</td><td>

The state, province, or other sub-national administrative area that this location is in.

</td></tr><tr><td>

City

</td><td>

The city that this location is in.

</td></tr><tr><td>

Street Address

</td><td>

The street address that this location describes. This property includes all aspects or parts of the street address.

</td></tr><tr><td>

Postal Code

</td><td>

The postal code that this location is in.

</td></tr><tr><td>

Confidence

</td><td>

Enter the confidence for this course of action.

</td></tr><tr><td>

TLP

</td><td>

TLP is used to ensure that sensitive information is shared with the appropriate audience. It employs four colors \(White, Green, Amber, and Red\) to indicate different degrees of sensitivity.

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
    |Notes|Add any additional notes for this location.|

<table id="table_ytw_tcd_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Additional Context

</td><td>

Add any additional context for this location.

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

Indicates the extensions for this location.

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
    |Select Tags|Select the tags that are associated with the location.|
    |Add Tags|Add new tags.|
    |Taxonomies|
    |Select Taxonomy|Select a Taxonomy that is associated with this location.|
    |Add Taxonomy Values|Add Taxonomy values that are associated with this location.|

8.  If you want to delete any record then, select **Delete** to delete the aggregated record.

    When you select this action, then it will remove all the related records, except the original source data, and trigger re aggregation.

    **Note:** A confirmation message will appear to verify that you want to delete the aggregated record. If you also want to delete the source records and prevent re aggregation, select the **Delete Source Records** check box. This action will remove all the associated source records.


## What to do next

Click any of the following related lists to view additional information about objects associated with the location.

|Field|Description|
|-----|-----------|
|External References|Lists the external references which refer to non-STIX information. This property is used to provide one or more external object identifiers.|
|Attack Patterns|Lists the attack patterns that help categorize attacks that are associated with this object.|
|Campaigns|Lists the campaigns associated with this object.|
|Identities|List of identities associated with this object.|
|Infrastructure|Lists systems, software services, and any associated physical or virtual resources that are associated with this object.|
|Intrusion Sets|Lists a set of adversarial behaviors and resources with common properties associated with this object.|
|Malware|Lists the malicious code associated with this object.|
|Marketing Definitions|Lists the marketing definitions associated with this object.|
|Observables|Lists the observables associated with this object.|
|Sightings|Lists the sightings associated with this object.|
|Threat Actors|Lists the individuals, groups, or organizations who act with malicious intent associated with this object.|
|Tools|Lists legitimate software that is used by threat actors to perform attacks associated with this object.|

**Note:**

1.  You can link and unlink the related records associated with this object. For more information, see [Link Threat Intel Related Records](link-threat-intel-releated-records.md).
2.  The various SDOs within the TI library also contains the potential relationships. To establish a relationships between any two objects, you use the **Potential Relationships** link from the **Threat Intel Library** to confirm the relationships between the objects. For more information, see [Confirm object-object potential relationships](define-object-object-potential-relationships.md).
3.  Also, use the **Related Records** section from the objects form view to confirm the relationships between two Objects using the **Potential Relationships** section available on the form view. For more information on see, [Confirm Potential Relationships from Related Records](confirm-potential-relationships.md).
4.  You can add objects to cases. For more information, see [Add to Case](add-to-case.md).

**Parent Topic:**[Location](../concept/location.md)

