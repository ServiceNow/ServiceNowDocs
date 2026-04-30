---
title: Create an AWS Discovery schedule in Discovery Admin Workspace
description: Use the Discovery Admin Workspace dashboard to create an Amazon Web Services \(AWS\) Discovery schedule.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Discovery, Admin, Workspace]
breadcrumb: [Discovery for AWS, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Create an AWS Discovery schedule in Discovery Admin Workspace

Use the Discovery Admin Workspace dashboard to create an Amazon Web Services \(AWS\) Discovery schedule.

## Before you begin

Verify the following:

-   You have at least one validated MID Server with a status of **Up**. The MID Server must reach the IP ranges that you intend to discover. You can install the MID Server by using [Use MID Server guided setup](https://www.servicenow.com/docs/access?context=use-mid-server-guidedsetup&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) or by manually downloading and running the installer. For details, see the MID Server installation instructions for [Linux](https://www.servicenow.com/docs/access?context=t_InstallAMIDServerOnLinux&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) and [Windows](https://www.servicenow.com/docs/access?context=mid-server-install-prereqs&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).
-   The MID Server used for Cloud Discovery is configured with the Cloud Management capability.
-   You have created suitable credentials in the ServiceNow AI Platform to connect with the service accounts on which you want to perform the discovery.
-   Cloud Discovery has adequate permission to discover the resources of the target cloud. For more information on AWS cloud permissions, see [Control AWS access and permissions using policies](../../it-operations-management/task/aws-create-user-policy-cloud-mgt.md).
-   You're using Discovery Admin Workspace v1.11.0 or later.

Role required: discovery\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Discovery Admin Workspace** &gt; **Schedules**.

2.  Select **New Discovery** from the header of any tab on the Schedules page.

3.  Select **Cloud-based discovery** and select **Continue**.

4.  Enter a unique and descriptive name for the Discovery schedule.

5.  Select **AWS** as the cloud provider.

6.  Choose a MID Server.

<table id="choicetable_bcg_4pg_z2c"><thead><tr><th align="left" id="d378337e224">

Option

</th><th align="left" id="d378337e227">

Description

</th></tr></thead><tbody><tr><td id="d378337e233">

**Use a cluster of MID servers**

</td><td>

Select an existing MID Server. Clusters provide failover protection and load balancing between MID Servers. See [Configure a MID Server cluster](https://www.servicenow.com/docs/access?context=t_ConfigureAMIDServerCluster&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

</td></tr><tr><td id="d378337e252">

**Automatically select a MID server**

</td><td>

An available MID Server with an Identity and Access Management \(IAM\) role is automatically selected when the Discovery schedule runs. See [Automatic MID Server selection](../../agent-client-collector/concept/acc-auto-mid-selection.md) for more information.

</td></tr><tr><td id="d378337e280">

**Search for a MID server**

</td><td>

Choose a MID Server to run the Discovery schedule. Only MID Servers that are validated, up, and have the Cloud Management capability are displayed.**Note:** If you select this option, you can restrict the search to MID Servers with credential-less Discovery enabled by checking the corresponding box.

</td></tr></tbody>
</table>7.  Select **Next**.

8.  Select a cloud account.

    |Option|Description|
    |------|-----------|
    |**Existing cloud account**|Select an existing cloud account on your instance. Once an account is selected, the **Account name** and **Account ID** fields auto-populate.|
    |**New cloud account**|Add a new cloud account to your instance by entering an account name and ID.|

9.  Choose whether you want to **Assume an IAM role** or **Use permanent credentials**.

<table id="choicetable_lvl_1hq_jhc"><thead><tr><th align="left" id="d378337e372">

Option

</th><th align="left" id="d378337e375">

Description

</th></tr></thead><tbody><tr><td id="d378337e381">

**Assume an IAM role**

</td><td>

The MID Server temporarily assumes an IAM role using a trust relationship. After selecting, provide the Access Role Name and account for access.**Note:** Before entering the Access Role Name and account, verify the following:

-   The IAM role exists on the target account, with the required permissions and policies for Cloud Discovery.
-   The IAM role must trust the MID Server's account so it can assume the role.
If these prerequisites aren't met, verification fails. It's best to confirm with your cloud admin that the role and trust relationship are properly configured before proceeding.

</td></tr><tr><td id="d378337e407">

**Use permanent credentials**

</td><td>

The MID Server uses static access keys tied to an IAM user.

</td></tr></tbody>
</table>    Even if the service account was previously verified, you can reverify if policies or permissions may have changed by selecting **Verify information.**

10. Select **Discover all member accounts** or **Discover specific member accounts**.

    **Note:** This option displays only when the target cloud account is an AWS management account.

    1.  If discovering specific subscriptions, select **Add member accounts**.

        The Discoverable Accounts dialog displays.

    2.  Select the check box next to one or more corresponding names and then select **Add**.

11. Select **Next**.

12. Select cloud regions for the discovery schedule.

    You can choose to include all regions linked to the cloud account or select specific regions. There’s no restriction on the number of cloud regions that you can add.

    1.  To discover specific cloud regions, select the check box for the cloud region you want to scan from the **Available cloud regions** list.

    2.  If the cloud regions don't appear, select **Refresh cloud regions**.

13. Select **Next**.

14. To complement your cloud schedule with an IP-based Discovery schedule, enable the **Create a server discovery schedule** toggle and choose a MID Server.

15. Select **Next**.

16. Configure the Discovery schedule.

    |Option|Description|
    |------|-----------|
    |**Run at a scheduled time**|The schedule runs at a scheduled date and time. Use the fields to define when the schedule runs.|
    |**Run on demand**|The schedule only runs when triggered manually. Trigger the schedule by selecting **Finish and run** at the end of this setup, or by navigating to the schedule in the Discovery Schedules \[discovery\_schedule\] table and selecting **Discover Now**.|
    |**Run after series**|The schedule runs after another existing Discovery schedule completes, staggering or chaining them together. Selecting an existing schedule displays a relationship map of all the other associated schedules.|
    |**Set discovery time out**|If the schedule exceeds the maximum runtime, it's canceled. After toggling, configure the runtime threshold.|
    |**Finish and run**|After being selected, all the information provided is validated. Then, a Discovery schedule is created in the background, a Discovery status is created, and the schedule is run. You're redirected to the Status Details page for the schedule.|
    |**Finish**|After being selected, all the information provided is validated. A Discovery schedule is created, and you're redirected to its entry in the Discovery Schedules \[discovery\_schedule\] table. You can edit the schedule information or run it by selecting **Discover Now**.|


