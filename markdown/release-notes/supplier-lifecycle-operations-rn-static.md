---
title: Supplier Lifecycle Operations release notes
description: ServiceNow Supplier Lifecycle Operations enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle.The Brazil Early Availability release introduces FedEx Dataworks integration to enable relationship managers assess supplier risk during onboarding, and benchmark supplier performance — without leaving the supplier workspace. The AI L1 SLO Service Desk Specialist enables quick resolution for general inquiry cases.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/supplier-lifecycle-operations-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 5
keywords: [supplier, supplier lifecycle, supplier performance, supplier workspace, supplier operations, Supplier collaboration, Supplier collaboration portal, Supplier Collaboartion portal, Relish, FedEx Dataworks, Otto, Now Assist summarization]
breadcrumb: [Source-to-Pay Operations release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Supplier Lifecycle Operations release notes

ServiceNow® Supplier Lifecycle Operations enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle.

## About Supplier Lifecycle Operations

Supplier Lifecycle Operations enables you to onboard suppliers quickly, effortlessly manage supplier data, add key supplier contacts, monitor supplier performance, and enhance the productivity of the teams that engage with suppliers.

Supplier Lifecycle Operations provides the following benefits:

-   Faster supplier onboarding: View details about new suppliers and onboard suppliers quickly using onboarding workflows and start purchasing goods and services.
-   Automatically import supplier information: Supplier Lifecycle Operations integrates with the supplier Intelligence platform, Craft, which enables you to import and view all the important supplier details.
-   Supplier self-service: Enhance the supplier experience by enabling suppliers to complete onboarding tasks, get their questioned answered, and fulfill requests, such as viewing open purchase orders and submitting invoices.
-   Supplier data management: Provide flexibility to suppliers to manage and update their own data, ensuring that the supplier data is current and up to date.
-   Supplier case and contact management: Create and manage supplier cases, add, and manage supplier contacts.
-   Minimize risk during supplier onboarding: Identify and assess potential supplier risks when onboarding new suppliers.
-   Manage supplier relationship and performance: Monitor and assess supplier performance by setting up criteria for measuring supplier performance though KPIs and thresholds.

For an overview of Supplier Lifecycle Operations capabilities, see [Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/supp-mgmt-landing-page.md).

## Activation and other requirements

**Note:** Supplier Lifecycle Operations is available in the ServiceNow Store.

-   **Activation information**

    Request Supplier Lifecycle Operations from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Source-to-Pay Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/source-to-pay-operations-rn-landing.md)

## Brazil Early Availability

The Brazil Early Availability release introduces FedEx Dataworks integration to enable relationship managers assess supplier risk during onboarding, and benchmark supplier performance — without leaving the supplier workspace. The AI L1 SLO Service Desk Specialist enables quick resolution for general inquiry cases.

### What's new

-   **[FedEx Dataworks Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/fedex-dataworks-overview.md)**

    FedEx Dataworks combines unmatched, proprietary real-world data signals with advanced analytics to power ServiceNow's Source-to-Pay workflows. Relationship managers can use these signals during supplier onboarding to validate suppliers, evaluate risk, and benchmark supplier performance — without leaving the supplier workspace.

    The FedEx Dataworks integration includes the following features:

    -   **Supplier validation in supplier onboarding Registration stage**: Verifies a supplier's details against FedEx Dataworks records to establish a FedEx Dataworks Supplier ID. This step is part of the supplier onboarding playbook and is required before risk assessment or performance benchmarking data can be retrieved.
    -   **FedEx Dataworks risk assessment in supplier onboarding Qualification stage**: Returns risk factor ratings for a matched supplier, covering customs risk, restricted country screening, and dangerous goods risk. Risk assessment is available in the supplier onboarding playbook after a successful supplier match.
    -   **Supplier performance benchmarking**: Retrieves FedEx Dataworks logistics performance metrics for a matched supplier, displayed in a dedicated section on the supplier profile page.
-   **[AI L1 SLO Service Desk Specialist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/ztsd-agent-slo.md)**

    The AI L1 SLO Service Desk Specialist is a fully autonomous help desk automation solution that resolves supplier inquiries without manual intervention from a fulfiller.

    For general inquiry cases, the AI L1 SLO Service Desk Specialist retrieves relevant information from published knowledge base articles and the FSC Common KG Tags added under the Enterprise knowledge graph to investigate the issue.

-   **[Generate a knowledge article from a closed supplier case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/generate-article-case.md)**

    Generate, review, and publish knowledge articles from closed supplier cases using ServiceNow Otto for SLO.

-   **[Generate a knowledge article from multiple closed cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/generate-article-multiple-cases.md)**

    Generate, review, and publish a knowledge article from multiple closed supplier cases using ServiceNow Otto for SLO.

-   **[Verify tax information change request using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/validate-tax-information.md)**

    Relish is a third-party supplier intelligence platform that validates supplier data while working on supplier cases.

    When a tax information change request is assigned to a supplier manager and they start working on it, they can verify the tax details using Relish.

-   **[View supplier sanction status using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/view-supplier-sanction-status.md)**

    Supplier managers can view the sanction status and last sanction check date for suppliers from the Manage Suppliers list.

    These fields in the supplier list are available regardless of whether Relish is installed or not, but are updated only when Relish is integrated. If Relish is not integrated, users can edit the field manually if they want.


### What's changed

-   **[Verify bank account ownership using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/verify-banking-information.md)**

    When a banking details change request is assigned to a supplier manager and they start working on it, they can verify the details using Relish.

    By default, bank validation checks only the bank routing number and address details. Relish also verifies the bank account number and account ownership information when bank account ownership validation is enabled.

-   **[Conduct bulk sanction screening using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/perform-bulk-sanction-screening.md)**

    When a sanction screening request for compliance verification is assigned to a supplier manager and they start working on it, they can verify the details using Relish.

    Supplier managers can conduct sanction screening for multiple suppliers simultaneously using the bulk sanction screening feature.

-   **[AI driven supplier onboarding using ServiceNow Otto for SLO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/source-to-pay-operations/supplier-onboarding-agentic-workflow.md)**
    -   Leverages Web search results to generate a supplier scorecard highlighting key strengths, positive indicators, and potential risk signals.
    -   If Craft is configured, the workflow leverages the Craft integration to generate a comprehensive, normalized supplier scorecard and risk assessment. It provides a structured evaluation of the supplier’s overall profile and associated risk factors.
    -   If Relish is integrated, the supplier's banking information is further validated and synchronized with Relish.

### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Gemma 4 joins our growing portfolio of open-weight models available through Now LLM Service. The latest industry advancements are available alongside sovereignty-focused options. All models are hosted and governed by ServiceNow with the same infrastructure and data protections. Older models will remain available for existing published AI skills, agents, and agentic workflows, but will no longer be available for new development or configuration. For details, see the [KB3066214: ServiceNow Otto Model Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3066214) article in the Now Support Knowledge Base.


