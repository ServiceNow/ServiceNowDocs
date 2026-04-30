---
title: Work on a digital forensic request
description: As a member of the digital forensic team, you work on a legal request to investigate and resolve the request.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage, Legal Digital Forensics, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Work on a digital forensic request

As a member of the digital forensic team, you work on a legal request to investigate and resolve the request.

## Before you begin

Role required: sn\_lg\_ops.legal\_fulfiller

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, under **Legal Requests**, click **All**.

    If you are a collaborator to a legal request, you can open your assigned collaborations from **Collaborations** under **Legal Request**.

4.  Open a digital forensic request to work on.

    -   If the legal request is unassigned, click **Assign to me** to assign it to yourself. To assign to another member, select the member's name in the **Assigned to** field and click **Save**.

        The state of the legal request updates to Assigned. If the **Digital Forensics - Privacy Approval** flow is active, an approval flow is triggered. For each custodial and non-custodial data in the digital forensic request, one corresponding approval record is created and is assigned to each member in the legal privacy group. Any member from the legal privacy group can review and [approve or reject these approval records](approve-reject-dft-request.md).

        The status of custodial and non-custodial data updates to Pending Approval. You can review the status of the approval records in the **Approvers** tab.

    -   If you need help from other fulfillers to work on the legal request, add them in the **Collaborators** field.

        The collaborators are notified via email that they have been added as collaborators to a legal request.

        **Note:** The collaborators get the same degree of access as you to work on the legal request, but they can't modify the **Assigned to**, **Assignment group**, and **Assignment group permission** fields.

    -   In the **Custodial Data** and **Non-custodial Data**, you can add new custodial and non-custodial data by clicking **New** and filling the details. For these newly added custodial and non-custodial records, the approval flow is triggered, which creates approval records and assigns them to each member of the legal privacy group.

        **Note:**

        The approval details appear under the **Approvals** tab on the Standard Ticket page.

    -   After [getting approvals](approve-reject-dft-request.md), promote the approved custodial data in the **Custodial Data** tab and the approved non-custodial data in the **Non-custodial Data** tab to a new or existing legal matter.

        -   To promote them to a new legal matter, select them and click **Create Matter**. You can choose to create the matter using a digital forensic matter template to populate the matter with predefined phases and tasks.
        -   To promote them to an existing legal matter, select them and click **Add to an Existing Matter**. In the Add to Existing Matter dialog box, select a matter from the list, and click **OK**.
        For more information, see [Promote a legal request to a legal matter](../../legal-request-management/task/promote-legal-request-to-matter.md).

        **Note:** You can promote the legal request to a legal matter only if you have installed Legal Matter Management and [set the record producer type](../../legal-request-management/task/associate-categories-practice-area.md) in the associated intake form as **Request and Matter**.

        The legal matter to which the custodial and non-custodial data records are promoted appears in the **Legal Matters** tab.

    -   Associate other related legal matters to the legal request. In the **Legal Matters** tab, click **Add** and select the legal matter to associate.
    -   Remove a legal matter from the legal request if the legal matter is not required to be tracked for the request. In the **Legal Matters** tab, select the legal matter to remove, and click **Remove**. If the removed matter is a digital forensic legal matter, all custodial and non-custodial records from the legal matter are also removed. The legal matter owner should cancel the associated phases and tasks from the matter manually.
    -   Close the legal request after you complete the required activities to resolve the matter.

        **Note:** A legal request is automatically closed when it is associated to a legal matter and the matter owner chooses to close the related requests while closing the matter.

    -   If the request no longer needs any resolution, cancel the request.

        All custodial and non-custodial data records, as well as any pending approval records associated with them, are also cancelled.


**Parent Topic:**[Managing digital forensics requests](../concept/managing-legal-dft-request.md)

