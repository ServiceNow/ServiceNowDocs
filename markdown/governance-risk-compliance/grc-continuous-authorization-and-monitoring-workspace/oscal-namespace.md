---
title: OSCAL namespace
description: To include CAM specific information, custom properties with a unique namespace are used to add impact and tailor the content as needed.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CAM OSCAL, CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# OSCAL namespace

To include CAM specific information, custom properties with a unique namespace are used to add impact and tailor the content as needed.

<table id="table_s4j_5vv_12c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

impact

</td><td>

Captures control objective impact.

</td></tr><tr><td>

justification

</td><td>

Justification for making baseline control not applicable. Present only when a baseline control is made not applicable.

</td></tr><tr><td>

source

</td><td>

Source of baseline control objective.

</td></tr><tr><td>

active

</td><td>

Indicates whether a control objective is active.

</td></tr><tr><td>

behavior

</td><td>

Comparing the control objective reference in the policy with those in the baseline controls.For matching records \(same reference ID as in the baseline controls\):

-   Override: Replaces the baseline control objective with the one from the selected policy.
-   Move to N/A: Moves the control objective with the matching reference ID to the Not Applicable state.
-   Skip: Ignores the matching record; no changes will be made to the Authorization Package from the selected policy.

For distinct records \(reference ID does not exist in baseline controls\):

-   Create new: Adds the new control objective from the selected policy to the Authorization Package.
-   Skip: Ignores the distinct record; it will not be added to the Authorization Package.

For more information, see [View package details in CAM Workspace](../task/auth-package-overview-ws.md).

</td></tr><tr><td>

configuration

</td><td>

Applying a policy to the baseline controls using configurations such as Addition, Subtraction, and Custom Action.

</td></tr><tr><td>

action

</td><td>

Combination of behavior and configuration.

</td></tr><tr><td>

order

</td><td>

The order in which you applied the policy.

</td></tr><tr><td>

impact-change-justification

</td><td>

If recommended impact is changed. This property will contain the justification for change.

</td></tr><tr><td>

category

</td><td>

Category of Information type.

</td></tr><tr><td>

sub\_category

</td><td>

Subcategory of information type.

</td></tr><tr><td>

pii-in-identifiable-form

</td><td>

PII information pii-in-identifiable-form.

</td></tr><tr><td>

pii-information-about-public

</td><td>

PII information pii-information-about-public.

</td></tr><tr><td>

privacy-impact-assessment

</td><td>

PII information privacy-impact-assessment.

</td></tr><tr><td>

system-of-records-notice

</td><td>

PII information system-of-records-notice.

</td></tr><tr><td>

privacy-sensitive-system

</td><td>

PII information privacy-sensitive-system.

</td></tr></tbody>
</table>**Parent Topic:**[CAM OSCAL](oscal-cam-ws.md)

