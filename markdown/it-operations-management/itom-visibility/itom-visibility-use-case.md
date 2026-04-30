---
title: Applying CSDM guidelines to ITOM Visibility
description: ITOM Visibility manages and uses CMDB tables. Several ServiceNow products benefit from and add value to ITOM Visibility.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ITOM Visibility and CSDM reference, ITOM Visibility, IT Operations Management]
---

# Applying CSDM guidelines to ITOM Visibility

ITOM Visibility manages and uses CMDB tables. Several ServiceNow products benefit from and add value to ITOM Visibility.

## Tables that ITOM Visibility manages

![CSDM tables managed by ITOM Visibility.](../image/csdm-tables-managed-by-itom-visibility-4.png)

-   **Mapped application service tables**

    The tables that ITOM Visibility manages depend on the method used to map the application service. You can use the Application Service wizard to populate an application service.

    -   Map the application service using top-down discovery of CI connections. This method requires Service Mapping, the sm\_admin role, and the current domain must be a leaf domain. This is the best option for accuracy and complete mapping. ITOM Visibility manages the Mapped Application Service table \[cmdb\_ci\_service\_discovered\]
    -   Map the application service using a tag list or tag family. This method requires Service Mapping and is preferred for public or private cloud where tags are typically used. ITOM Visibility manages the tag-based maps table \[cmdb\_ci\_service\_by\_tags\].
    -   Manually map the application service. This method requires that you select specific CIs — no automation is used. ITOM Visibility manages the service maps table \[cmdb\_ci\_service\_manual\].
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

![CSDM tables used by ITOM Visibility.](../image/csdm-tables-used-by-itom-visibility-4.png)

## Products that benefit from ITOM Visibility

-   IT Service Management
-   Customer Service Management \(CSM\)
-   Event Management
-   Cloud Management
-   Asset Management \(Hardware Asset Management and Software Asset Management\)
-   Strategic Portfolio Management \(Financial Management — Showback statements, Application Portfolio Management \[ APM \]\)
-   Security Operations \(Incident Response, software vulnerability management\)

## Implementing CMDB data

For details on implementing CMDB data to conform with the CSDM framework, see [Implementing the CSDM framework in stages](https://www.servicenow.com/docs/access?context=csdm-implementation-stages&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

