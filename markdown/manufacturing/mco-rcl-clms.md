---
title: Recall campaign
description: A recall process is a structured procedure launched by Original Equipment Manufacturers \(OEM\) to fix defects or issues in their manufactured products that are sold to the customers. Dealers can submit repair claims for work performed as part of recall campaigns, while OEM assessors benefit from a playbook-guided experience that simplifies and standardizes claim resolution.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [MCO core, Explore, Manufacturing Commercial Operations]
---

# Recall campaign

A recall process is a structured procedure launched by Original Equipment Manufacturers \(OEM\) to fix defects or issues in their manufactured products that are sold to the customers. Dealers can submit repair claims for work performed as part of recall campaigns, while OEM assessors benefit from a playbook-guided experience that simplifies and standardizes claim resolution.

![Recall campaign workflow](../image/recall-claim-wf.png "Recall campaign workflow")

1.  Create recall campaign: The Recall manager creates the recall campaign.
2.  Corrective action and charges: The dealer enters the parts and software asset details for which the claim is raised.
3.  Add impacted: The Recall manager adds the assets that are impacted for the recall campaign.
4.  Create campaign phases: The Recall manager creates the campaign phases based on the location or the dealer.
5.  Select dealers included: OEM selects the dealers who are impacted by the recall campaign.
6.  Publish the campaign to dealers: Recall phase owners sends the campaigns to the dealers.
7.  View recall campaign details: Dealers can view the recall campaign details created by the recall manager.
8.  Submit recall claims: The Dealer submits the recall claims.
9.  Close campaigns: The Recall manager closes the recall campaigns.

## Phases and sub-phases

The MCO agent portal enables manufacturers to manage recall campaigns through a structured workflow. The portal provides capabilities to create campaign phases and sub-phases, select target assets for recall, launch campaigns, and notify affected dealers.

## Working with recall campaign

Use the following to configure, use, and manage recall campaigns in MCO.

Review the entities and relationships within the [Recall campaign data model](../reference/recall-claims.md), including tables added or modified by the recall claim plugin.

1.  Configure recall campaign: Complete the following tasks to set up the recall campaign in your environment.
    1.  Install Manufacturing recall claim management \[sn\_rcl\_claim\_mgmt\]: [Installing applications, plugins, and products](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/installing-apps-app-manager.md).
    2.  Set up product models and parts: [Configuring product models](mco-product-models.md)
    3.  Set up assets and install base items: [Configuring assets](mco-assets.md) and [Create an install base item](mco-create-install-base-item.md)
    4.  Set up dealers: [Set up dealer](set-up-dealer.md)
    5.  Assign recall roles: [Assign roles](assign-mco-roles.md)
2.  Work with recall campaign \(OEM\): Use the Agents \(CSM/FSM\) workspace to create and manage recall campaigns, phases, and claims.
    1.  Create a recall campaign: [Create a campaign](mco-rc-my-campaigns.md)
    2.  Define corrective action and charges: [Corrective actions](../task/mco-corrective-actions.md)
    3.  Import impacted asset: [Importing impacted assets](../task/mco_importing_impacted_assets.md)
    4.  Create and manage campaign phases: [Recall a campaign phase](../task/mco-recall-campaign-phases.md)
    5.  Create phases and sub-phases: [Create a phase and sub-phase in a recall campaign](../task/mco_phases_sub-phases.md)
3.  Work with recall campaign \(Dealer\): Use the Dealer portal to submit and track recall claims. [Submit a repair claim for recall](../task/mco-submit-repair-claim-for-recall.md).

