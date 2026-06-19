---
title: Rolling grant approvals
description: Rolling grant approvals give grant program managers the flexibility to propose and submit funding decisions for any scored subset of applications during the Funding Allocation stage. Decisions can be submitted at any time, without waiting for the entire proposal portfolio to complete review.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/government-industry/public-sector-digital-services/psds-gm-rolling-grant-approvals-concept.html
release: australia
product: Public Sector Digital Services
classification: public-sector-digital-services
topic_type: concept
last_updated: "2026-06-08"
reading_time_minutes: 1
breadcrumb: [Grants Management, Playbooks and Solutions, Explore, Public Sector Digital Services \(PSDS\)]
---

# Rolling grant approvals

Rolling grant approvals give grant program managers the flexibility to propose and submit funding decisions for any scored subset of applications during the Funding Allocation stage. Decisions can be submitted at any time, without waiting for the entire proposal portfolio to complete review.

The **Funding Allocation** tab in the grant program workspace supports incremental decision-making alongside the traditional full-portfolio model. Grant program managers can process funding decisions as proposals are scored, grouping them into batches for Grant Program Director approval. No configuration toggle is required — both models are available by default.

From Grants Management version 1.31, you can choose to process funding decisions incrementally as proposals are scored, or continue working in the traditional full-portfolio model. No separate mode or configuration toggle is required. The rolling approval behavior is additive: customers running traditional competitive programs can continue their existing workflow unchanged. Customers with rolling programs gain the incremental processing capability they need, which is available by default.

## Key concepts

Grants Management version 1.31 introduces two new records to support rolling grant approvals.

-   **Funding Allocation Review Task** — the batch record the Grant program manager submits, storing the grant program, recommendation reason, proposal counts, allocated amount, and review state.
-   **Funding Allocation Proposal Mapping** — the record linking each proposal to its review task, with active/inactive flag to indicate the proposal state and the Grant program director comments.

A Funding Allocation Request is a record type that acts as an approval packet grouping a selected subset of proposals for Grant program director review. The funding request contains the Grant program manager’s recommendation reason and the associated budget figures. The batch can include both funding and decline recommendations. Funding requests are created automatically when the Grant program manager selects **Send for Approval** on the **Funding Allocation** tab.

Multiple funding requests can exist simultaneously for the same grant program, and each progresses through its own lifecycle independently.

## Related information

-   
-   

-   
-   

-   

-   [Grant Proposal funding statuses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/government-industry/public-sector-digital-services/psds-gm-proposal-funding-status-ref.md)


