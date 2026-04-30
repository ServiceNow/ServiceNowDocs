---
title: Block Request Category List
description: Block Request Category List classify observables in ServiceNow based on the block or allow action selected in the CrowdStrike platform. The Category List provides options to initiate a change request for list approval. This ensures that approvals are routed and processed seamlessly as part of the Block Request capability flow.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CrowdStrike Falcon Insight integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Block Request Category List

Block Request Category List classify observables in ServiceNow® based on the block or allow action selected in the CrowdStrike platform. The Category List provides options to initiate a change request for list approval. This ensures that approvals are routed and processed seamlessly as part of the Block Request capability flow.

## Before you begin

Role required: sn\_si.analyst

**Note:** You must configure the CrowdStrike Falcon Insight configuration tile to use the Block Request Capability for CrowdStrike. For more information on how to configure the integration, see [Install and configure CrowdStrike Falcon Insight](install-and-configure-crowdstrike-falcon-insight.md)

## About this task

Create a Block or Allow request 

The Block Request Category List includes two Hash Categories.

-   Allow List Entries – Displays observables added to the Allow Hash category.
-   Block List Entries – Displays observables added to the Block Hash category.

## Procedure

1.  Navigate to **All** &gt; **CrowdStrike Falcon Insight Integration** &gt; **Block Request Category List**.

2.  Select **Allow Hash**.

3.  **Create a change request:**

    1.  Select **Create Change Request**.
    2.  Select and hold \(or right-click\) the navigation bar and select **Save**.
    3.  A change Request field is created with the Request number.
4.  **Select Approvers:**

    1.  Select **Require Approval**.
    2.  Select **Approvers for adding observable** from the search bar.
    3.  Select **Approvers for Removing Observable** from the search bar.

        For a description of the field values, see [CrowdStrike Block Request Category List](../reference/block-req-category-list.md).

5.  Select **Update**.


## Result

CrowdStrike Falcon Insight block requests can be reviewed, tracked, and responded to in Security Incident Response using standard Block Request capability flow.

