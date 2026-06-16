---
title: Accounts Payable Invoice Processing release notes
description: Version history for the Accounts Payable Invoice Processing application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-rn-hr-accounts-payable-invoice-processing.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 7
breadcrumb: [ServiceNow Store - Accounts Payable Operations release notes, ServiceNow Store - Source-to-Pay Operations release notes, ServiceNow Store release notes]
---

# Accounts Payable Invoice Processing release notes

Version history for the Accounts Payable Invoice Processing application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 13.0.1 - June 2026**
    -   Enhanced exception definitions with configurable rejection modes \(Auto/Manual\) to automatically reject or stage invoices for review, with structured audit messages and supplier notifications generated on every exception execution.
    -   New condition builder enables exceptions to be scoped to specific suppliers, legal entities, or invoice attributes — reducing false positives and improving exception precision.
    -   Accounts Payable Operations now automatically detects and flags invoices received from unregistered or unknown sender email addresses as an "Unverified Sender Source" exception, enabling AP teams to take structured resolution actions directly from the AP Workbench.
-   **Version 11.2.1 - June 2026 \(Zurich\)**
    -   Enhanced exception definitions with configurable rejection modes \(Auto/Manual\) to automatically reject or stage invoices for review, with structured audit messages and supplier notifications generated on every exception execution.
    -   New condition builder enables exceptions to be scoped to specific suppliers, legal entities, or invoice attributes — reducing false positives and improving exception precision.
    -   Accounts Payable Operations now automatically detects and flags invoices received from unregistered or unknown sender email addresses as an "Unverified Sender Source" exception, enabling AP teams to take structured resolution actions directly from the exception.
-   **Version 9.3.1 - June 2026 \(Yokohama\)**
    -   Enhanced exception definitions with configurable rejection modes \(Auto/Manual\) to automatically reject or stage invoices for review, with structured audit messages and supplier notifications generated on every exception execution.
    -   New condition builder enables exceptions to be scoped to specific suppliers, legal entities, or invoice attributes — reducing false positives and improving exception precision.
    -   Accounts Payable Operations now automatically detects and flags invoices received from unregistered or unknown sender email addresses as an "Unverified Sender Source" exception, enabling AP teams to take structured resolution actions directly from the exception.
-   **Version 12.0.1 - March 2026**
    -   Automatically classifies incoming supplier email attachments as invoices, credit memos, or supporting documents upfront, ensuring only valid invoices proceed to extraction and reducing incorrect case creation and manual rework.
    -   Third‑party tax integration: Integrates Accounts Payable Operations with external tax engines to automatically calculate, validate, and generate tax lines on invoices, improving accuracy, compliance, and straight‑through invoice processing
-   **Version 11.1.1 - March 2026 \(Zurich\)**
    -   Automatically classifies incoming supplier email attachments as invoices, credit memos, or supporting documents upfront, ensuring only valid invoices proceed to extraction and reducing incorrect case creation and manual rework.
    -   Third‑party tax integration: Integrates Accounts Payable Operations with external tax engines to automatically calculate, validate, and generate tax lines on invoices, improving accuracy, compliance, and straight‑through invoice processing
-   **Version 9.2.1 - March 2026 \(Yokohama\)**
    -   Automatically classifies incoming supplier email attachments as invoices, credit memos, or supporting documents upfront, ensuring only valid invoices proceed to extraction and reducing incorrect case creation and manual rework.
    -   Third‑party tax integration: Integrates Accounts Payable Operations with external tax engines to automatically calculate, validate, and generate tax lines on invoices, improving accuracy, compliance, and straight‑through invoice processing
-   **Version 11.0.4 - December 2025**
    -   Distribution sets: This capability automates cost allocation across invoice lines using predefined templates based on supplier, country, invoice type, or ledger account etc. It works for both PO and non-PO invoices and ensures clear traceability of allocation sources. Distribution sets can be applied manually by AP specialists or automatically based on matching criteria. Once applied, allocation records are generated instantly.
    -   Reference Data Integrity. Ensures invoices use accurate, consistent reference data across ERP systems by validating source alignment during creation. Prevents mismatches that cause posting failures and manual rework. Applies to invoices created via API, Manual, and DocIntel processes.
    -   Improved accuracy for three exception types: Insufficient Goods Receipt, Insufficient Funds \(line and header\). Reduces false positives and streamlines processing.
-   **Version 9.1.1 - December 2025 \(Yokohama\)**
    -   Distribution sets: This capability automates cost allocation across invoice lines using predefined templates based on supplier, country, invoice type, or ledger account etc. It works for both PO and non-PO invoices and ensures clear traceability of allocation sources. Distribution sets can be applied manually by AP specialists or automatically based on matching criteria. Once applied, allocation records are generated instantly.
    -   Reference Data Integrity. Ensures invoices use accurate, consistent reference data across ERP systems by validating source alignment during creation. Prevents mismatches that cause posting failures and manual rework. Applies to invoices created via API, Manual, and DocIntel processes.
    -   Improved accuracy for three exception types: Insufficient Goods Receipt, Insufficient Funds \(line and header\). Reduces false positives and streamlines processing.
