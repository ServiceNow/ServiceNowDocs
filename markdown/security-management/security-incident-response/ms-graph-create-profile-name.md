---
title: Identify source for the profile
description: Specify the name and source for the profile.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create a profile, Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Identify source for the profile

Specify the name and source for the profile.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  To create a profile for an alert in your ServiceNow AI Platform instance, navigate to **Microsoft Graph Security API Integration** &gt; **Microsoft Graph Security API Profile**.

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

Check box is cleared by default. If this option is disabled, the profile is not active.**Note:** You should complete all sections in the profile before making it active.

</td></tr><tr><td>

Source

</td><td>

The Microsoft Azure tenant that you configured to ingest alerts. If you have multiple tenants configured, select the appropriate tenant for the alert types that you are planning to ingest for the profile. You are required to enter a value.

</td></tr><tr><td>

Order

</td><td>

Default is 100. If you have created multiple profiles, this value provides a run time execution priority when two or more profiles share the same triggering conditions. The lower the order value, higher the priority.

</td></tr><tr><td>

\(Optional\) Description

</td><td>

Additional text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>    The following figure is an example of a completed form.

    ![Microsoft Graph Security API: create profile name](../image/ms-graph-create-profile-1.png)


## What to do next

The next step is to map the alert fields.

