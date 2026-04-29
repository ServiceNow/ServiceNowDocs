---
title: Key CMDB success advisor concepts
description: Familiarize yourself with the key terms and concepts to work with CMDB success advisor.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, CMDB success advisor, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Key CMDB success advisor concepts

Familiarize yourself with the key terms and concepts to work with CMDB success advisor.

-   **Configuration Management Database \(CMDB\)**

    The central database that stores information about IT assets \(CIs\) and their relationships.

-   **Configuration item \(CI\)**

    Any IT component tracked in the CMDB, including hardware, software, applications, or network devices.

-   **Scope**

    The set of principal classes in Data Foundations or model categories in HAM that CMDB success advisor monitors for your organization.

-   **Principal class**

    A CI class, such as Server \[cmdb\_ci\_server\], designated as important for your organization within Data Foundations. When a class is principal, a filter is automatically applied to the CI fields in incidents, changes, and problems.

-   **Model category**

    A hardware classification used as the scope unit for HAM such as Computers, Servers, Printers.

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


**Parent Topic:**[CMDB success advisor reference](cmdb-sa-reference.md)

