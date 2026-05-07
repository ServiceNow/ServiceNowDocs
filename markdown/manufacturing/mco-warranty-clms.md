---
title: Repair claim
description: In the Repair claims workflow, the customer approaches the dealer with issues related to one or more products. The dealer diagnoses and fixes the issue​ and raises the reimbursement for the repair work performed.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [MCO core, Explore, Manufacturing Commercial Operations]
---

# Repair claim

In the Repair claims workflow, the customer approaches the dealer with issues related to one or more products. The dealer diagnoses and fixes the issue​ and raises the reimbursement for the repair work performed.

![Decorative](../image/repair-claim-wf.png "Repair claim workflow")

1.  Initiate claim: The dealer initiates the warranty or recall claim.
2.  Search serial number: Dealer can search the claim details based on the serial number.
3.  Enter claim job details: The dealer enters the job details in the dealer portal.
4.  Enter parts and labor, misc services, attachments: The dealer enters the labor code and parts in the dealer portal.
5.  Submit claim: The dealer submits the claims request to the OEM.
6.  Review claim: OEM reviews the claims request submitted by the dealer.
7.  Approve claim: OEM reviews the claims and either approves, rejects, partially approves, or sends back the claim.
8.  Generate expense line: The claims agent processes the expense line and is generated only for approved or partially approved claims.

## Working with repair claim

Use the following to configure, use, and manage recall campaigns in MCO.

Review the entities and relationships within the [Repair claims data model](../reference/repair-claims.md), including tables added or modified by the repair claim plugin.

1.  Configure repair claims: Complete the following tasks to set up the repair claims in your environment.
    1.  Install Manufacturing repair claim management \[sn\_repr\_claim\_mgmt\]: [Installing applications, plugins, and products](https://www.servicenow.com/docs/access?context=installing-apps-app-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
    2.  Set up product models and parts: [Configuring product models](mco-product-models.md).
    3.  Set up assets and install base items: [Configuring assets](mco-assets.md) and [Create an install base item](mco-create-install-base-item.md).
    4.  Set up dealer hierarchy: [Create a channel partner](../task/mco-create-channel-partner.md) and [Create an internal business location](../task/mco-create-internal-business-location.md).

        **Note:** Use the Partner Relationship Management data model to set up channel partners \(external entities\) and dealers \(external trading partners to the OEM\). Model company-owned dealer outlets as internal service organizations using the Service Model Foundation.

    5.  Set up dealers: [Set up dealer](set-up-dealer.md).
    6.  Assign repair claim roles: [Assign roles](assign-mco-roles.md)
2.  Work with repair claims \(OEM\): Use the Agents \(CSM/FSM\) workspace to create and manage repair campaigns, phases, and claims.
    1.  Create a repair claim: [Create a repair claim](mco-create-repair-claim.md).
    2.  Review repair claims: [Reviewing and approving repair claims](mco-approve-repair-claims.md).
3.  Work with repair claim \(Dealer\): Use the Dealer portal to submit and track repair claims.
    1.  Submit a repair claim for warranty: [Submit a repair claim for warranty](../task/mco-submit-repair-claim.md).
    2.  Submit a repair claim for recall: [Submit a repair claim for recall](../task/mco-submit-repair-claim-for-recall.md).

