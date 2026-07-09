---
title: Implement a repair claim set up
description: Configure the Manufacturing repair claim system to manage product repairs, dealer submissions, and claim approvals across your OEM and dealer network.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-set-up-repair-claim.html
release: australia
topic_type: task
last_updated: "2026-07-02"
reading_time_minutes: 2
breadcrumb: [MCO core implementation, Configure, Manufacturing Commercial Operations]
---

# Implement a repair claim set up

Configure the Manufacturing repair claim system to manage product repairs, dealer submissions, and claim approvals across your OEM and dealer network.

## Before you begin

Role required: admin or sn\_claim\_cmn.warranty\_specialist

## About this task

Use this task to set up the repair claim system in Manufacturing Commercial Operations. The system manages repair claims submitted by dealers and tracked by OEM administrators. Complete these setup steps to enable repair claim functionality across your environment.

## Procedure

1.  Review the entities and relationships within the [Repair claims data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/repair-claims.md), including tables added or modified by the repair claim plugin.

2.  Configure repair claims: Complete the following tasks to set up the repair claims in your environment.

    1.  Install Manufacturing repair claim management \[sn\_repr\_claim\_mgmt\]: [Install Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/install-manufacturing-commercial-operations-core.md).

    2.  Set up product models and parts: [Configure product model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-configure-product-model.md).

    3.  Set up assets and install base items: [Configure assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-configure-assets.md) and [Configure install base item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-create-install-base-item.md).

    4.  Set up dealer hierarchy: [Create channel partner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-create-channel-partner.md) and [Create internal business location](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-create-internal-business-location.md).

        **Note:** Use the Partner Relationship Management data model to set up channel partners \(external entities\) and dealers \(external trading partners to the OEM\). Model company-owned dealer outlets as internal service organizations using the Service Model Foundation.

    5.  Set up dealers: [Create dealer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-create-dealer.md).

    6.  Assign repair claim roles: [Assigning roles in Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/assign-mco-roles.md).

3.  Work with repair claims \(OEM\): Use the Agents \(CSM/FSM\) workspace to create and manage repair campaigns, phases, and claims.

    1.  Create a repair claim: [Create a repair claim using playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-create-rc-using-playbook.md).

    2.  Review repair claims: [Reviewing and approving repair claims](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-approve-repair-claims.md).

4.  Work with repair claim \(Dealer\): Use the Dealer portal to submit and track repair claims: [Repair claim for the dealer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/repair-claim-dealer.md).


