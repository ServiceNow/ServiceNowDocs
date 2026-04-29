---
title: Request an exception for remediation tasks using GRC: Policy and Compliance Management
description: Request policy exceptions using the GRC policy exception management capability in the Policy and Compliance Management application from within Configuration Compliance.
locale: en-US
release: australia
product: Configuration Compliance
classification: configuration-compliance
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Requesting and approving an exception for a remediation task, Use, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Request an exception for remediation tasks using GRC: Policy and Compliance Management

Request policy exceptions using the GRC policy exception management capability in the Policy and Compliance Management application from within Configuration Compliance.

## Before you begin

Before you can use the Policy Exception Integration to request policy exceptions, you must download the GRC: Policy and Compliance Management application from the ServiceNow Store.

Role required: sn\_vulc.remediation\_owner

You can also request exceptions in the classic UI.

## About this task

**Important:** As an admin and a remediation owner, you can request a policy exception for a Remediation Task \(RT\) in the [Vulnerability Manager Workspace](../../vulnerability-response/concept/vr-ws-exceptions-split-VMGR-ws.md) and [IT Remediation Workspace](../../vulnerability-response/task/vr-ws-request-exception-grc.md) respectively.

**Note:** Starting with v14.9 of Configuration Compliance, the following terms have been renamed:

|Terminology prior to v14.9|Terminology v14.9 onwards|
|--------------------------|-------------------------|
|Test Result Group|Remediation Task|
|Group Rules|Remediation Task Rules|
|Policy|Test group|

## Procedure

1.  Navigate to **All** &gt; **Application Vulnerability Response** &gt; **Application Vulnerable Items** \(or **Remediation Tasks**\)&gt;**All**, and open the item or group for which you want to request an exception.

    The selected item or group must be in Open, Under investigation, or Awaiting implementation state.

2.  On the selected form, click **Request Exception**.

3.  If GRC: Policy and Compliance Management is selected in the Exception Management screen, do the following.

    1.  On the form, fill in the fields.

<table id="table_stm_xty_flb"><thead><tr><th>

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

Control objectives that are associated with the policy you selected. If a policy isn’t selected, all the control objectives are listed.

</td></tr><tr><td>

Valid from

</td><td>

Date when the exception will start. The default value is the current date. This date can’t be in the past.

</td></tr><tr><td>

Valid until

</td><td>

Date when the policy exception expires and when the state of the vulnerable item or group changes from Deferred to Open.**Note:** The number of days that the policy exception is valid can’t exceed the **Maximum exception duration \(days\)** that you set for the policy in Policy and Compliance. For more information, see [Create a policy](https://www.servicenow.com/docs/access?context=t_DefineAPolicy&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

</td></tr><tr><td>

Reason

</td><td>

Reason for requesting an exception.

</td></tr><tr><td>

Justification

</td><td>

Details that are related to the reason why this request is being made. This field must be filled in by the remediation owner.

</td></tr></tbody>
</table>    2.  Submit the exception request by clicking **Request Approval**.

        The state of the remediation task changes to In Review and a policy exception is created. Use the **State Change Approval** tab to track the status of the exception request.

    3.  View the policy exception by clicking the Policy Exceptions related list.

    4.  Click the policy exception number.

    5.  In the **Approver** field, select the name of the approver.

    6.  Click the Source tab and select a control objective from the **Control objective** field.

    7.  Click the Risk assessment tab and select the risk rating from the **Risk rating** field.

    8.  Save the form.

    9.  Click the **Impacted Controls** tab.

    10. Add the controls by clicking **Add**.

    11. Save the form.

        **Note:** You can raise a compliance review by clicking **Request compliance review**.

    The approval form is sent to the approver.

    The approver can either approve the request by clicking **Approve** or request additional approval by clicking **Request Additional Approval**.

    The record state changes to Deferred. The reason stated is the one you selected when raising the exception request. The **Deferral** tab provides additional notes on the record.

    **Note:** If the request gets rejected, the record moves to its previous state.

4.  Click **Submit**.

    For more information on the Policy Exception Integration and the hand-off between the remediation owner and the compliance manager, see [Policy and Compliance Management optional setup](https://www.servicenow.com/docs/access?context=policy-compliance-optional-steps&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).


