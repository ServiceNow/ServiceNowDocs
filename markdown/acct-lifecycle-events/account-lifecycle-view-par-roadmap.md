---
title: View a product adoption roadmap
description: View and organize products or capabilities into lanes to create a visual adoption plan for customer engagements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/acct-lifecycle-events/account-lifecycle-view-par-roadmap.html
release: australia
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 3
breadcrumb: [Product adoption, Customer success, Use, Customer Success Management]
---

# View a product adoption roadmap

View and organize products or capabilities into lanes to create a visual adoption plan for customer engagements.

The product adoption roadmap is displayed as a visual board that organizes product usages and product capability usages into lanes based on your selected phase field. Each lane contains cards representing products or capabilities, showing key adoption metrics and status information.

\[Omitted image "product-adopt-roadmap.jpg"\] Alt text: Product adoption roadmap

## Product adoption roadmap header

The header section displays the following:

-   Roadmap name and description: Identifies the roadmap and its purpose
-   State: Shows whether the roadmap is in **Draft** or **Published** state
-   Phase field: The field used to organize lanes \(for example, Business criticality, Customer priority\)
-   Planning object: Indicates whether the roadmap organizes Product Usage or Capability Usage
-   Last updated: Date the roadmap was last modified
-   Template: Shows the template name if the roadmap was created from a template. See [Define a product adoption roadmap template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-create-par-roadmap-temp.md) for details.
-   Version: Shows the version label of the currently published roadmap state.

## Product adoption roadmap lanes

The roadmap displays lanes based on the value selected in the Phase field. The Phase field contains choice fields from the product or capability usage records, such as Business criticality, Customer priority, and Activation status. Each choice field has its own set of values that determine the lane headings. For example, selecting Business criticality creates lanes for Critical, High, Medium, Low, and Nice to have.

Each card displays the following:

-   Product or capability name: The item being tracked. You can drill down to the product or capability usage page.
-   Type: Product or capability designation
-   Adoption score: Percentage and rating
-   Adoption priority: Priority level
-   Usage plan: Current usage status.
-   Success objectives: Number of associated objectives and outcomes achieved

## Product adoption roadmap states

The roadmap can be in one of the following states:

-   Draft: You can edit and reorganize the roadmap when it is in this state. Select a card, drag and drop it into a different lane. The changes are automatically saved.
-   Published: Roadmap is in finalized state. Select **Edit** to switch to Draft state to make changes.
-   Canceled: Roadmap is no longer active and cannot be used.
-   Retired: Roadmap has been archived.

## Product adoption roadmap versions

Each time a roadmap is published, the system creates a version record that captures an immutable snapshot of the roadmap at that point in time. Version records are read-only and copy-safe.

The **Versions** related list on the roadmap record displays all published versions. Each version record shows the following:

-   Version: An editable label that identifies the version. The system automatically sets this to a major.minor format based on the internal version number \(for example, `1.0 Roadmap name`\). You can customize this label.
-   Internal version: A read-only integer that increments by 1 each time the roadmap is published. This field is not visible to end users and is used for internal tracking only.
-   Snapshots: JSON representations of the roadmap header, lanes, and items at the time of publishing. These fields are read-only.
-   Previous version: A reference to the version record that preceded this one, providing a full lineage chain.

To revert the roadmap to a previous version, see [Revert a product adoption roadmap to a previous version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-revert-par-roadmap.md).

-   **[Product adoption roadmap versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-par-versioning.md)**  
Versioning preserves a snapshot of your roadmap each time you publish it, creating a complete history you can review or restore when plans change.
-   **[Revert a product adoption roadmap to a previous version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-revert-par-roadmap.md)**  
Restore a product adoption roadmap to the state captured in a previous published version.

**Parent Topic:**[Product adoption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-use-product-adopt.md)

**Related topics**  


[Product adoption roadmap](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-par-roadmap.md)

[Product adoption roadmap versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-par-versioning.md)

[Revert a product adoption roadmap to a previous version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/acct-lifecycle-events/account-lifecycle-revert-par-roadmap.md)

