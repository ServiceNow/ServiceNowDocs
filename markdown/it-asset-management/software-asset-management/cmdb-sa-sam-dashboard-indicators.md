---
title: Indicators used in the CMDB success advisor for SAM dashboard
description: Indicators enable viewing of high-level metrics that highlight data quality, completeness, and licensing compliance issues across software installs and their related configuration items \(CIs\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/cmdb-sa-sam-dashboard-indicators.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-07-22"
reading_time_minutes: 3
keywords: [SAM advisor dashboard indicators, software install data quality metrics, duplicate software installs, server installs missing cloud license, virtual server host relationship indicators]
breadcrumb: [Use SAM advisor, Software Asset Management, IT Asset Management, Asset Management]
---

# Indicators used in the CMDB success advisor for SAM dashboard

Indicators enable viewing of high-level metrics that highlight data quality, completeness, and licensing compliance issues across software installs and their related configuration items \(CIs\).

## CMDB success advisor for SAM dashboard indicators

-   **Software installs**

    Total number of software installs from the Software Install \[cmdb\_sam\_sw\_install\] table that are in the selected scope and associated with a normalized software product, grouped by discovery source.

-   **Installs by**

    Software installs from the Software Install \[cmdb\_sam\_sw\_install\] table, grouped by a selectable dimension: software publisher \(default\), normalized software product, the CI class of the CI hosting the install, or discovery source.

-   **Software installs by normalization status**

    Software installs from the Software Install \[cmdb\_sam\_sw\_install\] table, grouped by normalized software product, the CI class of the CI hosting the install, and the normalization status recorded on the associated Software Discovery Model.

-   **Software installs missing edition**

    Total number of software installs from the Software Install \[cmdb\_sam\_sw\_install\] table where the associated Software Discovery Model doesn't have an edition value populated.

-   **Software installs missing version**

    Total number of software installs from the Software Install \[cmdb\_sam\_sw\_install\] table where the associated Software Discovery Model doesn't have a version value populated.

-   **Server installs missing cloud license**

    Total number of software installs on CIs where a cloud provider is populated and a cloud license type isn't populated, limited to a defined set of qualifying software products that require cloud license tracking.

-   **Installs by CI install status**

    Software installs from the Software Install \[cmdb\_sam\_sw\_install\] table, grouped by the install status of the CI hosting the install. On instances where the CSDM Activation plugin \(com.snc.cmdb.csdm.activation\) is active, this card is named **Installs by lifecycle stages**, and installs are grouped by life cycle stage instead.

-   **CIs missing environment**

    Total number of CIs with a software install in the selected scope that don't have an environment value populated.

-   **CIs missing assigned to**

    Total number of CIs with a software install in the selected scope that aren't assigned to a specific user.

-   **Server CIs missing CPU attributes**

    Total number of CIs with a software install in the selected scope that are missing key CPU attributes needed for accurate license calculations.

-   **CIs not updated in the last 30 days**

    Total number of CIs with a software install in the selected scope that haven't been updated in the last 30 days.

-   **CIs not updated in the last 60 days**

    Total number of CIs with a software install in the selected scope that haven't been updated in the last 60 days.

-   **CIs not updated in the last 90 days**

    Total number of CIs with a software install in the selected scope that haven't been updated in the last 90 days.

-   **Duplicate CIs**

    Total number of software installs on CIs identified as duplicates, where the CI has a follow-on de-duplication task in the Reconcile Duplicate Task \[reconcile\_duplicate\_task\] table that is still active, limited to installs of selected software products.

-   **Virtual machines without host server CI relationships**

    Total number of software installs, scoped to the selected SAM products, on Windows Server or Linux Server virtual CIs that don't have a Virtualized by::Virtualizes relationship to a host CI, limited to VMware ESX Server and Microsoft Hyper-V virtual infrastructure, resulting in gaps in licensing compliance tracking.

-   **Incorrect virtual server infrastructure relationships**

    Total number of Virtualized by or Member of relationships for virtual server CIs, limited to VMware ESX Server and Microsoft Hyper-V virtual infrastructure, that relationship health analysis flags as incorrect or suggested for removal. On the KPI Details page, this indicator appears under the heading Incorrect infrastructure relationships.

-   **Install status distribution matched**

    Virtual server software installs where the install status, or life cycle stage, of the virtual server CI matches the install status, or life cycle stage, of its related host CI.

-   **Install status distribution mismatched**

    Virtual server software installs where the install status, or life cycle stage, of the virtual server CI doesn't match the install status, or life cycle stage, of its related host CI.


**Note:** Relationship-based indicators require the **CMDB Health Dashboard - Relationship Compliance Processor** scheduled job to have run. If the job is inactive, the dashboard displays a `Relationship data incomplete` alert with a **Run job** action, and metrics in the Virtual CI relationships section may be incomplete.

