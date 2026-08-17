---
title: Implement a sales promotion setup
description: Set up sales promotions in your environment by installing the required application, configuring product models, assets, dealers, and roles, and then managing promotion campaigns and claims.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/manufacturing/mco-sales-promotion-setup.html
release: australia
topic_type: task
last_updated: "2026-07-06"
reading_time_minutes: 2
breadcrumb: [MCO core implementation, Configure, Manufacturing Commercial Operations]
---

# Implement a sales promotion setup

Set up sales promotions in your environment by installing the required application, configuring product models, assets, dealers, and roles, and then managing promotion campaigns and claims.

## Before you begin

Role required: admin or sn\_sales\_prm\_mgmt.sales\_promotion\_manager

## Procedure

1.  Review the entities and relationships within the [Sales promotion campaign data model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/sales-promotion-campaign-claims.md) application, including tables added or modified by the sales promotion plugin.

2.  Configure the sales promotion: Complete the following tasks to set up sales promotion in your environment.

    1.  Install Sales promotion claim management \[sn\_sls\_prm\_clm\_mgt\]: [Install Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/install-manufacturing-commercial-operations-core.md).

    2.  Set up product models and parts: [Configure product model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-configure-product-model.md).

    3.  Set up assets and install base items: [Configure assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-configure-assets.md) and [Configure install base item](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-create-install-base-item.md).

    4.  Set up dealers: [Set up Dealer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-dealer-setup.md).

    5.  Assign recall roles: [Assigning roles in Manufacturing Commercial Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/assign-mco-roles.md).

    6.  [Create promotion type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/create-promotion-type.md). [Create promotion questionnaire](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-create-input-set.md) [Create a checklist template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-checklist-template.md)

3.  Work with sales promotion \(OEM\): Use the Agents \(CSM/FSM\) workspace to create and manage sales promotion campaigns and review claims.

    -   [Create a sales promotion claim using playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-create-sales-promotion-claim-using-playbook.md)
    -   [Sales promotion management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-sls-pro-mgmt.md)
    -   [Sales promotion claim management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-sls-pro-clm-mgmt.md)
4.  Work with sales promotion \(Dealer\): Use the Dealer portal to submit and track sales promotion claims.

    -   [Submit a sales promotion claim](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-sales-promotion-single-claim.md)
    -   [Upload a bulk sales promotion claim](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/manufacturing/mco-sales-promotion-bulk-upload.md)

