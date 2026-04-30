---
title: Configure approver groups for benefit eligibility determination in Social Benefits Playbook
description: Configure an approval user group for the Propose Decision Activity, so that the constituent’s eligibility determination can be routed to the appropriate people for final approval.Create a scripted extension point to create an approver group for the Propose Decision Activity in the Social Benefits Playbook.Add users to approver group for the Propose Decision Activity in the Social Benefits Playbook.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2026-03-28"
reading_time_minutes: 1
breadcrumb: [Assign personas, roles, responsibilities, and groups, Social Benefits Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure approver groups for benefit eligibility determination in Social Benefits Playbook

Configure an approval user group for the Propose Decision Activity, so that the constituent’s eligibility determination can be routed to the appropriate people for final approval.

At the Propose Decision Activity, case agents need to decide whether to grant or deny benefits. An approver group needs to be configured, so that this decision can be routed to supervisors for review and approval. Create a scripted extension point to create an approver group for the Propose Decision Activity in the Social Benefits Playbook. Once the case agent makes a benefit decision during this activity, the case will be routed to the individuals in the approver group for review and approval.

## Create a scripted extension point for an approver group

Create a scripted extension point to create an approver group for the Propose Decision Activity in the Social Benefits Playbook.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Scripted Extension Points**.

2.  In the **API Name** column, select `sn_gsm_soc_bnfts.SocialBenefitsConfig`.

3.  Select the **Create implementation** related link.

    An alert banner that reads **New script include created and registered as an extension point instance** should appear.

4.  Select **Update**.


## Add users to an approver group

Add users to approver group for the Propose Decision Activity in the Social Benefits Playbook.

### Before you begin

Role required: admin

### About this task

A user record must have already been created.

### Procedure

1.  Navigate to **All** &gt; **System Security** &gt; **Groups**.

2.  Select the **Social Benefits – Propose Decision** group.

3.  Select the **Group Members** tab, then select **Edit**.

4.  Add the desired users to the Group Members List and select **Save**.

    Make sure a user record has been created within the organization; navigate to **All** &gt; **User Administration** &gt; **Users** to create a user record.

5.  Select **Update**.


### Result

An approver group has been created and can be used in the Propose Decision activity of the Social Benefits Playbook. You can edit this group at any time by removing or adding new users to the group Users list.

