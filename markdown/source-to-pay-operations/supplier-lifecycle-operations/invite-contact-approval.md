---
title: Configure the flow to create approval records for all supplier contact invite requests
description: Typically, an approval record is created only when a supplier contact self-registers to get access to the Supplier Collaboration Portal. However, a supplier admin can configure the Supplier Contact Onboarding flow to create approval records even when a supplier manager adds or invites a new supplier contact.
locale: en-US
release: xanadu
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure self-registration for external users, Install Supplier Collaboration Portal, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configure the flow to create approval records for all supplier contact invite requests

Typically, an approval record is created only when a supplier contact self-registers to get access to the Supplier Collaboration Portal. However, a supplier admin can configure the Supplier Contact Onboarding flow to create approval records even when a supplier manager adds or invites a new supplier contact.

## Before you begin

Role required: sn\_slm.admin

## About this task

After you perform this task, an approval record is created for the Enroll a new supplier user case type, regardless of whether a supplier contact self-registers or a supplier manager invites a new supplier contact.

**Important:** Supplier Lifecycle Operations creates an approval record if the "Ask For Approval" action is a part of any SLO flow. This approval record can be approved by the user who belongs to the Supplier Administrators group \(sys\_user\_group table\). For more information, see [Add a user to a group](https://www.servicenow.com/docs/access?context=t_AddAUserToAGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select the **Subflows** tab, search for and select the **Supplier Contact Onboarding** flow.

3.  Search for the **If the onboarding request is created by Relationship Manager or Contact is invited** condition label and select it, which expands the condition label.

4.  Delete the Condition 2 by selecting the remove condition icon \(![Remove condition icon.](../image/cross-flow-icon.png)\) next to the condition.

    ![Supplier Contact Onboarding flow.](../image/supp-onboard-flow.png)

5.  Select **Save**.


**Parent Topic:**[Configure self-registration for external users](config-reg-for-external-users-slm.md)

