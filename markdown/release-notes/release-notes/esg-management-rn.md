---
title: Operational Sustainability Management release notes
description: The ServiceNow Operational Sustainability Management application helps you to manage all your environmental, social, and governance \(ESG\) commitments. Operational Sustainability Management was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
---

# Operational Sustainability Management release notes

The ServiceNow® Operational Sustainability Management application helps you to manage all your environmental, social, and governance \(ESG\) commitments. Operational Sustainability Management was enhanced and updated in the Zurich release.

## Operational Sustainability Management highlights for the Zurich release

-   Enable organizations to provide estimated data using pre-defined methods like average when actual data isn’t available.
-   Enhance data accuracy and governance by adding a review process for automated metric definitions.
-   Integrate real-time energy consumption data from DEX into the ESG Sustainable IT Dashboard for more accurate and reliable sustainability reporting, especially for desktops and laptops.
-   Enabled tracking and reusing narratives or statements for disclosures, making it easy to highlight specific achievements or commitments.
-   Enable creating claims directly from Microsoft Word to ServiceNow via the Microsoft 365 plugin.
-   Use enhanced entity-based access for metric definitions, metrics, metric data tasks, and metric data, enhancing data security and granular access control.
-   Create and synchronize claims automatically when uploading disclosures from Word via the ServiceNow add-in. This streamlines ESG reporting and confirming traceability across templates.
-   Avoid calculation inconsistencies caused by missing operand values. The Calculated Metric Definition Settings table enables specifying default values for operands, confirming smooth execution and flexible configuration.
-   When renaming a metric definition, there’s an option to apply the updated name to its child metrics and their associated metric data tasks.
-   Enabled audit tracking for emission factor tables and all changes are automatically logged for compliance and traceability.
-   Removed the unit restrictions between calculated metric definitions and emission factors, enabling any emission factor to be applied regardless of unit.

