---
title: Legacy Import set data for Altiris
description: Learn the module names displayed by the Altiris import set data.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy: Altiris integration 2.0, ServiceNow provided integrations, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Legacy Import set data for Altiris

Learn the module names displayed by the Altiris import set data.

The Altiris import set data section shows a list of [Import sets](https://www.servicenow.com/docs/access?context=import-sets-landing-page&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) tables used in containing data retrieved from using JDBC to query the Altiris database. The module names \(hence the import set tables they point to\) match Altiris's table names and structure that it is loading from.

## Module names

**Note:** Functionality described here requires the Integration - Altiris 2.0 plugin.

-   Scheduled Cleanup \(Configure a schedule to cleanup/delete import set data that have already been transformed\)
-   vComputer
-   Inv\_AeX\_OS\_Operating\_System
-   Inv\_AeX\_HW\_CPU
-   Inv\_AeX\_HW\_Memory
-   Inv\_AeX\_HW\_Serial\_Number
-   Inv\_AeX\_HW\_Logical\_Disk
-   Inv\_AeX\_OS\_Add\_Remove\_Programs
-   Inv\_AeX\_AC\_TCPIP

When viewing each of these table lists, at the end of the list you have links to other operational functions of the import set.

![](../image/RelatedLinks.png "Altiris integration application")

-   [Import sets](https://www.servicenow.com/docs/access?context=import-sets-landing-page&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)
-   [Transform maps](https://www.servicenow.com/docs/access?context=c_CreatingNewTransformMaps&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)
-   **Transform History** - Log of completed import operations \(where an import set was transformed into a table\).
-   [Web service import sets](https://www.servicenow.com/docs/access?context=c_WebServiceImportSets&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)

**Parent Topic:**[Legacy: Altiris integration 2.0](../concept/c_AltirisIntegration2.0.md)

**Related topics**  


[Legacy: Web services import set tables for Altiris](r_WebServiceImportSetTables.md)

[Legacy: Altiris integration 2.0](../concept/c_AltirisIntegration2.0.md)

