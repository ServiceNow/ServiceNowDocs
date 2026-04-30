---
title: Create profiles for ingesting IBM QRadar offenses
description: You can set up a profile to ingest offenses.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a profile for IBM QRadar offense ingestion integration, Set up your ServiceNow AI Platform instance for the IBM QRadar offense ingestion integration, IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create profiles for ingesting IBM QRadar offenses

You can set up a profile to ingest offenses.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  To create a profile for an offense in your ServiceNow AI Platform instance, navigate to **IBM QRadar Integration** &gt; **IBM QRadar Profile**.

2.  Click **New**.

3.  Fill in the fields.

    An example of a completed form follows the table.

<table id="simpletable_jwn_5jj_nkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the profile. If names are not unique, an error will be displayed and duplicate profile names are not saved. Profile names in your ServiceNow AI Platform instance must be unique.

</td></tr><tr><td>

Active

</td><td>

Check box is cleared by default. If this option is disabled, the profile is not active and ingestion will not take place. **Note:** You should complete all sections in the profile before making it active.

</td></tr><tr><td>

Source

</td><td>

The IBM QRadar server that you configured to ingest offenses. If you have multiple IBM QRadar servers configured, select the appropriate server for the offense types that will be ingested for the profile. You are required to enter a value.

</td></tr><tr><td>

Order

</td><td>

Default is 100. If you have created multiple profiles, this value provides a run time execution priority when two or more profiles share the same triggering conditions. The workflow in the profile with the lowest number has the highest priority.

</td></tr><tr><td>

\(Optional\) Description

</td><td>

Additional text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>    The following figure is an example of a completed form.

    ![IBM QRadar: Create Profile: Name](../image/ibm-qradar-profile-name.png)


## What to do next

The next step is to select the offenses for ingestion.

