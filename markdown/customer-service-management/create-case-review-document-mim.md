---
title: Create a post case review for a major case
description: Create a post case review document for a resolved major case that captures the configured case information.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer Service case digests, Configure case digests, Configure case management, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a post case review for a major case

Create a post case review document for a resolved major case that captures the configured case information.

## Before you begin

Role required: sn\_customerservice\_manager, sn\_majorissue\_mgt.major\_issue\_manager, or admin

## About this task

You can create a post case review document for a resolved major case if the **sn\_customerservice.parent\_child\_case\_sync** is set to true.

**Note:** Setting this property to true disables the **Create Post Case Review** UI action for child cases.

## Procedure

1.  Open a major case in the **Resolved** state.

2.  Complete steps 2 through 7 in the [Create a post case review](create-case-review-document.md) topic.

3.  Select one of the following options.

<table id="choicetable_mg3_nhq_23b"><thead><tr><th align="left" id="d88448e87">

Option

</th><th align="left" id="d88448e90">

Description

</th></tr></thead><tbody><tr><td id="d88448e96">

**Publish to Case**

</td><td>

The system performs the following actions:1.  Syncs the child case PCR record with the parent case PCR record. \(If the child case PCR record is not present, the system creates a new child case PCR record.\) The following fields are synced:
    -   Assigned To
    -   Case Digest Configuration
    -   Short Description
    -   Root Cause Analysis
    -   Solution Provided
    -   Summary
    -   Symptoms
    -   Preventive Measures Taken
    -   Commitment Date
    -   Assignment Group
    -   State
    -   Approval Users
2.  Generates a PDF document for all of the child case PCR records with customer-specific information.
3.  Adds a link to the PCR document to the **Additional Comments** field on the child case form.


</td></tr><tr><td id="d88448e160">

**Copy to Child Cases**

</td><td>

The system syncs the child case PCR record with the parent case PCR record. \(If the child case PCR record is not present, the system creates a new child case PCR record.\) The following fields are synced: -   Assigned To
-   Case Digest Configuration
-   Short Description
-   Root Cause Analysis
-   Solution Provided
-   Summary
-   Symptoms
-   Preventive Measures Taken
-   Commitment Date
-   Assignment Group
-   State
-   Approval Users


</td></tr></tbody>
</table>
