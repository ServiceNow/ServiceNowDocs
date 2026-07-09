---
title: Supplier Lifecycle Operations release notes
description: The ServiceNow Supplier Lifecycle Operations application enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle. Supplier Lifecycle Operations was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 6
---

# Supplier Lifecycle Operations release notes

The ServiceNow® Supplier Lifecycle Operations application enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle. Supplier Lifecycle Operations was enhanced and updated in the Yokohama release.

## Supplier Lifecycle Operations highlights for the Yokohama release

**Important:**

-   Starting from the Yokohama December 2025 \(v 5.2.0\) release, the Supplier Lifecycle Operations plugin \(com.snc.sn\_supplier\_mgmt\) is renamed to Supplier Case Management. For more information, see [Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/supplier-case-management.md).
-   The new plugin Supplier Operations \(com.snc.sn\_so\) \(v 1.2.0 \) must be installed after upgrading to the Supplier Case Management Yokohama December 2025 \(v 5.2.0\) release. For more information, see [Install Supplier Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/install-supplier-ops.md).

-   Advanced case management for supplier lifecycle events including onboarding, offboarding, and ongoing operations.
-   Identify and prioritize suppliers for credit card payment adoption.
-   Estimate card payment benefits using the savings calculator tool.
-   Conduct sanction screening and validate banking details and supplier location change requests via Relish integration.
-   Map multiple internal stakeholders \(legal, business, technical, risk teams\) to suppliers to improve visibility and governance of supplier relationships.
-   Support for many-to-many \(M2M\) mapping between supplier contacts and suppliers. A single supplier contact can be the contact for multiple suppliers, if the suppliers share a parent-subsidiary relationship.
-   Automated KPI templates for automated data collection, KPI template modifications, and calculations.
-   KPI Management enhancements enable improved threshold setup, error messaging, and dashboard visualizations for KPI tracking.
-   Support for self-registration for supplier contacts. They can register with a supplier company name, enabling multiple domains under a single supplier.

See [Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/supp-mgmt-landing-page.md) for more information.

**Note:**

You can experience a longer upgrade time if you’re upgrading from Vancouver or an older release to Washington DC or any latest release. This delay is due to a mandatory script that runs for restructuring the Supplier Task \[sn\_slm\_task\] table and the duration of upgrade depends on the number of records in this table.

**Important:** Supplier Lifecycle Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Supplier Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/supplier-operations.md)**

    Supplier Operations ​ provides support for advanced case management capabilities to handle key supplier lifecycle events such as onboarding, offboarding, and ongoing operations. It includes the ability to resolve cases via Playbooks for a structured and consistent approach.

-   **[Supplier Payment Optimization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/supplier-pmnt-opt.md)**

    Supplier managers can identify, prioritize, and track suppliers with high potential for accepting credit card payments.

    -   Supplier Managers can initiate credit card enablement cases, enabling suppliers to use a credit card as their preferred payment method.
    -   They can initiate credit card enablement journey for new or existing suppliers after checking their propensity scores \(currently requires manual updates\).
    -   They can view the saving estimates associated with the card for a given supplier using the **Savings calculator** tool. They can also view the calculation details of the savings estimator formulas.

-   **[Relish Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/relish-slo-connector.md)**

    Supplier managers can conduct sanction screening, validate banking details change requests, and supplier location change requests via Relish integration.

-   **[Mapping multiple internal stakeholders to a supplier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/manage-internal-stakeholders.md)**

    This feature enhances supplier governance in SLO by enabling the mapping of multiple internal stakeholders such as legal, business, technical, and risk teams to suppliers, improving visibility and management of supplier relationships.

-   **[Universal Request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/universal-request.md)**

    Supplier contacts can create generic cases by selecting **Request Help** in the Supplier Collaboration Portal, if they can't find the relevant search results or are unsure of which department to contact for help. These cases are triaged and routed internally to appropriate case types. Universal requests remove ambiguity and improve efficiency for both suppliers and internal operations.

-   **[Overall supplier dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/overall-supplier-db.md)**

    The overall supplier performance dashboard provides detailed information about overall supplier scores, count of all active suppliers, their all-time spend, and overall risk ratings. It also includes the Supplier Insights section and the Action plans section showing relevant details.


-   **[Supplier Relationship and Performance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/supplier-performance-management-overview.md)**
    -   **Flexible KPI tracking**: Supplier managers can create KPIs directly without predefined templates, which results in simplified KPI creation, enabling faster and more efficient performance tracking.
    -   **Enhanced KPI management**: Improved threshold setup, error messaging, and dashboard visualizations for KPI tracking.
    -   **Multiple dimensions for KPI tracking**: Create supplier-level and contract-level KPIs using KPI templates to measure supplier performance. Contract-level KPIs are created under supplier-level KPIs. The overall KPI value of a supplier is calculated based on the latest aggregated values of all the related contract-level KPIs.
    -   **Action Plans for under-performing KPIs**: Address performance gaps by creating Action Plans linked to the under-performing KPIs, enabling visual tracking of milestones and tasks. The tasks triggered by the Action Plans are assigned to the suppliers and they can see and complete those tasks in the Supplier Collaboration Portal, streamlining the overall KPI remediation process.
    -   **Automated KPIs**: Enables automated data collection, KPI template modifications, and calculation at supplier and contract levels. The automated KPI system integrated into action plans can be used for comprehensive performance monitoring.
-   **[Many-to-many \(M2M\) mapping between supplier contact and suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/enable-m2m-supplier-contacts.md)**
    -   Supplier contacts can manage multiple supplier records under a single login, with the ability to toggle between records in the Supplier Collaboration Portal. One supplier contact can be the contact for multiple suppliers, provided the suppliers share a parent-subsidiary relationship.
    -   M2M mapping between supplier contact and suppliers also enables supplier contacts to register using a company name across different email domains, thus simplifying onboarding for distributed supplier teams.
    -   M2M mapping between supplier contact and suppliers is available from the Xanadu December 2024 release onwards. To enable this feature, see [Enable M2M mapping between supplier contact and suppliers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/enable-m2m-supplier-contacts.md).

-   **[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo.md)**
    -   View the summarized details of supply-related cases within the **Now Assist Panel** to keep the supplier managers and fulfillers informed about their progress and action items.
    -   Case summarization supports multiple languages.
-   **[AI driven supplier onboarding using Now Assist for SLO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/supplier-onboarding-agentic-workflow.md)**

    Use agentic AI in Now Assist for Supplier Lifecycle Operations \(SLO\) to streamline the supplier onboarding process by automating supplier registration.

-   **[Smart Assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/slo-campaign-mgmt.md)**

    Supplier managers can use the segmentation rules and assessment templates to create smart assessments in bulk for users. Smart assessments provide a survey-like experience with enhanced UI capabilities for both internal and external users. This feature utilizes the capabilities of the Smart Assessment Engine application.

-   **[Emails view for supplier managers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/enabling-emails-view-for-contacts.md)**

    Supplier managers can access their emails within the Source-to-Pay Workspace from the **Emails** tab in the case, task, and supplier details pages respectively. Email actions are reflected, incomplete email errors are handled, and email-related activities can be summarized from the workspace.

    Supplier contacts receive the emails and they can perform the assigned tasks directly via email without logging in to the Supplier Collaboration Portal.


## Deprecations

-   **[Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/supplier-manager-workspace.md)**

    Supplier Manager Workspace is being prepared for future deprecation. It’s hidden and no longer activated on new instances. Source-to-Pay Workspace provides the latest experience for this functionality.


## Activation information

Install Supplier Lifecycle Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Source-to-Pay Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/source-to-pay-operations-rn-landing.md)

