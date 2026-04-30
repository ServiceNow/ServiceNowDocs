---
title: Set up predefined Playbooks for Portals
description: Set up predefined Playbooks for Portals to provide end users with the playbook experience on your service portal.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Playbooks for Portals, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Set up predefined Playbooks for Portals

Set up predefined Playbooks for Portals to provide end users with the playbook experience on your service portal.

## Overview of Playbooks

Playbooks guide users through complex processes and enable them to save their progress and resume their work when convenient. They can also get the information that they need for each stage of the flow and its associated activities with the Customer Service Management \(CSM\) playbooks on service portals.

You can activate Playbooks for Portals if you have the admin role. The base system is delivered in an inactive state. You must activate it in the Playbooks \(PAD\) for the user to see it.

Plugins required:

-   Playbooks for Customer Service Management: sn\_csm\_playbook
-   Playbook Experience: sn\_playbook\_exp
-   Case Playbook for Onboarding: sn\_onboarding \(required if you need the predefined playbook experience\)
-   Case Playbook for Product Support: sn\_product \(required if you want to use the product case playbook and record generator\)

Plugins are available from the ServiceNow® Store. For more information, see [Playbook plugins](customer-service-case-playbooks.md).

## Summary of steps for setting up predefined Playbooks for Portals

You can set up Playbooks for Portals using the following high level steps.

1.  Activate the draft state in the onboarding case type state. For more information, see [Activate the draft state in the onboarding case type state](activate-the-draft-state-in-the-onboarding-case-type-state.md).
2.  [Activate the Record Generator](activate-the-record-generator.md)
3.  [Activate a new onboarding playbook with self-service](activate-a-new-onboarding-playbook-with-self-service-in-pad.md)
4.  Activate guided onboarding in the playbook content items. For more information, see [Activate guided onboarding in Playbook content items](activate-guided-onboarding-in-playbook-content-items.md).
5.  Add a **Process** tab to the Portal so that users can see where they are in the Playbook process. See [Add the Process tab to the Portal](../task/add-process-tab-portal.md) for more information.

