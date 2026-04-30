---
title: Create an Azure Discovery schedule in Discovery Admin Workspace
description: Use the Discovery Admin Workspace dashboard to create an Azure Discovery schedule.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery for Microsoft Azure Cloud, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Create an Azure Discovery schedule in Discovery Admin Workspace

Use the Discovery Admin Workspace dashboard to create an Azure Discovery schedule.

## Before you begin

Verify the following:

-   You have at least one validated MID Server with a status of **Up**. The MID Server must reach the IP ranges that you intend to discover. You can install the MID Server by using [Use MID Server guided setup](https://www.servicenow.com/docs/access?context=use-mid-server-guidedsetup&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) or by manually downloading and running the installer. For details, see the MID Server installation instructions for [Linux](https://www.servicenow.com/docs/access?context=t_InstallAMIDServerOnLinux&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and [Windows](https://www.servicenow.com/docs/access?context=mid-server-install-prereqs&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).
-   The MID Server used for Cloud Discovery is configured with the Cloud Management capability.
-   You have configured a service principal in the Azure Active Directory that has the necessary permissions so that the MID Server can access the cloud resources you plan to discover. For more information, see [Discovery for Microsoft Azure Cloud](../concept/azure-cloud-discovery.md).
-   You have created suitable credentials in the ServiceNow AI Platform to connect with the service accounts on which you want to perform the discovery. For more information, see [Create Azure cloud credentials](create-azure-cloud-credentials.md).
-   You're using Discovery Admin Workspace v1.11.0 or later.

Role required: discovery\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules**.

2.  Select **New Discovery** from the header of any tab on the Schedules page.

3.  Select **Cloud-based discovery** and select **Continue**.

4.  Enter a unique and descriptive name for the Discovery schedule.

5.  Select **Azure** as the cloud provider.

6.  Choose a MID Server.

    |Option|Description|
    |------|-----------|
    |**Use a cluster of MID servers**|Select an existing MID Server. Clusters provide failover protection and load balancing between MID Servers. See [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) for more information.|
    |**Automatically select a MID server**|An available MID Server is automatically selected when the Discovery schedule runs. See [Automatic MID Server selection](../../agent-client-collector/concept/acc-auto-mid-selection.md) for more information.|
    |**Search for a MID server**|Choose a MID Server to run the Discovery schedule. Only MID Servers that are validated, up, and have the Cloud Management capability are displayed.|

7.  Select **Next**.

8.  Select a cloud account.

<table id="choicetable_bbl_3zw_zgc"><thead><tr><th align="left" id="d492492e317">

Option

</th><th align="left" id="d492492e320">

Description

</th></tr></thead><tbody><tr><td id="d492492e326">

**Existing cloud account**

</td><td>

Select an existing cloud account on your instance. Once an account is selected, the **Account name** and **Subscription ID/Management Group ID** fields auto-populate.

</td></tr><tr><td id="d492492e341">

**New cloud account**

</td><td>

Add a new cloud account to your instance by entering a name and subscription ID or management group ID.**Note:** You can access the Subscription or Group ID in the Azure portal, under the **Subscriptions** or **Management Groups** section, respectively.

</td></tr></tbody>
</table>    Even if the service account was previously verified, you can reverify if policies or permissions may have changed by selecting **Verify information.**

9.  Select **Discover all Subscriptions** or **Discover specific Subscriptions**.

    **Note:** This option displays only when the target cloud account is an Azure management account.

    1.  If discovering specific subscriptions, select **Add subscriptions**.

        The Discoverable Subscriptions dialog displays.

    2.  Select the check box next to one or more corresponding names and then select **Add**.

10. Select **Next**.

11. Select cloud regions for the discovery schedule.

    You can choose to include all regions linked to the cloud account or select specific regions. There’s no restriction on the number of cloud regions that you can add.

    1.  To discover specific cloud regions, select the check box for the cloud region you want to scan from the **Available cloud regions** list.

    2.  If the cloud regions don't appear, select **Refresh cloud regions**.

12. Select **Next**.

13. To complement your cloud schedule with an IP-based Discovery schedule, enable the **Create a server discovery schedule** toggle.

    1.  Select a MID Server or cluster that can discover the Virtual Machines \(VM\) and their attributes.

14. Select **Next**.

15. Configure the Discovery schedule.

    |Option|Description|
    |------|-----------|
    |**Run at a scheduled time**|The schedule runs at a scheduled date and time. Use the fields to define when the schedule runs.|
    |**Run on demand**|The schedule only runs when triggered manually. The schedule can be triggered by selecting **Finish and run** at the end of this setup, or by navigating to the schedule in the Discovery Schedules \[discovery\_schedule\] table and selecting **Discover Now**.|
    |**Run after series**|The schedule runs after another existing Discovery schedule completes, staggering or chaining them together. Selecting an existing schedule displays a relationship map of all the other associated schedules.|
    |**Set discovery time out**|If the schedule exceeds the maximum runtime, it's canceled. After toggling, configure the runtime threshold.|
    |**Enable event-driven discovery**|If Azure sends resource change events, the Configuration Management Database \(CMDB\) is updated without running the full discovery schedule. Only the affected resources are processed. For more information, see [Azure change processing](../../it-operations-management/concept/azure-change-processing.md).|
    |**Finish and run**|After being selected, all the information provided is validated. Then, a Discovery schedule is created in the background, a Discovery status is created, and the schedule is run. You're redirected to the Status Details page for the schedule.|
    |**Finish**|After being selected, all the information provided is validated. A Discovery schedule is created, and you're redirected to its entry in the Discovery Schedules \[discovery\_schedule\] table. You can edit the schedule information or run it by selecting **Discover Now**.|


