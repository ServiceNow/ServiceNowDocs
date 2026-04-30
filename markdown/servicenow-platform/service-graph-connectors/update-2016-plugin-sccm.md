---
title: Upgrade from the legacy SCCM plugin to the Service Graph Connector for Microsoft SCCM
description: Deactivate the scheduled imports and pull records so that you can upgrade from the Microsoft SCCM 2016 plugin or an earlier version of the plugin to the Service Graph Connector for Microsoft SCCM.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Microsoft SCCM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Upgrade from the legacy SCCM plugin to the Service Graph Connector for Microsoft SCCM

Deactivate the scheduled imports and pull records so that you can upgrade from the Microsoft SCCM 2016 plugin or an earlier version of the plugin to the Service Graph Connector for Microsoft SCCM.

## Before you begin

Role required: none

If you are upgrading to the Service Graph Connector for Microsoft SCCM, the following steps are mandatory. The steps must be executed in any instance with an existing install of the Microsoft SCCM 2016 plugin or with an earlier version of the plugin.

**Note:** The Service Graph Connector for Microsoft SCCM is an independent implementation that does not reuse any components from the Microsoft SCCM 2016 plugin.

## About this task

The Service Graph Connector for Microsoft SCCM is a successor to the Microsoft SCCM 2016 plugin. If you already have the Microsoft SCCM 2016 plugin or an earlier version installed in your instance, you must follow these steps to enable the successful transition from using the SCCM plugin to using the Service Graph Connector. Additionally, you can run a SG-SCCM cleanup to delete the Network Adapters and Disks created from the older SCCM plugin to make the migration faster.

When the Service Graph Connector for Microsoft SCCM is installed in an instance, you must no longer run any components from the Microsoft SCCM 2016 plugin, including Data Sources and Scheduled Data Imports. The SCCM 2016 plugin Scheduled Data Imports must be tuned off. The Service Graph Connector for Microsoft SCCM installs a new set of SG-SCCM Data Sources and Scheduled Data Imports.

**Warning:** This upgrade process should be performed and validated in a non-production or test instance that is based on a recent clone of the customer production instance. Failure to first validate upgrade in a non-production instance may result in unexpected outcomes and possible data loss or corruption.

Any customizations to the SCCM 2016 plugin will not automatically migrate. The customizations would have to be reimplemented in the Service Graph Connector for Microsoft SCCM, such as by using IntegrationHub-ETL.

## Procedure

1.  If you are migrating from the SCCM 2016 plugin, then run the Migration Readiness Tool for Service Graph Connector for SCCM.

    The plugin can be downloaded from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/8d1c188588b764502170ac298d9399de/1.1.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DSCCM%2520Migration&sl=sh).

    The tool does not migrate any changes, but runs a series of ATF tests to identify any customizations that were done to the legacy SCCM 2016 plugin compared to the OOB SCCM 2016 plugin. It will not migrate the changes between the two plugins, but serves to alert any customizations.

2.  After the tool has finished running, review the tests that were failed.

    A failed test means that a customization was made in the plugin. The customization could be a transform map. For example, if a transform map was modified, then it needs to be reimplemented in the connector.

3.  Deactivate the scheduled imports from the older SCCM plugin.

    For more information on how to deactivate scheduled imports, see [Upgrade the SCCM integration version](https://www.servicenow.com/docs/access?context=t_UpgradeSCCMIntegrationVersion&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

4.  Delete duplicate OS software records in the older SCCM plugin.

    **Note:** There is no cleanup required for Computer OS Software records if SAM is enabled.

    1.  Navigate to the Software Package or Software Instance table in the older SCCM plugin.

    2.  Search for the duplicate OS records that you want to delete.

        You can tell which records are the SG-SCCM software OS records if the version number is included in the Name or Product Name.

    3.  To delete the duplicate software OS records from the Software Package table, do the following:

        1.  On the Software Package table, select the duplicate OS record that does not have **SG-SCCM** in the **Discovery Source** column.
        2.  Delete the duplicate OS record and repeat with other records as needed.
    4.  To delete the duplicate software OS records from the Software Instance table, do the following:

        1.  On the Software Instance table, select the duplicate OS record that has the **SCCM group ID** column empty.
        2.  Delete the duplicate OS record and repeat with other records as needed.
    **Note:** This step is optional because there is a difference in the way software OS records are written to the CMDB, between the legacy SCCM plugin and Service Graph Connector. The SCCM plugin did not record values to sys\_object\_source, a discovery\_source, or a sccm\_group\_id.

5.  After you are finished deactivating the scheduled imports and deleting the duplicate OS records from the older SCCM plugin, configure the connector.

    For instructions, see [Configure the Service Graph Connector for Microsoft SCCM](configure-sccm-integration.md).

6.  Clean up the Disk and Network Adapter records created by the SCCM plugin.

    1.  Confirm that you are in the Service Graph Connector for Microsoft SCCM application scope.

    2.  Navigate to **Scheduled Job** &gt; **SG-SCCM CleanupUtil**.

    3.  Select the **SG-SCCM CleanupUtil** scheduled job, and then switch to the global application scope.

    4.  To make a copy of the scheduled job, right-click the header of the scheduled job and select **Insert and Stay**.

    5.  Change the name to **SG-SCCM CleanupUtil Global**.

    6.  Click **Update**.

    7.  When you need to run the scheduled job, click **Execute Now**.

    8.  To check the progress of the run, do the following:

        1.  Navigate to **System Log** &gt; **All**.
        2.  To filter the records for the script run, enter `SG-SCCM CleanupUtil` under the **Message** search box.

            The script will have a log message for each batch so that you know the status of the current run and its progress.

            **Note:** The duration of the run depends on the amount of Network Adapter and Disk data in the CMDB from the previous SCCM integration. The data must meet the condition for the cleanup.


## What to do next

When you execute the Service Graph Connector components, your existing CMDB data created by the SCCM plugin becomes managed and maintained by Service Graph Connector for Microsoft SCCM.

