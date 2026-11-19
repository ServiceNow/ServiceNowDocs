---
title: October 2026
description: Submit and manage contract requests without a parent record, directly from the Employee Center or Contract Workspace. Contract Management Pro also introduces a renewal workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/cmpro-rn-2026-10.html
release: australia
topic_type: topic
last_updated: "2026-10-04"
reading_time_minutes: 1
breadcrumb: [Contract Management Pro release notes, Contract Management Pro release notes, Employee Service Management release notes, Features and changes by product, Release notes for upgrading from Zurich, Learn about the Australia release, Australia release notes]
---

# October 2026

Submit and manage contract requests without a parent record, directly from the Employee Center or Contract Workspace. Contract Management Pro also introduces a renewal workflow.

## What's new

-   **[Standalone contract requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-sa-submit.md)**

    Create and process a contract request without linking a parent record such as a purchase requisition or sourcing event. Initiate a standalone request from the Contract Workspace, other business unit workspaces, or the Employee Center. The Employee Center has new intake forms for new contract, amendment, and renewal requests available in the base system, accessible from **Employee Center** &gt; **Help Center** &gt; **Contracts**.

-   **[Contract renewals](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cmpro-renewal-landing.md)**

    Manage contract renewals with a dedicated Renewal request type, available alongside New contract and Amendment. Submit a renewal request for contracts due for expiry or expired contracts.

    After signature, a renewed contract repository record is created with a link to the previous contract. When a renewal is signed, a new executed contract record is created with field values copied per configuration. Track the full renewal chain from the Contract History tab of the contract repository record.

-   **[Contract Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-contract-workspace.md)**

    Contract report viewers with the sn\_cm\_core.contract\_report\_viewer role can now access the Contracts dashboard in the Contract Workspace and filter data by Request Type \(New Contract, Amendment, or Renewal\).


## What's changed

-   **[Create a contract configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-contract-config.md)**

    Configurator-managed setups support the Renewal request type through a multi-select Request Type field, without requiring duplicate configuration entries. Both admin configuration and AI feature configuration extend to cover renewals.

-   **[Initiate an amendment from a contract record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/cncore-amend-from-cntr.md)**

    Initiate an amendment from the contract workspace or from within a contract repository record.


**Parent Topic:**[Contract Management Pro release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/cmpro-rn.md)

