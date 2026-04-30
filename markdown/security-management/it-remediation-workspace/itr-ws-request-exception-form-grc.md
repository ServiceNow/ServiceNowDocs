---
title: Request exception form fields for policy exceptions
description: The following table shows the fields that you must fill on the Request exception form for policy exceptions.
locale: en-US
release: yokohama
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [IT Remediation Workspace reference information, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Request exception form fields for policy exceptions

The following table shows the fields that you must fill on the Request exception form for policy exceptions.

<table id="table_fml_xt3_fwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy

</td><td>

Vulnerability Management policy that you’re requesting an exception for.

</td></tr><tr><td>

Control objective

</td><td>

Control objectives associated with the policy that you selected. If a policy isn’t selected, all the control objectives are listed.

</td></tr><tr><td>

Valid from

</td><td>

Date when the exception starts. The default value is the current date. This date can't be in the past.

</td></tr><tr><td>

Valid until

</td><td>

Date that the policy exception expires and the state of the vulnerable item or group changes from Deferred to Open.**Note:** The number of days that the policy exception is valid can't exceed the value in the **Maximum exception duration \(days\)** field that you set for the policy. For more information, see [Create a policy](https://www.servicenow.com/docs/access?context=t_DefineAPolicy&version=yokohama&pubname=yokohama-governance-risk-compliance&ft:locale=en-US).

</td></tr><tr><td>

Reason

</td><td>

Reason for requesting an exception.

</td></tr><tr><td>

Justification

</td><td>

Details related to the reason this exception is being requested. This field must be filled in by the remediation owner.

</td></tr></tbody>
</table>**Related topics**  


[Request an exception using GRC: Policy and Compliance Management in the IT Remediation Workspace](../../vulnerability-response/task/vr-ws-request-exception-grc.md)

