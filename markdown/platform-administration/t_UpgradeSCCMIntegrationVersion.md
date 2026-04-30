---
title: Upgrade the SCCM integration version
description: If you're using an earlier version of an System Center Configuration Manager\(SCCM\) plugin, you can switch over to a later version to take advantage of new features.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Microsoft SCCM integration, ServiceNow provided integrations, Integration options, Integration with third-party applications and data sources, Integrations, Configure core features, Administer]
---

# Upgrade the SCCM integration version

If you're using an earlier version of an System Center Configuration Manager\(SCCM\) plugin, you can switch over to a later version to take advantage of new features.

## Before you begin

Role required: admin

## About this task

The ServiceNow SCCM integrations are self-contained and can exist independently. They each use their own import set tables, data sources and transform maps. However, all SCCM integrations will transform data into the same tables within the ServiceNow CMDB. To avoid the data being overwritten by another source:

-   Use one SCCM integration and disable all other SCCM scheduled imports.
-   Perform a [full import](../../../integrate/cmdb/reference/how-sccm-integration-works.md) to clear the cmdb\_software\_instance table, the cmdb\_sam\_sw\_install table, and other tables of old SCCM data.

**Note:** It is possible to configure each plugin to integrate with SCCM 2007 or 2012 because the mechanism of the integration is actually the same, which is to leverage Java Database Connectivity \(JDBC\) imports. However, a data source must be modified if it is used for an SCCM version for which it was not written. Use the plugin version that corresponds to the SCCM version for which the data source is intended.

To change the SCCM integration:

-   Disable the current integration by deactivating the SCCM import schedule.
-   Activate the new SCCM plugin.
-   Reimport all the software records when you're switching to an integration that supports incremental imports of removed software.

To disable the SCCM import schedule:

## Procedure

1.  Navigate to **All** &gt; **Integration - Microsoft SCCM 20xx** &gt; **Scheduled Import**.

2.  Clear the **Active** check box.

3.  Select **Save** or **Update**.

4.  To activate the new SCCM plugin, navigate to **All** &gt; **Admin Center** &gt; **Application Manager**.

5.  Search for **\*SCCM** to see all the available SCCM integrations plugins.

6.  Activate the plugin.


**Parent Topic:**[Microsoft SCCM integration](../../../integrate/cmdb/concept/c_MicrosoftSCCMIntegration.md)

**Related topics**  


[SCCM data import process and source tables](../../../integrate/cmdb/reference/how-sccm-integration-works.md)

