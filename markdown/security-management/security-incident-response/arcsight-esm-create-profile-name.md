---
title: Create and name the profile for ArcSight ESM event ingestion integration
description: You can set up a profile to ingest correlation events.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Set up instance, ArcSight ESM Event Ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create and name the profile for ArcSight ESM event ingestion integration

You can set up a profile to ingest correlation events.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  To create an event profile for a correlation event in your ServiceNow AI Platform instance, navigate to **ArcSight ESM Integration** &gt; **ArcSight ESM Event Profile**.

2.  Click **New**.

3.  Fill in the fields.

    An example of a completed form follows the table.

<table id="choicetable_k3k_1y3_hcc"><thead><tr><th align="left" id="d160972e99">

Field

</th><th align="left" id="d160972e102">

Description

</th></tr></thead><tbody><tr><td id="d160972e108">

**Name**

</td><td>

Unique name for the profile. If names are not unique, an error will be displayed and duplicate profile names are not saved. Profile names in your ServiceNow AI Platform instance must be unique.

</td></tr><tr><td id="d160972e122">

**Active**

</td><td>

heck box is cleared by default. If this option is disabled, the profile is not active and ingestion will not take place. **Note:** You should complete all sections in the profile before making it active.

</td></tr><tr><td id="d160972e133">

**ArcSight Source**

</td><td>

The ArcSight ESM server configured during the initial authentication step. If you have multiple ArcSight ESM servers configured, select the appropriate server for the correlation event types that will be ingested for the profile. You are required to select a value.

</td></tr><tr><td id="d160972e148">

**Query Viewer ID**

</td><td>

Enter the Resource ID of the configured Query Viewer in the ArcSight ESM Console. The Resource ID is a unique identifier for any Query Viewer configured in the ArcSight ESM server. Once the Resource ID is submitted, the name of the Query View will be returned to ensure that the right Query Viewer has been selected. See the section below for screen shot view of how to determine the Resource ID for the selected Query Viewer in ArcSight ESM.

</td></tr><tr><td id="d160972e164">

**Order**

</td><td>

Default is 100. If you have created multiple profiles, this value provides a run time execution priority when two or more profiles share the same triggering conditions. The workflow in the profile with the lowest number has the highest priority.

</td></tr><tr><td id="d160972e175">

**\(Optional\) Description**

</td><td>

Additional text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>    The following figure is an example of a completed form.

    ![ArcSight Event Profile: Name](../image/sir-arcsight-esm-profile-name.png)

    After you have entered the profile details, click **Continue**. The Query Viewer ID is validated and if a corresponding Resource ID is present in the ArcSight ESM Query Viewer, the name of the Query Viewer will be returned as shown below. If the validation fails, check if the Resource ID exists in the ArcSight ESM console. If the Resource ID is not found, find the correct Resource ID and enter it in the profile.

    ![ArcSight Query Viewer](../image/sir-arcsight-query-viewer.png)


## What to do next

The next step is to select the correlation event types for ingestion from the Query Viewer that was selected in the prior step.