-   **Version 10.0.0 - August 2025**
    -   Invoice Type Conversion and Reprocessing
        -   AP Specialists can manually change invoice types \(e.g. from non-PO to PO\), triggering reprocessing and re-validation from draft status.
    -   Enhanced Invoice Exceptions
        -   The valid coding required exception now accommodates cost distribution across multiple ledgers or cost centers.
        -   GL/Cost Center validation is bypassed at invoice line when invoice line cost is distributed across multiple GLs or CCs.
        -   When cost is split across multiple cost centers, the CC field on the invoice line becomes read-only \(same for GL\) and allows one type of allocation type in cost allocations
        -   New Exception Type: Introduced a dedicated exception for missing tax code details, tax code validation is separated from the “Valid coding required” exception.
    -   Improved Exception Handling for ITAM-Driven Invoices
        -   As part of ITAM and SPO better together process, during ITAM PO-based invoice processing, APO validates receipt quantity and notifies assigned users in ITAM PO if the required quantity has not been received.
-   **Version 9.0.5 - May 2025**
    -   New:
        -   Improved Invoice Extraction: Leveraging DocIntel with GPT-4.0, invoice extraction accuracy has been significantly improved.
        -   AI-Powered Purchase Order Line Mapping: A new GenAI-based feature improves purchase order line matching accuracy, boosting overall productivity.
        -   Admin configuration for PO Mapping: Customers can now enable or disable purchase order \(PO\) mapping based on their specific needs.
        -   New Invoice Exception: Added a new exception type, "Missing Required Information - Invoice Lines", to help identify and address incomplete invoices more effectively.
    -   Fixed: Improved the invoice ingestion process to allow manual invoice creation when the DocIntel service is temporarily unavailable.
-   **Version 8.0.2 - February 2025**

    Provided an API enabling invoice ingestion from external systems. API supports XML formats.

-   **Version 7.0.2 - November 2024**
    -   Provided cost allocation feature enabling distribution of invoice line cost across different cost centers, ledger accounts etc.
    -   Provided an API enabling invoice ingestion from external systems. API supports cXML and JSON formats.
-   **Version 6.0.3 - August 2024**
    -   New: Provided tax compliance feature enabling accounts payable specialist/tax specialist to validate and verify the tax provided by supplier.
    -   Fixed: Resolved the issue which was causing the DocIntel screen to open in a new tab in the workspace instead of opening it as sub tab within the invoice processing case.
-   **Version 5.0.1 - June 2024**

    Fixed: Resolved an issue related to conversion of invoice type from "PO invoice" to "Non-PO credit memo".

-   **Version 5.0.0 - May 2024**
    -   New:
        -   Improved the workflow to support credit memo invoice processing.
        -   Introduced guided invoice processing experience to enhance experience and visibility for AP specialist, aiming to improve efficiency in resolving errors.
        -   Introduced error handling flow allowing accounts payable team to review and resolve integration errors related to invoice posting in the ERP system.
        -   Improved workflow allowing AP specialist to modify and re-submit invoices rejected by business owners.
-   **Version 4.0.1 - February 2024**
    -   New:
        -   Introduced new workflows and staging tables in the integrations framework for third-party sourcing tools to integrate with Accounts Payable Operations for invoice posting, invoice ingestion and invoice payment ingestion use cases.
        -   Introduced new supplier notification in case invoice is found to be duplicate.
    -   Changed invoice line deletion experience.
-   **Version 3.0.1 - November 2023**
    -   New:
        -   Define tolerance rules, which will be applied to the variances between invoice and matched purchase order, and will help in reducing the number of exceptions.
        -   Sidebar and Microsoft Teams integration is now available on all APO objects that have extended from the task tables, such as Invoice case, invoice task. This feature will improve the collaboration between the accounts payable team and cross-functional stakeholders and will expedite the exception resolution
-   **Version 2.0.2 - August 2023**
    -   New:
        -   Improved supplier experience by allowing to manage and submit new invoices from ServiceNow Supplier Collaboration Portal
        -   Enabled accounts payable team to process Non-PO invoices
        -   New OOTB exceptions that are applicable for both PO and Non-PO invoices
        -   Minor bug fixes
    -   Changed:
        -   Updated PO matching rules to improve touchless automation
        -   Updated exception engine performance
-   **Version 1.0.1 - May 2023**

    The ServiceNow Accounts Payable Invoice Processing application helps automate the end-to-end process from invoice ingestion through, purchase order matching, exception resolution, and approval. Maintain visibility into the process to identify bottlenecks and reduce risk.


