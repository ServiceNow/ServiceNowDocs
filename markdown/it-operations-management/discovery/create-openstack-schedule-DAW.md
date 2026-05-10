---
title: Create an OpenStack Discovery schedule in Discovery Admin Workspace
description: Use the Discovery Admin Workspace dashboard to create an OpenStack Discovery schedule.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Create an OpenStack Discovery schedule in Discovery Admin Workspace

Use the Discovery Admin Workspace dashboard to create an OpenStack Discovery schedule.

## Before you begin

Verify the following:

-   You have at least one validated MID Server with a status of **Up**. The MID Server must reach the IP ranges that you intend to discover. You can install the MID Server by using [Use MID Server guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/use-mid-server-guidedsetup.md) or by manually downloading and running the installer. For details, see the MID Server installation instructions for [Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_InstallAMIDServerOnLinux.md) and [Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/mid-server-install-prereqs.md).
-   The MID Server used for Cloud Discovery is configured with the Cloud Management capability.
-   You have configured an OpenStack user in the Keystone identity service with the required roles for the project so that the MID Server can access the selected cloud resources you plan to discover.
-   You have created suitable credentials in the ServiceNow AI Platform to connect with the OpenStack user that you want to use for discovery. For more information, see [OpenStack resource discovery](../../service-mapping/reference/openstack-discovery.md).
-   You're using Discovery Admin Workspace v1.13.0.

Role required: discovery\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules**.

2.  Select **New Discovery** from the header of any tab on the Schedules page.

3.  Select **Cloud-based discovery** and select **Continue**.

4.  Enter a unique and descriptive name for the Discovery schedule.

5.  Select **OpenStack** as the cloud provider.

6.  Choose a MID Server.

    |Option|Description|
    |------|-----------|
    |**Use a cluster of MID servers**|Select an existing MID Server. Clusters provide failover protection and load balancing between MID Servers. See [Configure a MID Server cluster](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_ConfigureAMIDServerCluster.md) for more information.|
    |**Automatically select a MID server**|An available MID Server is automatically selected when the Discovery schedule runs. See [Automatic MID Server selection](../../agent-client-collector/concept/acc-auto-mid-selection.md) for more information.|
    |**Search for a MID server**|Choose a MID Server to run the Discovery schedule. Only MID Servers that are validated, up, and have the Cloud Management capability are displayed.|

7.  Select **Next**.

8.  Select a cloud account.

<table id="choicetable_bbl_3zw_zgc"><thead><tr><th align="left" id="d366058e314">

Option

</th><th align="left" id="d366058e317">

Description

</th></tr></thead><tbody><tr><td id="d366058e323">

**Existing cloud account**

</td><td>

Select an existing cloud account on your instance. Once an account is selected, the **Account name**, **OpenStack Account ID**, and **Cloud URL** fields auto-populate.

</td></tr><tr><td id="d366058e341">

**New cloud account**

</td><td>

Add a new cloud account to your instance by entering an account name, ID, and Cloud URL.**Note:**

-   You can access the Cloud URL in Horizon via **Project** &gt; **API Access**
-   Example Cloud URL \(OpenStack identity service endpoint\): `https://<openstack dns>:<port>`


</td></tr></tbody>
</table>    Even if the cloud account was previously verified, you can reverify if policies or permissions may have changed by selecting **Verify information.**

9.  Select **Next**.

10. Select cloud regions for the discovery schedule.

    You can choose to include all regions linked to the cloud account or select specific regions. There’s no restriction on the number of cloud regions that you can add.

    1.  To discover specific cloud regions, select the check box for the cloud region you want to scan from the **Available cloud regions** list.

    2.  If the cloud regions don't appear, select **Refresh cloud regions**.

11. Select **Next**.

12. To complement your cloud schedule with an IP-based Discovery schedule, enable the **Create a server discovery schedule** toggle.

    1.  Select a MID Server or cluster that can discover the Virtual Machines \(VM\) and their attributes.

13. Select **Next**.

14. Configure the Discovery schedule.

    |Option|Description|
    |------|-----------|
    |**Run at a scheduled time**|The schedule runs at a scheduled date and time. Use the fields to define when the schedule runs.|
    |**Run on demand**|The schedule only runs when triggered manually. The schedule can be triggered by selecting **Finish and run** at the end of this setup, or by navigating to the schedule in the Discovery Schedules \[discovery\_schedule\] table and selecting **Discover Now**.|
    |**Run after series**|The schedule runs after another existing Discovery schedule completes, staggering or chaining them together. Selecting an existing schedule displays a relationship map of all the other associated schedules.|
    |**Set discovery time out**|If the schedule exceeds the maximum runtime, it's canceled. After toggling, configure the runtime threshold.|
    |**Finish and run**|After being selected, all the information provided is validated. Then, a Discovery schedule is created in the background, a Discovery status is created, and the schedule is run. You're redirected to the Status Details page for the schedule.|
    |**Finish**|After being selected, all the information provided is validated. A Discovery schedule is created, and you're redirected to its entry in the Discovery Schedules \[discovery\_schedule\] table. You can edit the schedule information or run it by selecting **Discover Now**.|


