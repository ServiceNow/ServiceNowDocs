---
title: Contract Management Pro
description: The ServiceNow Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract, amendment and renewal requests. The solution uses AI to analyze contracts and extract metadata. It also supports e-signatures, wet signatures, and external storage systems. See the following sections for release notes by version.Contract Management Pro adds standalone contract requests, direct contract submission from the Employee Center, and a contract renewal workflow.Contract Management Pro supports parallel signing, enabling you to group signatories to sign a contract at the same time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/contract-management-pro-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [standalone contract request, Employee Center intake, contract renewal, renewal request type, Contract Workspace, parent field, configurator, Renewal History, parallel signing order, parallel signature, signing order, sequential order, Wet/Offline signature, Signatories tab, Contract Workspace, DocuSign, AdobeSign]
breadcrumb: [Contract Management Pro release notes, Employee Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Contract Management Pro

The ServiceNow® Contract Management Pro solution enables you to set up contract document templates, clauses, and clause variations, and to initiate contract, amendment and renewal requests. The solution uses AI to analyze contracts and extract metadata. It also supports e-signatures, wet signatures, and external storage systems. See the following sections for release notes by version.

## About Contract Management Pro

-   Reduce contract turnaround time by automatically generating contracts from dynamic Word templates, with clauses, tables, and signatories populated based on predefined conditions.
-   Support secure contract execution with both electronic and wet signatures, using integrations with e-signature providers such as Adobe Acrobat Sign and Docusign.
-   Maintain a centralized contract repository with automated reminders for upcoming renewals and terminations.
-   Create and track obligation tasks, with timely reminders to ensure all contractual commitments are fulfilled.
-   Gain visibility into contract volume and streamline day-to-day work with a contract workspace and dashboard.

See [Contract Management Pro](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-cmpro-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Contract Management Pro by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Contract Management Pro release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/cmpro-landing-page.md)

## Version 1.7.15

Contract Management Pro adds standalone contract requests, direct contract submission from the Employee Center, and a contract renewal workflow.

### What's new

-   **[Standalone contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-sa-submit.md)**

    Create and process a contract request without linking a parent record such as a purchase requisition or sourcing event. Initiate a standalone request from the Contract Workspace, other business unit workspaces, or the Employee Center. The Employee Center has new intake forms for new contract, amendment, and renewal requests available in the base system, accessible from **Employee Center** &gt; **Help Center** &gt; **Contracts**.

-   **[Contract renewals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cmpro-renewal-landing.md)**

    Manage contract renewals with a dedicated Renewal request type, available alongside New contract and Amendment. Submit a renewal request for contracts due for expiry or expired contracts.

    After signature, a renewed contract repository record is created with a link to the previous contract. When a renewal is signed, a new executed contract record is created with field values copied per configuration. Track the full renewal chain from the Contract History tab of the contract repository record.

-   **[Contract Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-contract-workspace.md)**

    Contract report viewers with the sn\_cm\_core.contract\_report\_viewer role can now access the Contracts dashboard in the Contract Workspace and filter data by Request Type \(New Contract, Amendment, or Renewal\).


### What's changed

-   **[Create a contract configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-contract-config.md)**

    Configurator-managed setups support the Renewal request type through a multi-select Request Type field, without requiring duplicate configuration entries. Both admin configuration and AI feature configuration extend to cover renewals.

-   **[Initiate an amendment from a contract record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-amend-from-cntr.md)**

    Initiate an amendment from the contract workspace or from within a contract repository record.


## Version 1.7.13

Contract Management Pro supports parallel signing, enabling you to group signatories to sign a contract at the same time.

### What's new

-   **[Support for parallel signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-signature-workflow.md)**

    Enable parallel signing by assigning the same signing order to multiple signatories. Signatories with the same signing order receive signature requests at the same time and can complete their signatures independently. Signatory statuses update individually as each signatory signs, declines, or takes other actions.

    **Note:** Parallel signing is supported for electronic signatures.


### What's changed

-   **[Assign a signing order while adding a signatory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-update-sign-ss-cmr.md)**

    The **Signatory order** field on the Add signatory form is editable. Assign a unique signing order to each signatory for sequential signing, or assign the same signing order to multiple signatories for parallel signing.

-   **[Modify the signing order on the Signatories related list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-set-signing-order.md)**

    Set the signing order for a signatory by entering a number directly in the **Signatory order** column on the Signatories related list in Contract Workspace. The **Reorder** option is not available to modify the signing orders.

-   **[Signing order gaps and parallel grouping corrected automatically](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/cncore-signature-workflow.md)**

    When you change a contract signing method from electronic signature to wet signature, signatories with the same signing order are assigned unique sequential signing order, and any gaps in the signing order are removed.

    When you select **Send for signature** or **Prepare for signature**, any gaps in the signing order are automatically removed.


