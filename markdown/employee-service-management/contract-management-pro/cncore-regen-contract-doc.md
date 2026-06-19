---
title: Regenerate contract document after modifying request
description: As a contract user or contract fulfiller, regenerate the contract document for self-served requests when the parent request has been modified.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/contract-management-pro/cncore-regen-contract-doc.html
release: zurich
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use self-served contract request, Use, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Regenerate contract document after modifying request

As a contract user or contract fulfiller, regenerate the contract document for self-served requests when the parent request has been modified.

## About this task

When the parent request is modified, you can use the **Regenerate** option to generate a new contract document from the contract template with the latest metadata, signatories, and tables. You can regenerate a contract document only when the State is Draft or Work in progress.

Any changes made to the signatory information in the contract request will be overwritten by the signatory information from the contract template. If the signatory information is incomplete or inconsistent after regeneration, you can manually update the signatories. For more information, see [Updating and synchronizing signatories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/contract-management-pro/cncore-update-sync-signatories.md).

## Before you begin

Role required: sn\_cm\_core.contract\_fulfiller or sn\_cm\_core.contract\_user

## Procedure

1.  Navigate to your workspace.

2.  Open the contract request.

3.  Select the More Actions icon \(\[Omitted image "more-button-icon.png"\] Alt text: More Actions icon\) and select **Regenerate**.

    \[Omitted image "cmpro-regenerate-doc.png"\] Alt text: Regenerate contract document in a contract request


## Result

The results of the regeneration depends on the initial state of the document:

-   Draft: Replaces the existing contract document revision.
-   Work in progress: Creates a new contract document revision. Any changes made in the previous revision are discarded.

Note that although contract fulfillers can see all contract document revisions, a contract user can see only the latest revision.

**Parent Topic:**[Use self-served contract request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown)

