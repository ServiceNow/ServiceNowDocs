---
title: Configure E-signature for approvals
description: Approval with e-Signature plugin \(com.glide.e\_signature\_approvals\) enables users to approve requests by authenticating their login credentials.
locale: en-US
release: yokohama
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Approvals hub, Setup task management, Configure, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Configure E-signature for approvals

Approval with e-Signature plugin \(com.glide.e\_signature\_approvals\) enables users to approve requests by authenticating their login credentials.

## Before you begin

Ensure you install Approval with e-Signature plugin \(com.glide.e\_signature\_approvals\) from **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

Role required: Admin

## About this task

On activation, the **Approval with e-signature** plugin adds a prompt for credentials when an approver attempts to approve a request from the list context menu. Enable E-signature approvals on a table-by-table basis. For detailed information on the plugin, see [Approval with e-signature](https://servicenow.com/docs/bundle/vancouver-servicenow-platform/page/administer/service-administration/concept/approval-with-e-signature.html).

For the OOTB approvals:​

-   Approval users are prompted with e-signature ​before approving or rejecting the item.
-   Approval users can add comments first and without the e-signature.
-   When you cancel the e-signature, the task remains in the pending tasks.​
-   When you approve with an e-signature, the task progresses to the completed section.​

E-signature approvals provide security, compliance, and accountability by introducing the ability for users to enter login credentials before taking an action.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **e-Signature Registries**.

2.  In **Table name**, select an existing table from the drop-down list.

    -   **Table**: A table list to select the table that requires e-signature.
    -   **Enabled**: On selection, an e-signature is required. Clear this option to remove the e-signature requirement.
3.  Select **Save**.


## Result

When you select a table \(sc\_request\) and enable the e-signature, the approvers can perform the approve or reject actions only after a successful user credential authentication. The approver authentication window redirects to the identity provider login screen for an SSO enabled instance.​

![User credential authentication for approval](../images/esignature-authentication.png "Approver authentication")

**Note:** When you do not upgrade to the latest employee center, you do not see the authentication window.

For more information on approvals, see [Use Approvals hub](ec-to-dos-use-approval-hub.md).

