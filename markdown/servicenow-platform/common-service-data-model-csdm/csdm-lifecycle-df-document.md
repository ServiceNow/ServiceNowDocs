---
title: Life cycle value definitions for document and contract entities
description: The Life Cycle Stage and Life Cycle Stage Status values for the document and contract life-cycle process are visible only in tables related to document entities in Contracts and CMDB.
locale: en-US
release: yokohama
product: Common Service Data Model \(CSDM\)
classification: common-service-data-model-csdm
topic_type: reference
last_updated: "2025-05-07"
reading_time_minutes: 1
breadcrumb: [Reference, CSDM, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Life cycle value definitions for document and contract entities

The Life Cycle Stage and Life Cycle Stage Status values for the document and contract life-cycle process are visible only in tables related to document entities in Contracts and CMDB.

## Definitions of document and contract life cycle stage and life cycle stage status values

![Relationships between CSDM stages and life cycle values.](../image/csdm-lifecycle-vp-doc-contract.png)

-   **Ideation life cycle stage**

    The materials are in initial draft form.

    -   **Draft**: The document or contract is in the initial creation and editing process.
    -   **Under Evaluation**: After creation, the materials are reviewed before activation as operational in use or published.
-   **Operational life cycle stage**

    The materials are in active use.

    -   **In Use**: The document or contract is in active operational status before first renewal
    -   **Published**: After approval for release, publication is the formal act of making the materials visible for consumption.
    -   **Renewal in Process**: For an existing contract that is set to expire, the effort to renew the contract is occurring.
    -   **Renewed**: The contract has been renewed.
    -   **Pending Retirement**: The document, such as contract, has a pending expiration/end date or expiration date.
-   **End of Life life cycle stage**

    The document or contract is no longer active.

    -   **Expired**: Date-limited material such as contracts that are past their expiration date.
    -   **Retired**: Materials that are no longer needed by the organization.

**Parent Topic:**[CSDM reference](../concept/csdm-content-frame-reference.md)

