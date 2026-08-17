---
title: Implement a recall campaign set up
description: Set up a recall campaign to define corrective actions, identify impacted assets, create tracking phases, and control dealer visibility throughout the recall lifecycle.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-recall-campaign-setup.html
release: australia
topic_type: task
last_updated: "2026-07-01"
reading_time_minutes: 2
breadcrumb: [MCO core implementation, Configure, Manufacturing Commercial Operations]
---

# Implement a recall campaign set up

Set up a recall campaign to define corrective actions, identify impacted assets, create tracking phases, and control dealer visibility throughout the recall lifecycle.

## Before you begin

Role required: sn\_rcl\_claim\_mgmt.recall\_manager or admin

## Procedure

1.  Review the entities and relationships within the [Recall campaign data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/recall-claims.md), including tables added or modified by the recall claim plugin.

2.  Configure recall campaign: Complete the following tasks to set up the recall campaign in your environment.

    1.  Install Manufacturing recall claim management \[sn\_rcl\_claim\_mgmt\]: [Install Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/install-manufacturing-commercial-operations-core.md).
    2.  Set up product models and parts: and [Configure product model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-configure-product-model.md).
    3.  Set up assets and install base items: [Configure assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-configure-assets.md) and [Configure install base item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-create-install-base-item.md).
    4.  Set up dealers: [Set up Dealer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-dealer-setup.md)
    5.  Assign recall roles: [Assigning roles in Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/assign-mco-roles.md).
3.  Work with recall campaign \(OEM\): Use the Agents \(CSM/FSM\) workspace to create and manage recall campaigns, phases, and claims.

    1.  Create a recall campaign: [Create a campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-rc-my-campaigns.md).

    2.  Define corrective action and charges: [Corrective actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-corrective-actions.md).

    3.  Import impacted asset: [Importing impacted assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco_importing_impacted_assets.md).

    4.  Create and manage campaign phases: [Recall a campaign phase](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-recall-campaign-phases.md).

    5.  Create phases and sub-phases: [Create a phase and sub-phase in a recall campaign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco_phases_sub-phases.md).

4.  Work with recall campaign \(Dealer\): Use the Dealer portal to submit and track recall claims.


