---
title: Request exception form for risk reduction
description: The following table shows the fields that you must fill on the Request exception form for risk reduction requests.
locale: en-US
release: yokohama
product: IT Remediation Workspace
classification: it-remediation-workspace
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [IT Remediation Workspace reference information, IT Remediation Workspace, Vulnerability Response Workspaces, Unified Security Exposure Management, Security Operations]
---

# Request exception form for risk reduction

The following table shows the fields that you must fill on the Request exception form for risk reduction requests.

<table id="table_kxh_gh2_4lb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reason

</td><td>

Reason for your exception request. Select Mitigating Control in Place for risk reduction request.To see how to add new reason choices, see [Define policy reason mapping](../../vulnerability-app-vuln-mgmt/task/define-policy-reason-mapping.md).

</td></tr><tr><td>

Request for Deferral

</td><td>

Deffer the record. This field is selected by default.**Note:** This field appears only when the Mitigating Control in Place option is selected in the **Reason** field.

</td></tr><tr><td id="entry-risk-reduction">

Request for Risk Reduction

</td><td>

Enables you to request for the risk score reduction.**Note:** This check box appears only when the Mitigating Control in Place option is selected in the **Reason** field.

</td></tr><tr><td>

Current Risk Rating

</td><td>

Current severity of the risk.**Note:** This field appears only when the **Request for Risk Reduction** check box is selected.

</td></tr><tr><td>

Desired Risk Rating

</td><td>

New risk rating that you want to assign to the record.The highest risk score in this risk rating range is applied to the record when your request is approved.

**Note:** This field appears only when the **Request for Risk Reduction** check box is selected.

</td></tr><tr><td id="entry-select-controls">

Select Compensating Controls

</td><td>

Reason for your request to reduce the risk rating.

</td></tr><tr><td>

Until

</td><td>

Date on which the deferral or risk reduction request expires.When the exception request expires:

-   The record reverts to the Open state.
-   The compensating controls expire.
-   The calculated score will be in place of a reduced score.

</td></tr><tr><td>

Justification notes

</td><td>

Details that are related to the reason why this request is being made.

</td></tr></tbody>
</table>**Related topics**  


[Request risk reduction for a vulnerable item or remediation task](../../vr-vulnerability-manager-workspace/task/request-risk-reduction.md)

