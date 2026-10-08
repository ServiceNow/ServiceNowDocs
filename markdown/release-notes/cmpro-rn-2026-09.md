---
title: September 2026
description: Contract Management Pro supports parallel signing, enabling you to group signatories to sign a contract at the same time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/cmpro-rn-2026-09.html
release: australia
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [parallel signing order, parallel signature, signing order, sequential order, Wet/Offline signature, Signatories tab, Contract Workspace, DocuSign, AdobeSign]
breadcrumb: [Contract Management Pro release notes, Contract Management Pro release notes, Employee Service Management release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# September 2026

Contract Management Pro supports parallel signing, enabling you to group signatories to sign a contract at the same time.

## What's new

-   **[Support for parallel signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-signature-workflow.md)**

    Enable parallel signing by assigning the same signing order to multiple signatories. Signatories with the same signing order receive signature requests at the same time and can complete their signatures independently. Signatory statuses update individually as each signatory signs, declines, or takes other actions.

    **Note:** Parallel signing is supported for electronic signatures.


## What's changed

-   **[Assign a signing order while adding a signatory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-update-sign-ss-cmr.md)**

    The **Signatory order** field on the Add signatory form is editable. Assign a unique signing order to each signatory for sequential signing, or assign the same signing order to multiple signatories for parallel signing.

-   **[Modify the signing order on the Signatories related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-set-signing-order.md)**

    Set the signing order for a signatory by entering a number directly in the **Signatory order** column on the Signatories related list in Contract Workspace. The **Reorder** option is not available to modify the signing orders.

-   **[Signing order gaps and parallel grouping corrected automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-signature-workflow.md)**

    When you change a contract signing method from electronic signature to wet signature, signatories with the same signing order are assigned unique sequential signing order, and any gaps in the signing order are removed.

    When you select **Send for signature** or **Prepare for signature**, any gaps in the signing order are automatically removed.


**Parent Topic:**[Contract Management Pro release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/cmpro-rn.md)

