---
title: Identify the source of the profile
description: Specify the name and source of the profile.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create a profile, Secureworks CTP Ticket Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Identify the source of the profile

Specify the name and source of the profile.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  To create a profile for a ticket in your ServiceNow AI Platform instance, navigate to **Secureworks Ticket Ingestion Integration** &gt; **Secureworks Profiles**.

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

Source

</td><td>

Select the source from where you want to ingest the data.

</td></tr><tr><td>

Order

</td><td>

Default is 100. If you have created multiple profiles, this value provides a run time execution priority when two or more profiles share the same triggering conditions. The lower the order value, higher the priority.

</td></tr><tr><td>

Active

</td><td>

This option is cleared by default. If this option is disabled, the profile is not active.**Note:** You should complete all sections in the profile before making it active.

</td></tr></tbody>
</table>    The following figure is an example of a completed form.

    ![Secureworks CTP: Create Profile: Identify Source](../image/secureworks-create-profile-name.gif)


## What to do next

Map the ticket fields.

