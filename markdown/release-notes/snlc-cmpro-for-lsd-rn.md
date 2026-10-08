---
title: Contract Management Pro for Legal Service Delivery
description: The ServiceNow Store Contract Management Pro for Legal Service Delivery application enables you to configure and automate the legal contract lifecycle by creating contract document templates, clauses, and clause variations. You can submit, review, finalize, and manage legal contract requests, and the application supports e-signatures and external storage systems. See the following sections for release notes by version.Contract Management Pro for Legal Service Delivery supports a contract renewal workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/snlc-cmpro-for-lsd-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-22"
reading_time_minutes: 2
breadcrumb: [Legal Service Delivery release notes, Employee Service Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Contract Management Pro for Legal Service Delivery

The ServiceNow Store Contract Management Pro for Legal Service Delivery application enables you to configure and automate the legal contract lifecycle by creating contract document templates, clauses, and clause variations. You can submit, review, finalize, and manage legal contract requests, and the application supports e-signatures and external storage systems. See the following sections for release notes by version.

## About Contract Management Pro for Legal Service Delivery

-   Configure and automate the legal contract lifecycle with reusable contract document templates, clauses, and clause variations.
-   Submit, review, finalize, and manage legal contract requests, including amendments and renewals.
-   Support secure contract execution with both electronic and wet signatures.
-   Integrate with external storage systems for contract documents.

See [Contract Management Pro for Legal Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/snlc-mgmt-pro-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Contract Management Pro for Legal Service Delivery \(sn\_lg\_cnt\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Legal Service Delivery release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/lsd-rn-landing-page.md)

## Version 3.10.1

Contract Management Pro for Legal Service Delivery supports a contract renewal workflow.

### What's new

-   **[Contract renewals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/snlc-renewal-landing.md)**

    Manage contract renewals with a dedicated Renewal request type, available alongside New contract and Amendment. Submit a renewal request for contracts due for expiry or expired contracts.

    After signature, a renewed contract repository record is created with a link to the previous contract. When a renewal is signed, a new executed contract record is created with field values copied per configuration. Track the full renewal chain from the Contract History tab of the contract repository record.


### What's changed

-   **[Intake forms availability](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/snlc-install-legal-contracts.md)**

    For new installations of Contract Management Pro for Legal Service Delivery, the base system legal intake forms — NonDisclosure Agreement, Third-Party Contract Review, and Contract Amendment and Renewal request intake forms—are hidden by default. If administrators enable these forms, they are available under **Legal Services** &gt; **Legal Agreements**.

    For existing customers, intake form behavior is preserved after upgrade. Whether the intake forms were enabled or disabled before the upgrade, that configuration remains unchanged.