See [Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](https://www.servicenow.com/docs/access?context=esg-landing-page&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US) for more information.

**Important:** Operational Sustainability Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Support estimation when actual data isn’t available](https://www.servicenow.com/docs/access?context=provide-data-for-metric-data-task&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Enable organizations to provide estimated data when actual data is unavailable. Use standardized or personalized custom methods to confirm accurate and reliable ESG reporting.

-   **[Approve automated metric definitions](https://www.servicenow.com/docs/access?context=provide-data-for-metric-data-task&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Configured a new approval stage for automated metric definitions, confirming that collected data undergoes review before being added to relevant tables. This improves data accuracy and governance for automated metric definitions.

-   **[DEX integration with Sustainable IT Dashboard](https://www.servicenow.com/docs/access?context=sustainable-it-dashboard&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Real-time energy consumption data from DEX is now integrated into the ESG Sustainable IT Dashboard. This enhances sustainability reporting for IT assets, providing real-time usage trends, total energy consumption, and detailed regional and model insights, thereby supporting more accurate and actionable ESG initiatives.

-   **[Claims for reporting](https://www.servicenow.com/docs/access?context=claims-for-reporting&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Track and reuse narratives or statements for disclosures and reports. Claims play a crucial role in disclosures, highlighting key achievements and commitments while confirming actionable and credible reporting. This enhances the efficiency, consistency, and credibility of your sustainability disclosures.

-   **[Provide responses for multiple metrics](https://www.servicenow.com/docs/access?context=provide-data-for-multiple-metrics&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    This release brings multiple improvements that aim to improve the overall functionality and usability of the Operational Sustainability Management:

    -   Enhanced Metric data task filtering by approval level.
    -   Various bug fixes and UI enhancements for a better user experience.
-   **[Monitoring assessment data using ESG Management dashboards](https://www.servicenow.com/docs/access?context=monitor-data-using-esg-dashboards&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Introduction of Platform Analytics view in ESG Management for creating dashboards and reports.

-   **[Creating claims from O365](https://www.servicenow.com/docs/access?context=create-a-claim-from-microsoft-word&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Enhanced the Microsoft 365 plugin to enable creating and submitting claims directly from Microsoft Word to ServiceNow, streamlining the claims process.

-   **[Emission factor enhancements](https://www.servicenow.com/docs/access?context=usage-of-emission-factors-in-a-calculated-metric-definition&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Updated calculated metric definition calculation logic to automatically recalculate data when emission factor values change, using the new values for dates within the validity period. This confirms that the metrics data is consistent and accurate.

-   **[Forecast planning](https://www.servicenow.com/docs/access?context=scenario-analysis-forecast&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    The forecast planning now includes support for both manual and automated metric definitions and metrics, in addition to calculated metric definitions. This enhancement enables for more flexible and accurate forecasting across a wider range of metrics. You can adjust values either as absolute amounts or as percentages, making it easier to model various scenarios and anticipate future trends.

-   **[Entity based assess](https://www.servicenow.com/docs/access?context=entity-based-access&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)**

    Entity-based access aims to provide a more granular approach to data access, confirming that users can only access data through entity-based access.

    -   The entity-based access has been enabled for metrics, metric data tasks, metric data, metric data by entity and metric threshold.
    -   Administrators can grant access to an entity's related records by adding users or user groups, or by using entity user fields for entity-based access configuration.
-   **[Upload a disclosure document](https://www.servicenow.com/docs/access?context=upload-a-disclosure-document&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Claims Disclosure enables you to create and link claims directly from Word documents using the ServiceNow add-in. Once uploaded, claims are automatically synced and created in to the relevant disclosures, confirming traceability and simplifying ESG reporting.

-   **[Set default values for CMD formula operands](https://www.servicenow.com/docs/access?context=activate-default-values-for-cmd-calculations&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Default values for operands in CMD formulas can now be defined in the Calculated Metric Definition Settings table. When an operand value is missing during formula execution, the system automatically retrieves and applies the specified default value, confirming uninterrupted calculations. Default values can be customized or new records added to meet specific calculation requirements.

-   **[Update metric definition](https://www.servicenow.com/docs/access?context=update-automated-metric-definition&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    When renaming a metric definition, an option is available to apply the change to associated child metrics. Selected child metric names are updated, and their related metric data tasks automatically reflect the new name, confirming consistency across all linked elements.

-   **[Components installed with Operational Sustainability Management \(formerly ESG Management\)](https://www.servicenow.com/docs/access?context=components-installed-with-esg&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Updated ESG Management roles to update compliance feature roles. The following roles are updated:

    -   sn\_esg.data\_owner
    -   sn\_esg.program\_manager
    -   sn\_grc\_metric.admin
    -   sn\_grc\_metric.manager
    -   sn\_grc\_metric.user
-   **[ESG content accelerator](https://www.servicenow.com/docs/access?context=esg-content-accelerator&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    The Unified Content Accelerator has been renamed to Unified Content Management. Its user interface has been redesigned for improved usability and intuitive workflows, while retaining core functionality.

-   **[Emission factor library](https://www.servicenow.com/docs/access?context=emission-factor-library&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    Audit tracking is now enabled by default on Emission Factor tables, confirming that every modification is automatically recorded in a secure audit log. You can review detailed entries, including the user who initiated the change, the timestamp, the type of update, and the modified data values.

-   **[General guidelines for formula building](https://www.servicenow.com/docs/access?context=Formula-building-general-guidelines&version=zurich&pubname=zurich-environmental-social-governance&ft:locale=en-US)**

    You can now select any emission factor when creating a calculated metric definition \(CMD\), regardless of unit type. This update removes that constraint, enabling broader formula combinations and supporting sustainability scenarios where unit alignment isn’t required for calculations.


## Activation information

Install Operational Sustainability Management by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Now Assist for Operational Sustainability Management Management release notes](now-assist-for-esg-management-rn.md)**  
The ServiceNow® Now Assist for Operational Sustainability Management application brings generative AI to Operational Sustainability Management. Now Assist for Operational Sustainability was enhanced and updated in the Zurich release.

**Parent Topic:**[Features and changes by product](../new-features-changes.md)

