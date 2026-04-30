---
title: Upgrade to the latest version of Service Graph Connector for Microsoft SCCM
description: Upgrade your Service Graph Connector for Microsoft SCCM. When you upgrade versions, you can select the files that you want to transfer from the earlier version to the later version of the Service Graph Connector for Microsoft SCCM.
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft SCCM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Upgrade to the latest version of Service Graph Connector for Microsoft SCCM

Upgrade your Service Graph Connector for Microsoft SCCM. When you upgrade versions, you can select the files that you want to transfer from the earlier version to the later version of the Service Graph Connector for Microsoft SCCM.

## Before you begin

To avoid any serious upgrade issues, perform the upgrade in a test or development instance prior to upgrading in a production environment.

Role required: admin

## About this task

When you upgrade from an earlier version to the latest version of the Service Graph Connector for Microsoft SCCM, there are Skipped Updates. The original SCCM data source files that were installed have the last run date updated as part of the data source runs. The files will be treated as custom files by the platform. When the newer version is installed, the newer data sources will not be automatically upgraded.

After you have upgraded to the newer version, you can check the upgrade status.

## Procedure

1.  Review all the updates from the upgrade center and select the data source files from the newer version.

    You can access the upgrade history and review the updates from the Skipped Changes to Review related list. See [Review skipped records using related lists](https://www.servicenow.com/docs/access?context=uc-access-rl&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

2.  If you have customized the earlier version, select the changes that you need from the older file and migrate them to the new file.

    **Note:** Repeat this migration process for all the other skipped update files.


## What to do next

After the upgrade, if there are changes to the SQL in the data source files or mapping, then do the following:

1.  Clear the **Use last run datetime** check box in all the data sources.
2.  Perform a full pull of data from all the data sources.

**Note:** Upgrading from Service Graph Connector for Microsoft SCCM v2.3 to v2.3.1 requires a minimum pull of Computer and Software, because the Source Native Key for the software within the SQL was changed in the SG-SCCM Removed Software data source. Without the correct Source Native Keys, it will not be able find the software in the CMDB.

For more information on resolving any conflicts, see the following topics:

-   [Revert a customization](https://www.servicenow.com/docs/access?context=uc-revert-customization&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)
-   [Resolve a skipped update and set a resolution status](https://www.servicenow.com/docs/access?context=uc-resolve-skipped-update&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)
-   [Skipped Changes to Review related list](https://www.servicenow.com/docs/access?context=uc-access-rl&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)

