---
title: Functional domain bulk update
description: The functional domain feature enables users to efficiently filter and sort records within a workspace based on domain-specific tags. For instance, when working in the Privacy Workspace, users can exclude records that are not tagged with privacy, allowing for a more focused view and reducing potential confusion.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tag records with functional domain, Common GRC features, Governance, Risk, and Compliance]
---

# Functional domain bulk update

The functional domain feature enables users to efficiently filter and sort records within a workspace based on domain-specific tags. For instance, when working in the Privacy Workspace, users can exclude records that are not tagged with privacy, allowing for a more focused view and reducing potential confusion.

The bulk update functionality enables users to apply or remove functional domains to multiple records simultaneously.

## Manual and automatic tagging of records

Tagging methods: Users can tag records with functional domains using two methods: manual and automatic.

-   Manual tagging: Directly selecting a functional domain for a record.
-   Automatic tagging: Functional domains are populated through a parent record and applied to child records via an overnight schedule job.

    The **Tag method** column displays whether the tagging was done manually or automatically, providing transparency in the tagging process. The **Inheritance validation** column is specific to child records. It checks if the child records are correctly inheriting the functional domain from their parent records. The system also alerts users that updating a parent record will cause the child records to be updated during a nightly job, ensuring consistency in domain inheritance.

    The following image shows the functional domain screen. The numbers in red against the tables indicate the number of records that do not have any functional domain assigned to them.

    ![The figure displays the functional domain screen where users can update functional domains for multiple records](../image/functional-domain-bulk-update.png "Functional domain bulk update")


**Parent Topic:**[Tagging records with functional domain](tagging-records-with-functional-domain.md)

