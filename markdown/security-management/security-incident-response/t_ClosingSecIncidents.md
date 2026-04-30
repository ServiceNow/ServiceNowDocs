---
title: Close security incidents
description: When a security incident has transitioned to the Review state, it’s possible to close it and enter an appropriate closure code. Closure codes can be searched on later for ease of location.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Close security incidents

When a security incident has transitioned to the Review state, it’s possible to close it and enter an appropriate closure code. Closure codes can be searched on later for ease of location.

## Before you begin

Role required: sn\_si.write

## About this task

## Procedure

1.  If the security incident you want to close isn’t already open, navigate to **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**, and locate the security incident you want to close.

    **Note:** If there are any [post incident review assessments](t_PerformPostIncidentReview.md) that haven’t been completed for this security incident, the security incident can’t be closed. Return to **Security Incident** &gt; **Post Incident Review** &gt; **All Incomplete Reviews**, locate the reviews that are incomplete, and either ask the reviewers to complete their reviews or cancel the remaining assessments.

2.  Select the **Closure Information** tab and fill in the fields, as appropriate.

<table id="table_vks_thr_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create knowledge article

</td><td>

The option to create a draft knowledge base article that contains the contents of the post incident review.

</td></tr><tr><td>

Close code

</td><td>

The close code that best describes the reason you’re closing this security incident.-   Investigation completed
-   Threat mitigated
-   Patched vulnerability
-   Invalid vulnerability
-   Not resolved
-   False positive


</td></tr><tr><td>

Closed by

</td><td>

Displays the user who closed the security incident after the record is updated.

</td></tr><tr><td>

Closed

</td><td>

Displays the date and time of closure after the record is updated.

</td></tr><tr><td>

Close notes

</td><td>

Additional notes that describe the outcome of closing this security incident.

</td></tr></tbody>
</table>3.  Select **Update**.

4.  The assigned user can manually change the **State** to **Closed**.

    **Note:** To prevent users from modifying attachments on a closed security incident, enable the `sn_si.lock_attachments_on_closure` system property.

    When a parent incident is closed, all response tasks belonging to the child incident are canceled. If there are no other types of tasks, the child incident is also closed.


