---
title: ITOM Visibility and CMDB tables
description: ITOM Visibility manages and uses CMDB tables. Several ServiceNow products benefit from and add value to ITOM Visibility.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ITOM Visibility and CSDM reference, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# ITOM Visibility and CMDB tables

ITOM Visibility manages and uses CMDB tables. Several ServiceNow products benefit from and add value to ITOM Visibility.

## Tables that ITOM Visibility manages

![CSDM tables managed by ITOM Visibility.](../image/csdm-v5-tables-managed-by-itom-vis.png)

-   **Mapped application service tables**

    The tables that ITOM Visibility manages depend on the method used to map the service instance \(the label for the table was formerly application service\) . You can use the Application Service wizard to populate an application service.

    -   Map the Service instance using top-down discovery of CI connections. This method requires Service Mapping, the sm\_admin role, and the current domain must be a leaf domain. This is the best option for accuracy and complete mapping. ITOM Visibility manages the Mapped Application Service table \[cmdb\_ci\_service\_discovered\]
    -   Map the service instance using a tag list or tag family. This method requires Service Mapping and is preferred for public or private cloud where tags are typically used. ITOM Visibility manages the tag-based maps table \[cmdb\_ci\_service\_by\_tags\].
    -   Manually map the service instance. This method requires that you select specific CIs — no automation is used. ITOM Visibility manages the service maps table \[cmdb\_ci\_service\_manual\].
    -   Use Dynamic Service to synchronize manually-created CI relationships to a Service Map view.
-   **Configuration items \(CIs\) tables \[cmdb\_ci\_\*\]**

    -   Application table \[cmdb\_ci\_appl\]
    -   Server table \[cmdb\_ci\_server\]
    -   Virtual machines table \[cmdb\_ci\_vm\_instance\]
    -   Load balancer table \[cmdb\_ci\_lb\]
    -   Network gear table \[cmdb\_ci\_netgear\]
    ![ITOM Visibility table structure.](../image/itom-visibility-table-structure.png)


## Tables that ITOM Visibility uses

1.  Dynamic CI Group table \[cmdb\_ci\_query\_based\_service\]
2.  Product model tables \(for Technology Portfolio Management \[TPM\]\) software and hardware models

![CSDM tables used by ITOM Visibility.](../image/csdm-v5-tables-used-by-itom-vis.png)

## Products that benefit from ITOM Visibility

-   IT Service Management
-   Customer Service Management \(CSM\)
-   Event Management
-   Cloud Management
-   Asset Management \(Hardware Asset Management and Software Asset Management\)
-   Strategic Portfolio Management \(Financial Management — Showback statements, Application Portfolio Management \[ APM \]\)
-   Security Operations \(Incident Response, software vulnerability management\)

## Implementing CMDB data

For details on implementing CMDB data to conform with the CSDM framework, see [Implementing the CSDM framework in stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/common-service-data-model-csdm/csdm-implementation-stages.md).

**Parent Topic:**[ITOM Visibility and CSDM reference](../concept/itom-visibility-use-case-product-view.md)

