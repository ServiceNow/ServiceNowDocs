---
title: Set up Playbooks for Portals
description: Set up Playbooks for Portals to provide end users with the playbook experience on your service portal.Portal user can save a case during the intake process and continue at a later time​ with the draft state.Activate the record generator to the portal case and display the new guided playbook to the user. Portal user can navigate through the playbook steps to complete the case intake.Activate a new onboarding playbook with self-service in Playbooks \(PAD\) to ensure that the new playbook is visible.Activate guided onboarding in playbook content items and verify that the new content item launches the playbook record generator that is associated with it.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Playbooks for Portals, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Set up Playbooks for Portals

Set up Playbooks for Portals to provide end users with the playbook experience on your service portal.

## Overview of Playbooks

Playbooks guide users through complex processes and enable them to save their progress and resume their work when convenient. They can also get the information that they need for each stage of the flow and its associated activities with the Customer Service Management \(CSM\) playbooks on service portals.

You can activate Playbooks for Portals if you have the admin role. The base system is delivered in an inactive state. You must activate it in the Playbooks \(PAD\) for the user to see it.

Plugins required:

-   Playbooks for Customer Service Management: sn\_csm\_playbook
-   Playbook Experience: sn\_playbook\_exp
-   Case Playbook for Onboarding: sn\_onboarding \(required if you need the out of the box playbook experience\)
-   Case Playbook for Product Support: sn\_product \(required if you want to use the product case playbook and record generator\)

Plugins are available from the ServiceNow® Store. For more information, see [Playbook plugins](customer-service-case-playbooks.md).

## Summary of steps for setting up Playbooks for Portals

You can set up Playbooks for Portals using the following high level steps.

1.  Activate guided onboarding in the playbook content items. For more information, see [Activate guided onboarding in Playbook content items](activate-playbooks-for-portals.md#).
2.  Define your process using Workflow Studio. See [Create a playbook](https://www.servicenow.com/docs/access?context=create-process-definition&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US) for more information.
3.  Activate the draft state in the onboarding case type state. For more information, see [Activate the draft state in the onboarding case type state](activate-playbooks-for-portals.md#).
4.  Activate the record generator. For more information, see [Activate the Record Generator](activate-playbooks-for-portals.md#).
5.  Set up ACLs \(Access Control Lists\) to provide the appropriate read, write, and create permissions for users. See [Explicit Roles in CSM](../../../administer/contextual-security/concept/explicit-roles-in-csm.md) for more information.

    **Note:** Add write and create roles with a condition based on "State=draft" so that users can only edit the fields in the draft state.

6.  Create a Playbook Content Item so that users can navigate to the Playbook experience. See  for more information.
7.  Set up a redirection widget so that users are redirected to the playbook intake experience once the state changes from "draft" to "new." See  for more information.
8.  Add a **Process** tab to the Portal so that users can see where they are in the Playbook process. See  for more information.

## Activate the draft state in the onboarding case type state

Portal user can save a case during the intake process and continue at a later time​ with the draft state.

### About this task

Activate a draft state for the onboarding case type so that the case remains in the draft state during the intake stage until the case is submitted.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **sys\_choice.list**.

2.  Select the record with **Table name** - **sn\_onboarding\_case** with the **Element** field value as **state**, and the **Label** field name as **Draft**.

3.  Select **Edit**.

4.  Clear the **Inactive** check box.

5.  Select **Update**.

6.  Navigate to **System Definition** &gt; **Scheduled Job**and search for **sys\_id** - **ba5ba3d8944e7110f87759453e4c7084** or **Name** - **Update My Lists URL for draft cases**.

7.  Select **Execute Now**.

    This action excludes the Draft cases from the list filter on the **My List** tab on the initial page load.


## Activate the Record Generator

Activate the record generator to the portal case and display the new guided playbook to the user. Portal user can navigate through the playbook steps to complete the case intake.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Playbook Experience** &gt; **Record Generators**.

2.  In the list, select the **Table name** - **sn\_onboarding\_case** with **Process Definition** name - **Onboarding with Self-Service**.

3.  Select **Edit**.

4.  Select the **Active** check box.

5.  Select **Update**.


## Activate a new onboarding playbook with self-service

Activate a new onboarding playbook with self-service in Playbooks \(PAD\) to ensure that the new playbook is visible.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation Designer**.

2.  On the Processes tab, select the label **Onboarding with Self-Service**.

3.  From the More actions menu, select **Activate**.

    Verify that the previous PAD process is deactivated.


## Activate guided onboarding in Playbook content items

Activate guided onboarding in playbook content items and verify that the new content item launches the playbook record generator that is associated with it.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Playbook Experience** &gt; **Playbook Content Items**.

2.  Select **New Guided Onboarding Request**.

3.  Select **Edit**.

4.  Select the **Active** check box.

5.  Select **Update**.


