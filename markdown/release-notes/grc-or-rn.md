---
title: Operational Resilience release notes
description: The ServiceNow Operational Resilience application helps organizations maintain business services during adverse events, such as pandemics, severe weather, or cyber attacks. See the following sections for release notes by version.Operational Resilience, version 23.0.9 enhances Digital resilience incident reporting \(DRIR\) assessment cases with role-based contributor and collaborator assignment controls. It strengthens regulatory compliance and data quality for Digital Operational Resilience Act \(DORA\) reporting through controlled access and better management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/grc-or-rn.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Governance, Risk, and Compliance release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Operational Resilience release notes

The ServiceNow® Operational Resilience application helps organizations maintain business services during adverse events, such as pandemics, severe weather, or cyber attacks. See the following sections for release notes by version.

## About Operational Resilience

-   Identify, assess, and monitor operational risks across people, processes, systems, and external dependencies to understand impact on critical business services and customer outcomes.
-   Develop and execute resilience strategies, conduct scenario testing, and track remediation actions to strengthen your organization's ability to withstand and recover from operational disruptions.

See [Operational Resilience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/grc-opres-landing-page.md) for more information.

## Activation and other requirements

-   **Activation information**

    Install Operational Resilience by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

-   **Upgrade information**

    If you're upgrading from an earlier release, upgrade sequentially through each release rather than skipping versions. Upgrade scripts depend on running in order, and skipping releases can cause data inconsistencies or broken functionality.


**Parent Topic:**[Governance, Risk, and Compliance release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/grc-rn-landing.md)

## Version 23.0.9

Operational Resilience, version 23.0.9 enhances Digital resilience incident reporting \(DRIR\) assessment cases with role-based contributor and collaborator assignment controls. It strengthens regulatory compliance and data quality for Digital Operational Resilience Act \(DORA\) reporting through controlled access and better management.

### What's new

-   **[Enable contributor assignment in DRIR assessment cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/work-on-action-tasks.md)**

    Assign contributor and collaborator roles to streamline multi-stakeholder DRIR investigations. You can now assign contributors and collaborators to DRIR assessment instances, with role-based access controls ensuring appropriate team members can participate. This simplifies accountability and coordination during incident responses.

-   **[Tracking field-level changes in linked source records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/integration-with-incident-management.md)**

    Maintain DRIR cases current with evolving incident data by tracking field-level changes in linked source records. The application detects modifications to incidents after case creation, generates audit trail records with complete change details, and displays pending updates in a banner within the workspace.

-   **[Enhance regulatory compliance and data quality for DORA reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/properties-dora.md)**

    Improve financial data accuracy with better decimal handling, automated snapshot exports, and data quality warnings.

-   **[Define terminology for ROI export](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/opres-dora-roi-ter-def.md)**

    Document register-of-information terminology directly in the workspace. Only the **Description** field is editable for each term. Term definitions are automatically included in the `B_99.01` CSV export through a scheduled quarterly job.

    The scheduled job that generates this export is inactive by default; an administrator must activate it before it runs. The default frequency is quarterly, but administrators can adjust it. No email notification is sent for this job, because it runs as a system action rather than a user-initiated action.


### What's changed

-   **[Pending updates displayed in the banner](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/integration-with-incident-management.md)**

    The pending updates for the DRIR case are displayed in a banner within the workspace.

-   **[Decimal precision for DORA monetary values](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/opres-dora-validate-roi.md)**

    Monetary value fields now support up to two decimal places. Previously, only zero or negative values were accepted, with all monetary values defaulting to zero. Values greater than zero are no longer rounded down to zero during download.

-   **[CSV download only references applied filters when selecting all records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-excel-upload-download-request.md)**

    When a filter is applied to a list and users select all records for CSV download, only the filtered records are included. Previously, all records were downloaded regardless of the applied filter.

-   **[Impact analysis correctly resolves Profile records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/scheduled-jobs-installed-with-or.md)**

    Previously, impact analysis failed to resolve entities when a scheduled job processed GRC Profile records directly. This issue has been fixed. Impact analysis now correctly resolves Profile records in Operational Resilience and entity resolution completes as expected for all record types.

-   **[Rank 1 supply chain records update automatically when a contract's service provider changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-drtp-reg-supply-chain.md)**

    If you change the service provider on a DORA contract record, the associated Rank 1 supply chain records update automatically. The records reflect the new provider or recipient.

-   **[Excel export for DORA Functions requests no longer fails on large datasets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-excel-upload-download-request.md)**

    Exporting a Functions-type Excel drop-down download and upload request no longer fails when drop-down fields reference large CMDB or reference tables. Results are capped at 10,000 records per drop-down field.

-   **[Parent record navigation added to DORA third-party and contract records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/create-new-cont-arrange-form.md)**

    A reference field is available on DORA third-party and third-party engagement records. Use it to navigate back to the originating contract record after arriving from a related list. Previously, there was no way to return to the parent contract or company record from these pages.

-   **[Notice period fields accept a value of zero](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/tprm-validation-roi.md)**

    The notice period fields \(`B_02.02.0100` and `B_02.02.0110`\) now accept a value of `0`. Previously, a value of `0` was rejected as if the field were empty.


