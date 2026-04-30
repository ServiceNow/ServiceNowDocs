---
title: Configure KINEXON integration
description: Configure Contact Tracing and enable the KINEXON SafeZone tracing system to use data from KINEXON wearable devices in diagnostic requests. This data enables the identification of potentially exposed contacts based on the interactions and proximity of users with KINEXON wearable devices.
locale: en-US
release: zurich
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Setting up Contact Tracing, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Configure KINEXON integration

Configure Contact Tracing and enable the KINEXON SafeZone tracing system to use data from KINEXON wearable devices in diagnostic requests. This data enables the identification of potentially exposed contacts based on the interactions and proximity of users with KINEXON wearable devices.

## Before you begin

To successfully enable the KINEXON SafeZone tracing system, note the following requirements:

-   The Emergency Outreach application must be installed. For more information, see [Install Emergency Outreach](../../business-continuity/task/install-emergency-outreach.md#).
-   Privacy consent settings for Contact Tracing must be configured. For more information, see [Setting up data privacy consent settings for Contact Tracing](../concept/set-up-privacy-consent-settings.md).
-   Users must have KINEXON wearable devices managed with KINEXON SafeZone.
-   Users should have an email address in the **Name** column in the KINEXON SafeZone software. Email addresses are used to match KINEXON users to users in Contact Tracing.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Properties**.

2.  Set the Contact Tracing property values related to the KINEXON SafeZone integration.

    |Property|Description|
    |--------|-----------|
    |**sn\_imt\_tracing.kinexon\_api\_endpoint**|API endpoint used to log in to the KINEXON SafeZone instance and access KINEXON data. This API endpoint is also used to fetch information required for Contact Tracing. Replace the default endpoint with the endpoint of your instance.|
    |**sn\_imt\_tracing.kinexon\_api\_username**|KINEXON administrator user name.|
    |**sn\_imt\_tracing.kinexon\_api\_password**|KINEXON administrator password.|
    |**sn\_imt\_tracing.kinexon\_api\_param\_min\_duration**|The minimum duration of contact \(in seconds\) between two KINEXON sensors required to determine whether a user is a potentially exposed contact. The query omits all records with values below this duration. The default value is `300`.|
    |**sn\_imt\_tracing.kinexon\_api\_param\_min\_acc\_duration**|The minimum total duration \(in seconds\) of all contact between two KINEXON sensors within the queried date range. If the total duration is shorter than this value, the query omits all records of contact between the pair of sensors. The default value is `300`.|
    |**sn\_imt\_tracing.kinexon\_api\_param\_max\_distance**|The maximum distance \(in meters\) between two KINEXON sensors that determines whether users are in contact. The query omits any instances of contact beyond this distance. The default value is `2`.|
    |**sn\_imt\_tracing.kinexon\_api\_param\_max\_time\_gap\_in\_sequence**|Determines the amount of time that can pass \(in seconds\) between any two consecutive instances of contact before the potential exposure is considered two potential exposures. The default value is `15`.|

3.  Navigate to **Emergency Exposure Management** &gt; **Tracing Systems** and click **Kinexon SafeZone**.

4.  Activate the tracing system.

    1.  Select **Active**.

    2.  Click **Update**.

5.  Add all users with KINEXON wearable devices in your organization to the privacy consent audience.

    1.  Navigate to **Emergency Outreach** &gt; **Safe Workplace Audience** and click **privacy audience**.

    2.  Add users to the audience.

        For detailed instructions on adding users to an audience, see [Add a Safe Workplace audience](../../employee-readiness-core/task/add-safe-workplace-audience.md)

    3.  Click **Update**.

6.  Assign the sn\_imt\_core.privacy\_consent\_user role to KINEXON users to enable them to access and complete the privacy consent.

7.  Send your organization's privacy consent outreach to KINEXON users.

    Users in a location that requires privacy consent must consent to the privacy policy to create exposed contact records. Users who do not have an assigned location or are in a location that does not require privacy consent do not have to submit a privacy consent.


## Result

You can now use the KINEXON SafeZone tracing system in diagnostic requests. For more information on identifying potentially exposed contacts using diagnostic requests, see [Identify potentially exposed contacts](identify-exposed-contacts.md).

**Parent Topic:**[Setting up Contact Tracing](../concept/set-up-contact-tracing.md)

