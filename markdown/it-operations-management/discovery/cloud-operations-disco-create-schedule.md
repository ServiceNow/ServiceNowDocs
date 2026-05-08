---
title: Create a discovery schedule in Cloud Discovery Workspace
description: Create schedules for discovering cloud resources based on the discovery method that you choose: service accounts or IP ranges. The discovery schedule defines the various settings for the cloud discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Create a discovery schedule in Cloud Discovery Workspace

Create schedules for discovering cloud resources based on the discovery method that you choose: service accounts or IP ranges. The discovery schedule defines the various settings for the cloud discovery.

## Before you begin

**Important:**

-   Starting with the Zurich release, Cloud Discovery Workspace is being prepared for future deprecation. It will be hidden and no longer activated on new instances, but will continue to be supported. Discovery Admin Workspace provides the latest experience for this functionality. For details, see the [Application/Plugin Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.
-   Starting with version 1.11.0, you can create [AWS](create-AWS-schedule-DAW.md), [Azure](create-azure-schedule-DAW.md), and [GCP](create-gcp-schedule-DAW.md) schedules in Discovery Admin Workspace.
-   Starting with version 1.13.0, you can create [Alibaba](create-alibaba-schedule-DAW.md), [IBM](create-ibm-schedule-DAW.md), [OCI](create-oci-schedule-DAW.md), [OpenStack](create-openstack-schedule-DAW.md), [oVirt](create-ovirt-schedule-DAW.md), and [VMware](create-vmware-schedule-DAW.md) schedules in Discovery Admin Workspace

-   Verify that version 1.7.1 or later of the Cloud Discovery Workspace application is installed on the ServiceNow AI Platform. For more information, see [Install Cloud Discovery Workspace](../../cloud-operations-workspace/task/install-cloud-ops-wrksp.md).
-   Before you attempt to configure Cloud Discovery, you must have at least one validated MID Server with a status of **Up**. The MID Server must reach the IP ranges that you intend to discover. You can install the MID Server by using Use MID Server guided setup or by manually downloading and running the installer. For details, see the MID Server installation instructions for Linux and Windows. Ensure to configure the MID Server used for Cloud Discovery with the Cloud Management capability.
-   Ensure that suitable credentials are available in the ServiceNow AI Platform to connect with the service accounts on which you want to perform the discovery.
-   Pattern-based discovery runs by default. In scenarios where the latest patterns application is not installed, discovery fails and you are prompted to install or migrate from CAPI-based discovery. For more information, see [Migrate from CAPI to Patterns](migrate-from-capi-to-pattern.md).

Role required: discovery\_admin

## About this task

The ServiceNow® Cloud Discovery wizard begins with the account selection and testing phase. To prevent long waits or unexpected timeouts, use the **cdu.record.watcher.timeout** system property to define the maximum waiting period for these Cloud Discovery configuration processes:

-   Service account validation
-   Member account discovery
-   Discovery of logical datacenters

The default timeout value is 300000 milliseconds or 5 minutes.

You can configure Cloud Discovery to auto-refresh the list of subaccounts and datacenters before each scheduled discovery. For more information, see [Create Discovery schedules for cloud resources](../concept/discovery-manager.md#).

## Procedure

1.  Navigate to **Workspaces** &gt; **Cloud Discovery Workspace** &gt; **Cloud Discovery**.

2.  Select **New discovery schedule**.

3.  Select the cloud provider.

    1.  Fill the values on the Choose the provider form.

        For description of the form fields, see [Create a new discovery schedule form reference](../reference/create-a-new-discovery-schedule-form.md).

    2.  Select **Next**.

4.  Select service account for the Cloud Discovery scheduleor create a service account.

    For description of the service account form fields, see [Cloud Discovery service account form reference](../reference/cloud-operations-disco-service-account-form.md). If you select an existing account, the system auto-completes the form with the available information.

    **Note:** VMware discovery can run without a service account. To discover VMware resources, configure the schedule to run on the IP address of the vCenter server.

    1.  To check the connection with the service account, select **Test account**.

    2.  If you're creating the discovery schedule for a management account, specify whether you want to discover all the member accounts or only specific member accounts.

        By default, all the existing member accounts are selected for the discovery schedule.

    3.  If you're creating the discovery schedule for a management account and the validation process doesn't return the subaccounts, select **Refresh** or rerun the account validation.

    4.  Select **Next**.

5.  Select datacenters for the discovery schedule.

    You can either select all the datacenters attached with the service account or select specific datacenters.

    1.  If you want to discover specific datacenters, select the datacenters from the **Select the data centers** drop-down list.

    2.  If the datacenters don't appear, select **Refresh Datacenters** or rerun the account validation.

    3.  Select **Next**.

6.  Specify whether you want to discover the Virtual Machines \(VM\) and their attributes.

    1.  Specify whether you want to perform VM discovery using AWS Systems Manager.

        **Note:** This option displays only when the system property **glide.discovery.enable\_ssm** is enabled and **AWS** is selected as the cloud provider in Step 3.

    2.  Select a MID Server or MID cluster that can discover the VMs.

        If you're not sure about the MID selection, select **Auto-Select MID Server**.

    3.  Select **Next**.

7.  Create a schedule to execute the Cloud Discovery.

    1.  Select an execution frequency for the Cloud Discovery schedule.

    2.  Specify a start time for executing the discovery.

    3.  Specify criteria to cancel the discovery.

    4.  Activate the discovery schedule.

8.  Do any of the following actions.

    |Option|Description|
    |------|-----------|
    |**Finish and run**|Cloud Discovery saves the schedule and executes it.|
    |**Finish**|Cloud Discovery saves the schedule and executes it as per the defined frequency.|


