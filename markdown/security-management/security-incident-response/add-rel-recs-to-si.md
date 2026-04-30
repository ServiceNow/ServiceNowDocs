---
title: Add related problems, changes, and incidents to a security incident
description: You can add related records, such as problems, changes, and incidents to existing security incidents.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Add information to a security incident, Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add related problems, changes, and incidents to a security incident

You can add related records, such as problems, changes, and incidents to existing security incidents.

## Before you begin

Role required: sn\_si.basic

## Procedure

1.  If it is not already open, open the security incident you want to update.

2.  Click the **Related Records** tab.

3.  Fill in the fields, as needed.

<table id="table_l2p_dcs_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Problem

</td><td>

Select a Problem \(PRB\) record that resolves the underlying issue that caused this security incident to be created. The PRBs for this incident are typically created by right-clicking in the security incident form header and selecting **Create Problem**.

</td></tr><tr><td>

Parent

</td><td>

Select a task record related to the underlying issue that caused this security incident to be created.

</td></tr><tr><td>

Parent security incident

</td><td>

Select a security incident record related to the underlying issue that caused this security incident to be created. See [Parent and child security incident relationships](../concept/c_ParentChildRelationships.md).

</td></tr><tr><td>

Incident

</td><td>

Select an Incident \(INC\) record that resolves the underlying issue that caused this security incident to be created. The incident is typically created by right-clicking in the security incident form header and selecting **Create Incident**.

</td></tr><tr><td>

Change request

</td><td>

Select a Change Request \(CHG\) record that resolves the underlying issue that caused this security incident to be created. The change request is typically created by right-clicking in the security incident form header and selecting **Create Change**.

</td></tr></tbody>
</table>4.  Click any of the following tabs to further update the security incident:

    -   [Incident Details](add_inc_details_to_si.md)
    -   [Post Incident Review](../concept/c_PostIncidentReview.md)
    -   [Closure Information](add-closure-info-to-si.md)
5.  When you have completed your entries, click **Submit**.


