---
title: CMDB success advisor release notes
description: Version history for the ServiceNow CMDB success advisor application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-cmdb-rn-success-advisor.html
release: store
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 2
breadcrumb: [ServiceNow Store - Configuration Management Database \(CMDB\), ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# CMDB success advisor release notes

Version history for the ServiceNow® CMDB success advisor application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

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


**Parent Topic:**[ServiceNow Store - Configuration Management Database \(CMDB\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-cmdb-landing.md)

