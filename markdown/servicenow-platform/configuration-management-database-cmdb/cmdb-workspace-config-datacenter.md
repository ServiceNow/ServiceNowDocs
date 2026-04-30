---
title: Configure datacenters for Cloud vs Non-cloud resources
description: The Cloud vs Non-cloud resources chart in CMDB Workspace determines which CIs and application services are stored on a cloud and which aren't in the organization. In addition to base system classifications, you can add cloud versus non-cloud classifications that reflect specific datacenter deployments in the organization.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, CMDB Workspace, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure datacenters for Cloud vs Non-cloud resources

The Cloud vs Non-cloud resources chart in CMDB Workspace determines which CIsand application services are stored on a cloud and which aren't in the organization. In addition to base system classifications, you can add cloud versus non-cloud classifications that reflect specific datacenter deployments in the organization.

## Before you begin

Role required: sn\_cmdb\_admin

## About this task

The Datacenter Types \[sn\_cmdb\_ws\_datacenter\_type\] table stores datacenter classes with a classification of being used as a cloud storage or not in the organization. The calculations for the Cloud vs Non-cloud resources chart in the CI overview tile in [CMDB Workspace](../concept/cmdb-workspace.md), reflects on the datacenters in that table and their classifications.

CIs are counted as non-cloud mainly if either of the following conditions is met:

-   The CI is not associated with any datacenter.
-   The CI is associated with a datacenter that is classified as non-cloud in the Datacenter Types table.

In the base system, the Datacenter Types table contains several common datacenters. For example, the Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] class is classified as 'Cloud'. Therefore, the Cloud vs Non-cloud resources chart includes in its calculations and bars the Azure Datacenter \[cmdb\_ci\_azure\_datacenter\] class.

## Procedure

1.  Select **All**.

2.  In the Filter navigator, enter `sn_cmdb_ws_datacenter_type.list` to access the Datacenter Types table.

3.  Click **New** and fill out the Datacenter Type form for a datacenter that is used in the organization.

    |Field|Description|
    |-----|-----------|
    |Datacenter class|A child class of the Logical Datacenter \[cmdb\_ci\_logical\_datacenter\] class which is used in the organization.|
    |Type|Classification that reflects whether the specified **Datacenter class** is being used as cloud storage or not.|
    |Cloud Provider|Custom label for the cloud provider.|

4.  Click **Submit**.


**Parent Topic:**[Configuring CMDB Workspace](../concept/configuring-cmdb-workspace.md)

