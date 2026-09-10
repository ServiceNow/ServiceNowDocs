---
title: CMDB success advisor release notes
description: Version history for the ServiceNow CMDB success advisor application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-rn-success-advisor.html
release: store
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes, ServiceNow Store - ServiceNow AI Platform Capabilities version history release notes, ServiceNow Store version history release notes]
---

# CMDB success advisor release notes

Version history for the ServiceNow® CMDB success advisor application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

-   **Version 3.1.1 - September 2026**
    -   New:
        -   Added a data quality summary, ranked by number of affected CIs \(data integrity issues first, then missing attributes, then governance gaps\), to the SAM advisor dashboard for CMDB success advisor for SAM.
        -   Added scope selection logic to CMDB success advisor for SAM.
        -   Added a CI class categories filter to the advisor dashboard for CMDB success advisor for Data Foundations.
        -   Added a Reset filters option to each product's advisor dashboard \(HAM, SAM, and Data Foundations\). Filter selections persist for the session until reset.
    -   Changed:
        -   Removed the "CIs missing owner" Performance Analytics \(PA\) indicator from the HAM advisor dashboard.
        -   Narrowed the KPI list on the Duplicate CIs KPI page when it exceeds a performance threshold, improving load time, for Data Foundations and HAM.
        -   Improved performance of SAM scheduled data-collection jobs.
-   **Version 3.0.1 - August 2026**
    -   New:
        -   Dedicated Software Asset Management \(SAM\) advisor dashboard with tree-based navigation and editable software product scope.
        -   Dashboard KPIs capture data issues across three layers: Installs \(breakdowns by CI install status, cloud license type, missing CPU, core, or thread count, missing environment or assigned-to, Duplicate CIs, and Stale CIs, plus install trends and breakdowns by publisher, product, integration source, and class\), Installed On \(CI-to-host install status mismatches\), and Infrastructure Relationships \(infrastructure relationship errors between virtual server CIs and their host servers\).
        -   Filter the SAM advisor dashboard by publisher, product, Data Model Navigator categories, and classes.
        -   Role-based access to SAM advisor for users with the SAM user role.
        -   HAM advisor entry point added to the Config Console for Hardware Asset Management \(HAM\).
        -   Summarization and remediation actions are now available on the Data Foundations advisor dashboard.
        -   HAM advisor dashboard metrics now include CI breakdown by HAM normalization status.
    -   Removed: CIs missing owner metric removed from HAM advisor dashboard.
-   **Version 2.1.3 - August 2026**

    Changed: Auto-setup is disabled for Data Foundations and Hardware Asset Management \(HAM\) in the CMDB success advisor.    Note: Auto-setup will be re-enabled in a later release with performance optimization.

-   **Version 2.1.2 - August 2026**

    Changed: Auto-setup is disabled for Data Foundations and Hardware Asset Management \(HAM\) in the CMDB success advisor.    Note: Auto-setup will be re-enabled in a later release with performance optimization.

-   **Version 2.1.0 - July 2026**
    -   New:
        -   CMDB success advisor for HAM dashboard is set up automatically on upgrade to v2.1.
        -   Model categories are recommended for CMDB success advisor for HAM scope selection.
        -   CMDB success advisor for HAM can be set up without HAM installation, but HAM Pro entitlement is required.
        -   CMDB success advisor for HAM generates a summary of CMDB data quality for HAM outcomes and lists the top 5 issues with guided remediation actions.
        -   HAM CI install status vs. asset state supports life cycle stage mismatch between CI and asset for instances where CSDM plugin \(com.snc.cmdb.csdm.activation\) is installed and migrated to life cycle stage.
    -   Changed:
        -   Charts show the top 10 values with the remainder grouped as "Others" on CMDB success advisor for Data Foundations and CMDB success advisor for HAM dashboards.
        -   Data Foundation advisor setup and edit modals no longer show exclusion-list CI classes.
    -   Fixed: Data Foundations advisor scope modal not showing principal classes marked via CI Class Manager when absent from inclusion list or on exclusion list.
-   **Version 2.0.0 - June 2026**
    -   New:
        -   Role-based access for Data Foundations advisor with cmdb\_user and cmdb\_editor roles can only view dashboards with no access to Settings and Integrations tabs. The cmdb\_admin role retains full access to advisor.
        -   Auto-setup of Data Foundations advisor dashboard with user notifications; 65 million CIs guardrail skips auto-setup.
    -   Changed: Performance at enterprise scale with pre-aggregation, read-replica routing, and dedicated Performance Analytics indicator data sources; 5-minute setup eliminated.
    -   Fixed:
        -   Accessibility related improvements including keyboard support, ARIA labels, fixed heading hierarchy, and per-route page titles.
        -   Other functional improvements including refreshed classes list in Data Foundations advisor, redesigned KPI list views, and entry-point fixes.
-   **Version 1.1.3 - April 2026**

    Fixed: For instances without HAM entitlement, completion of the Data Foundations advisor setup through the CMDB success advisor entry point is now available.

-   **Version 1.1.2 - March 2026**
    -   Expanded support for Data FoundationsAdded Data Foundations as a supported outcome, extending outcome‑based CMDB guidance beyond Hardware Asset Management \(HAM\).
    -   Scope setting based on principal class recommendationsGuided scope selection for Data Foundations using principal class recommendations derived from incident, problem, and change activity—helping teams focus on the most impactful CI classes instead of the entire CMDB.
    -   Recommended data integrationsSuggested Discovery patterns and Service Graph Connectors based on CI class and attribute coverage to support accurate and complete data ingestion.
    -   Prebuilt Data Foundations dashboardReady‑to‑use dashboards with targeted health indicators to monitor CMDB health, identify data quality gaps, and track improvement progress.
    -   Guided analysis and remediationRoot‑cause analysis across CMDB data issues and governance‑related settings, with guided remediation paths to improve data accuracy and completeness.
-   **Version 1.0.1 - November 2025**

    Unlock the full potential of your Configuration Management Database \(CMDB\) to achieve technical excellence, starting with value-maximizing Hardware Asset Management \(HAM\) outcomes. The CMDB success advisor empowers administrators with intuitive, step-by-step guidance to enhance CMDB health and data quality, without requiring deep technical expertise. By resolving issues faster and enabling continuous improvement, the tool helps align your CMDB with business goals, reduce operational risk, and maximize asset visibility and control.


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\) version history release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

