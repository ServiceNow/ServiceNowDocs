---
title: Opportunity publishing approval
description: The Opportunity Marketplace's publishing approval framework streamlines the approval process, allowing Opportunity Owners to submit drafts for approval and receive notifications upon approval or rejection.
locale: en-US
release: australia
product: Opportunity Marketplace
classification: opportunity-marketplace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Opportunity Marketplace, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Opportunity publishing approval

The Opportunity Marketplace's publishing approval framework streamlines the approval process, allowing Opportunity Owners to submit drafts for approval and receive notifications upon approval or rejection.

In versions 2.3 and later, Opportunity Marketplace includes an out-of-the-box framework to automate the publishing approval workflow for the gig, volunteer, and project opportunity types.

-   The Opportunity Owner can submit a draft opportunity for approval from the Create an opportunity form and monitor the status of the approval request. They receive an email notification when the Opportunity Approver approves or rejects the draft.
-   The Opportunity Approver is notified of the approval request via email and an assigned approval task. They can review the opportunity draft and either approve or reject with comments from the notification interface.
-   Admins can configure approver users and additional approval rules.

## Approval workflow

Each out-of-the-box opportunity type \(gig, volunteer, and project\) has a respective subflow to facilitate the approval workflow. Each subflow has default configurations, which determine the conditions under which the opportunity is sent for approval.

1.  If the conditions are met, the subflow requests approval from the users listed in the Opportunity Type Auxiliary \[sn\_opp\_market\_opportunity\_type\_aux\] table for that respective opportunity type.
2.  If an approver approves the opportunity, the system notifies the Opportunity owner and publishes the opportunity.
3.  If the approver rejects the opportunity, the system reverts the opportunity to draft state and notifies the Opportunity owner of the approver’s feedback, which they can implement and resubmit for approval.

**Note:** By default, only one approval is necessary for the system to publish an opportunity, and only one rejection is necessary to prevent an opportunity from being published, however the admin can configure alternative approval scenarios, such as requiring a greater number of required approvals or at minimum two rejections. For more information, see the **Approvers** section below.

The following diagram provides a visual of the approval workflow:![Visual overview of the approval steps described above](../image/oppt-approval-wkflw.png)

The following describes the default configurations for the subflows, which can be modified in the Workflow studio.

|Subflow|Settings description|
|-------|--------------------|
|Gig opportunity posting &amp; editing approval|This subflow sends the opportunity for approval if it requires a time commitment of 20 or more hours per week \(line 2\). Unlike the other two subflows, this one assigns the opportunity owner’s manager as the approver \(line 7-10\) in addition to the listed approvers.|
|Volunteer opportunity posting &amp; editing approval|This subflow requires approval for the opportunity if the total number of participants is twenty or more \(line 1\).|
|Project opportunity posting &amp; editing approval|This subflow requires approval for the opportunity if the total number of participants is five or more \(line 1\).|

**Note:** Only the `Project opportunity posting & editing approval` flow is assigned to the project opportunity type out-of-the-box; for volunteer and gig opportunity types, the admin must manually assign the flow. For the steps on assigning the approval flows, see .

For custom opportunity types, the admin can reuse either the `Project opportunity posting & editing approval` or `Volunteer opportunity posting & editing approval` flows, as they support opportunities with multiple roles.

## Approvers

If your instance has demo data loaded, the group `OPM Opportunity Approvers` is assigned to the gig, volunteer, and project opportunity types. An admin can add users to the `OPM Opportunity Approvers` group to review all opportunity drafts. Alternatively, the admin can define approvers for a specific opportunity type. For the steps on assigning approvers to an opportunity type, see step 4 of .

While the default subflow requires only one approval or rejection, the admin can configure alternative approval scenarios, such as requiring a greater number of required approvals to publish an opportunity or at minimum two rejections to prevent the opportunity from being published.![Under the Ask for Approval action, users can modify the rule regarding how many users must approve or reject an opportunity](../image/modify-approvers.png)

**Parent Topic:**[Explore Opportunity Marketplace \(OPM\)](egd-oppt-mrktplc-explore.md)

