---
title: Review your current infrastructure with Cloud Migration Assessment
description: Use the holistic view of all discovered resources to assess your infrastructure. You can also drill in and see detailed information on all discovered resources. Understanding which resources your organization uses is an important step in planning the migration process.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Planning the migration process, Using Cloud Migration Assessment in Configurable Workspace, Cloud Migration Assessment, ITOM Cloud Accelerate, IT Operations Management]
---

# Review your current infrastructure with Cloud Migration Assessment

Use the holistic view of all discovered resources to assess your infrastructure. You can also drill in and see detailed information on all discovered resources. Understanding which resources your organization uses is an important step in planning the migration process.

## Before you begin

Ensure that Discovery successfully ran horizontal discovery on the relevant segment of your IT infrastructure.

If there are third-party discovery applications, make sure that they entered the discovered information into the Configuration Management Database \(CMDB\).

Role required: sn\_cloud\_migration.operator

## About this task

Cloud Migration Assessment builds on the information that Discovery finds and stores in the CMDB. It also uses probes to discover information necessary for the cloud migration process. Cloud Migration Assessment can display the information that third-party discovery applications find. It means that if your organization deploys such applications, you can get an all-inclusive view of your infrastructure.

You can view at a glance the number of deployed servers, applications, and virtual machines \(VMs\). The Overview tab presents servers by class.

## Procedure

1.  Navigate to **All** &gt; **** &gt; **Cloud Migration** &gt; **Cloud Migration Workspace**.

2.  Review the summary of the discovered resources on the **Overview** tab.

    ![Review information about servers.](../image/cm-workflows-servers-breakdown.png "Overview tab showing information about servers")

    By default the **Overview** tab shows only the categories that have discovered information for these categories. The category is hidden unless there is related information to display for it. For example, if there is no discovered information on Amazon AWS Cloud resources, the AWS category does not appear under the **Categories** filter.

3.  Use filters to display the relevant information on the **Overview** tab:

    |Filter|Description|
    |------|-----------|
    |Categories|
    |All resources|Resources of all categories.|
    |All on-premise resources|Resources located on premise, not on cloud.|
    |Physical server|Physical servers.|
    |Virtual server|Virtualization solution: VMware Virtualization, IBM HMC Virtualization, HyperV Virtualization, Hutanix Virtualization, Solaris Virtualization, Openstack Virtualization.|
    |Cloud resources|Resources located in the cloud.|
    |AWS|Resources located on AWS|
    |Azure|Resources located on Microsoft Azure Cloud.|
    |GCP|Resources located on Google Cloud Platform \(GCP\).|
    |IBM|Resources located on IBM Cloud Platform.|
    |VMware Cloud|Resources located in your on-premise environment.|
    |All resources|Resources assigned and unassigned to assessment tasks.|
    |Unassigned resources|Resources unassigned to assessment tasks.|
    |All discovered times|Resources discovered at all times.|
    |Discovered 15 days ago|Resources discovered 15 days ago.|
    |Discovered 30 days ago|Resources discovered 30 days ago.|
    |All discovery sources|Resources discovered by Discovery and any other third-party discovery tool integrated with the ServiceNow AI Platform®.|
    |ServiceNow &amp; ServiceWatch|Resources discovered by Discovery.|

    The **Overview** tab displays only the information that matches the categories you selected. All lists that you can access by selecting other tabs and tiles on this page are also filtered by the same categories. For example, if you selected **Physical servers** from **Categories**, the list on the **Servers and VMs** tab shows only physical servers.

4.  In the **Server breakdown** pie chart report and the **Resources by category** bar report, hide irrelevant server CI classes by selecting their names in the chart legend.


-   **[Review detailed server information in Configurable Workspace](migration-review-server-info.md)**  
Review the information on the discovered resources to understand how they are deployed in your current infrastructure. Analyzing and assessing your current infrastructure is the first step in the cloud migration process.
-   **[Review detailed information on virtual machines in Configurable Workspace](migration-review-vm-info.md)**  
Review the information on the discovered virtual machines \(VMs\) to understand how they are deployed in your current infrastructure. Analyzing and assessing your current infrastructure is the first step in the cloud migration process.
-   **[Review detailed application information in Configurable Workspace](migration-review-application-info.md)**  
Review the information on the discovered applications to understand how they are deployed in your current infrastructure. Analyzing and assessing your current infrastructure is the first step in the cloud migration process.

**Parent Topic:**[Planning the migration process](../concept/cloud-migration-planning.md)

**Previous topic:**[Analyzing your current infrastructure](../concept/cloud-migration-analyzing-resources.md)

**Next topic:**[Review detailed server information in Configurable Workspace](migration-review-server-info.md)

