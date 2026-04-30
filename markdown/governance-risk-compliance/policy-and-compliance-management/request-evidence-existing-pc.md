---
title: Reuse existing evidence from the related items of an engagement
description: Inform the audit and compliance user about the evidences that are already existing for the related items of an engagement. You can add such an evidence, if it is already existing for any of the related item table of an engagement for which you are requesting an evidence.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage evidence requests, Use the Classic user interface for Policy and Compliance tasks, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Reuse existing evidence from the related items of an engagement

Inform the audit and compliance user about the evidences that are already existing for the related items of an engagement. You can add such an evidence, if it is already existing for any of the related item table of an engagement for which you are requesting an evidence.

## Before you begin

Role required: sn\_audit.user

## About this task

For an engagement, an evidence can be created on Entity, Control, Audit Task, Control Test Issue, Other Issues, or any of the related item table. If there are existing evidences, then the Request Evidence pop-up displays a message that there are existing evidences that you might want to add.

**Note:** Evidences that are directly created on a related item, and existing evidences that are in **Closed** state as well as those that are within six months from the due date of evidence response can only be added.

The logged in user must also have access to the engagement for which evidence records exist or must be the user who has access to the engagement record to view and add them. If the logged in user does not have access to those records, although there are evidences existing on those related items, they are not displayed for the user to add.

## Procedure

1.  Navigate to **All** &gt; **Audit** &gt; **Engagements** &gt; **All Engagements**.

2.  Click to open an engagement.

3.  Select the related list from which you want to request evidence.

4.  From the **Action on selected rows** list, select **Request Evidence**.

    You can either create a new evidence request or add existing evidence request. The Evidence request is created but not evidence request tasks.

5.  To create a new evidence request, enter details on the Request Evidence pop-up and click the **Request** button.

6.  To view existing requests, click **View** in the message.

    ![Add existing evidence.](../image/RequestEvidenceViewMessage.png "Add existing evidence")

    **Note:** If there is no existing evidence, then the message does not appear in the Request Evidence pop-up.

7.  To view all existing evidences created on the related items, click the Evidence related list.

    When the evidence is in **Closed Complete** state, the UI action buttons such as **New**, **Add existing evidence**, **Remove**, and **Delete** are disabled. You can perform these UI actions only when the engagement or any other audit and compliance object is in an active state.

8.  To associate the evidence, click the **Add Existing Evidence** button and select the evidence.

    **Note:** The **Add Existing Evidence** button is only available in the Evidence related item of an Engagement form and not in any other compliance or audit objects of the Classic environment.

9.  To remove the association of the evidences linked to the engagement, select the evidences in the Evidence related list and click **Remove** in the **Actions on selected rows** list.

    **Note:** The remove action only removes the association of the existing evidences from the engagement and does not remove the evidence record from the database.


