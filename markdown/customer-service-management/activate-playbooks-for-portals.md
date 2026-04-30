---
title: Set up custom Playbooks for Portals
description: Create custom Playbooks for Portals to provide end users with the playbook experience on your service portal.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Playbooks for Portals, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Set up custom Playbooks for Portals

Create custom Playbooks for Portals to provide end users with the playbook experience on your service portal.

## Overview of Playbooks

Playbooks guide users through complex processes and enable them to save their progress and resume their work when convenient. They can also get the information that they need for each stage of the flow and its associated activities with the Customer Service Management \(CSM\) playbooks on service portals.

You can activate Playbooks for Portals if you have the admin role. The base system is delivered in an inactive state. You must activate it in the Playbooks \(PAD\) for the user to see it.

Plugins required:

-   Playbooks for Customer Service Management: sn\_csm\_playbook
-   Playbook Experience: sn\_playbook\_exp
-   Case Playbook for Onboarding: sn\_onboarding \(required if you need the predefined playbook experience\)
-   Case Playbook for Product Support: sn\_product \(required if you want to use the product case playbook and record generator\)

Plugins are available from the ServiceNow® Store. For more information, see [Playbook plugins](customer-service-case-playbooks.md).

## Summary of steps for setting up Playbooks for Portals

You can set up Playbooks for Portals using the following high level steps.

1.  Define your process using Workflow Studio. See [Create a playbook](https://www.servicenow.com/docs/access?context=create-process-definition&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US) for more information.
2.  Activate the record generator. For more information, see [Activate the Record Generator](activate-the-record-generator.md).
3.  Set up ACLs \(Access Control Lists\) to provide the appropriate read, write, and create permissions for users. See [Explicit Roles in CSM](../../../administer/contextual-security/concept/explicit-roles-in-csm.md) for more information.

    **Note:** Add write and create roles with a condition based on "State=draft" so that users can only edit the fields in the draft state.

4.  Create a Playbook Content Item so that users can navigate to the Playbook experience. See [Create a Playbook Content Item](../task/create-content-item.md) for more information.
5.  Set up a redirection widget so that users are redirected to the playbook intake experience once the state changes from "draft" to "new." See [Set up a redirection widget](../task/set-up-redirection-widget.md) for more information.

