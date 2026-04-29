---
title: Create a policy exception from Employee Center
description: Use the Employee Center to request exceptions for policies, control objectives, controls, or issues by specifying the reason of exception on a particular list of the systems, applications, networks, or entities for which the exception applies.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Manage GRC tasks from Employee Center, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Create a policy exception from Employee Center

Use the Employee Center to request exceptions for policies, control objectives, controls, or issues by specifying the reason of exception on a particular list of the systems, applications, networks, or entities for which the exception applies.

## Before you begin

Role required: sn\_grc.business\_user, sn\_grc.business\_user\_lite, sn\_grc\_emp\_user.grc\_employee

## Procedure

1.  Navigate to **Self-Service** &gt; **Employee Center**.

2.  Select the **Browse all Risk &amp; Compliance** section.

3.  Select the **Policy Exception** catalog item.

4.  On the form, fill in the fields.

<table id="policy-excep-table"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

What is the exception for?

</td><td>

Type of policy exception that you want to create. The options are:-   Policy: Create a policy exception based on a policy.
-   Control objective: Default is a single control objective on which the policy exception is created.
-   Controls: Option to create a policy exception on multiple controls.
-   Issue: Option to create a policy exception on an issue.


</td></tr><tr><td>

Policy

</td><td>

Policy associated with this policy exception.

</td></tr><tr><td>

Control objective

</td><td>

Control objective associated with this policy exception.When you select a control objective, the**Impacted controls** field appears.

</td></tr><tr><td>

Control

</td><td>

Select **Control** to associate multiple controls from different control objectives. This option supports multiple controls objectives for your policy exception, instead of creating multiple policy exceptions that could be applied on multiple controls.

</td></tr><tr><td>

Issue

</td><td>

Issue associated with this policy exception.

</td></tr><tr><td>

Impacted controls

</td><td>

Controls associated to the control objective.

</td></tr><tr><td>

Short description

</td><td>

Brief description about the policy exception request.

</td></tr><tr><td>

Description

</td><td>

Detailed description of the policy exception request.

</td></tr><tr><td>

Reason

</td><td>

Reason for the exception

</td></tr><tr><td>

Justification

</td><td>

Evidence or rationale for the policy exception.

</td></tr><tr><td>

Risk description

</td><td>

Description of the risk as performed by the risk manager during risk assessment.

</td></tr><tr><td>

Valid from

</td><td>

Day on which the policy exception begins.

</td></tr><tr><td>

Valid to

</td><td>

Day on which the policy exception ends.

</td></tr><tr><td>

Priority

</td><td>

Approval priority of this policy exception.

</td></tr><tr><td>

Watch list

</td><td>

Users that are notified when the request is updated.

</td></tr></tbody>
</table>5.  Click **Submit**.

    You are directed to the My Request page where you can view your policy exception number for the submitted policy exception request. This page is read-only and you can view all your requests that you have raised as a business user.

6.  Post a message to support the policy exception in the **Activity** field.

7.  To attach a document related to the policy exception, select the **Attachments** tab.

8.  Click **My Requests** link at the top right corner to view a list of all your requests that includes your issues and policy exceptions.

    The list shows 15 requests at a time. Click **Show More Requests** for more requests to be listed.

9.  Select **Request Approval** from the **Actions** list if the request is in **Analyze** state.

    If you raise a policy exception from Employee Center and if verification rules are not configured, then the policy exception moves to the Analyze state. However, if verification rules are configured for the policy exception, then the policy exception moves to the New state and the verification approval process is triggered. As verification rules are configured the approver is required to verify the policy exception and approve it, only then the policy exception moves to Analyze state.

    ![Request approval for a policy exception.](../image/PolicyExcepReqApproval.png "Request approval for a policy exception")

10. After the policy exception is approved, you can request extension of your policy exception, select **Request extension** from the **Actions** list.

    1.  Enter the new extension date that is later than the current **Valid to** date.

        By default, you cannot extend your policy for more than 30 days from the **Valid from** date. However, the extension can be relaxed based on the maximum exception duration days of the policy.

    2.  Select a reason for extension from the list in the **Extension reason** field.

    3.  Enter a justification for the extension.

    4.  Click **Request**.

        The number of remaining extensions that you can avail to request is displayed as **Remaining extensions**.


