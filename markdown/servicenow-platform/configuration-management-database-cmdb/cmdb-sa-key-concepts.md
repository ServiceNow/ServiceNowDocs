---
title: Key CMDB success advisor concepts
description: Familiarize yourself with the key terms and concepts to work with CMDB success advisor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-key-concepts.html
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-07-22"
reading_time_minutes: 1
keywords: [CMDB success advisor key concepts, CMDB success advisor glossary, principal class definition, model category definition, scope definition CMDB success advisor, remediation actions definition]
breadcrumb: [Reference, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Key CMDB success advisor concepts

Familiarize yourself with the key terms and concepts to work with CMDB success advisor.

-   **Configuration Management Database \(CMDB\)**

    The central database that stores information about IT assets \(CIs\) and their relationships.

-   **Configuration item \(CI\)**

    Any IT component tracked in the CMDB, including hardware, software, applications, or network devices.

-   **Scope**

    The set of principal classes in Data Foundations, model categories in HAM, or software products in Software Asset Management \(SAM\) that CMDB success advisor monitors for your organization.

-   **Principal class**

    A CI class, such as Server \[cmdb\_ci\_server\], designated as important for your organization within Data Foundations. When a class is principal, a filter is automatically applied to the CI fields in incidents, changes, and problems.

-   **Model category**

    A hardware classification used as the scope unit for HAM such as Computers, Servers, Printers.

-   **Software product**

    A licensable software classification, grouped by publisher, used as the scope unit for Software Asset Management \(SAM\).

-   **Service Graph Connectors**

    A pre-built integration that imports data from an external system into the CMDB.

-   **Discovery pattern**

    An automated ServiceNow Discovery rule that scans the network to find and populate CI attributes.

-   **Key Performance Indicator \(KPI\)**

    A measurable metric showing CMDB health in a specific area including completeness, correctness, and compliance.

-   **Remediation actions**

    Context-aware suggestions shown on the KPI details page for addressing a specific data quality issue. Actions appear only when actionable insights are available for the selected chart segment.

-   **Data quality issue**

    A detected problem in CMDB data, such as a CI missing a serial number, a stale record, or a duplicate.

-   **CMDB Data Manager**

    A ServiceNow feature that defines which integration source has authority \(ownership\) over each CI attribute.


**Parent Topic:**[CMDB success advisor reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/configuration-management-database-cmdb/cmdb-sa-reference.md)

