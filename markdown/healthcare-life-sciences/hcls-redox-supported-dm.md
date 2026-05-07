---
title: Supported data models and event types for Redox Inbound Integration
description: In the Redox engine, a request is determined by the event type and workflow set up for your integration.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Redox Inbound Integration, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Supported data models and event types for Redox Inbound Integration

In the Redox engine, a request is determined by the event type and workflow set up for your integration.

**Important:**

Starting with the Yokohama release, Redox Inbound Integration is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

The following table shows a list of event types in the Redox data models that are supported by the Redox Inbound Integration application.

<table id="table_bvp_5jk_ctb"><thead><tr><th>

Data model

</th><th>

Event type

</th></tr></thead><tbody><tr><td rowspan="2">

Clinical Summary

</td><td>

Patient Push

</td></tr><tr><td>

Visit Push

</td></tr><tr><td rowspan="2">

Claim

</td><td>

Submission

</td></tr><tr><td>

Payment

</td></tr><tr><td rowspan="4">

Provider

</td><td>

New

</td></tr><tr><td>

Update

</td></tr><tr><td>

Activate

</td></tr><tr><td>

Deactivate

</td></tr><tr><td rowspan="4">

Medications

</td><td>

Administration

</td></tr><tr><td>

New

</td></tr><tr><td>

Update

</td></tr><tr><td>

Cancel

</td></tr><tr><td rowspan="7">

PatientAdmin

</td><td>

NewPatient

</td></tr><tr><td>

PatientUpdate

</td></tr><tr><td>

Arrival

</td></tr><tr><td>

Cancel

</td></tr><tr><td>

Discharge

</td></tr><tr><td>

PreAdmit

</td></tr><tr><td>

Registration

</td></tr><tr><td rowspan="5">

Scheduling

</td><td>

New

</td></tr><tr><td>

Reschedule

</td></tr><tr><td>

Modification

</td></tr><tr><td>

Cancel

</td></tr><tr><td>

NoShow

</td></tr><tr><td rowspan="5">

SurgicalScheduling

</td><td>

New

</td></tr><tr><td>

Reschedule

</td></tr><tr><td>

Modification

</td></tr><tr><td>

Cancel

</td></tr><tr><td>

NoShow

</td></tr></tbody>
</table>For information on the Redox data models, see [Event types for data models](https://docs.redoxengine.com/basics/redox-data-model-api/event-types-for-data-models) in [Redox documentation](https://docs.redoxengine.com/).

**Parent Topic:**[Redox Inbound Integration reference](hcls-redox-app-reference.md)

