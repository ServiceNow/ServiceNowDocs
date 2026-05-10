---
title: Create a Discovery schedule for Alibaba Cloud
description: Create a Discovery schedule to run Alibaba Cloud discovery.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 2
breadcrumb: [Discovery for Alibaba Cloud, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Create a Discovery schedule for Alibaba Cloud

Create a Discovery schedule to run Alibaba Cloud discovery.

## Before you begin

Role required: discovery\_admin

## Procedure

1.  Navigate to **Discovery** &gt; **Discovery Schedules**.

    **Note:** Starting with v1.13.0, you can also create an Alibaba Cloud in Discovery Admin Workspace. For more information, see [Create an Alibaba Cloud Discovery schedule in Discovery Admin Workspace](create-alibaba-schedule-DAW.md).

2.  Select the **Cloud Discovery** button.

3.  In the **Provider** field, select **Alibaba**.

4.  Provide a name in the **Schedule Name** field.

5.  Choose the method of selecting the MID Server from the **MID Selection Type** drop-down list.

    -   **Auto-Select MID Server**: Automatically chooses the most appropriate MID Server.
    -   **Specific MID Server**: A specific MID Server that you choose from the **MID Server** drop-down list.
    -   **Specific MID Cluster**: A MID Server cluster that you choose from the **MID Cluster** drop-down list.
6.  Either create a new account or select an existing one.

<table id="choicetable_wm3_pvr_ghc"><thead><tr><th align="left" id="d395448e170">

Existing or new account

</th><th align="left" id="d395448e173">

Actions

</th></tr></thead><tbody><tr><td id="d395448e179">

**Add account**

</td><td>

1.  Select **Add Account**.
2.  Provide a name in the **Name** field.
3.  Enter the ID in the **Account ID** field.
4.  In the **Credentials** field, select existing credentials or create new credentials.
    -   To use existing credentials, select the credential from the drop-down list.
    -   To create new credentials, select the plus button and fill in the fields.

For more information, see [Create Alibaba Cloud API Credentials](create-alibaba-cloud-api-credentials.md).

5.  Enter the URL of a datacenter in the **Datacenter URL** field.


</td></tr><tr><td id="d395448e250">

**Select Account**

</td><td>

1.  Select **Select Account**.
2.  Select the account from the drop-down list.

The form fields are populated with the information from the selected account.

</td></tr></tbody>
</table>7.  Validate the account by selecting **Test Account**.

8.  Select **Next**.

9.  On the Select Datacenters page, determine whether to select specific datacenters to be discovered or to discover all datacenters.

    -   Manually select the datacenters to be discovered by moving them into the **Selected** column.
    -   Discover all available datacenters by turning on the **Discover all datacenters listed below** option.
10. Select **Next**.

11. On the **Discover Virtual Machines** page, set up the running of VM OS Discovery.

    1.  Retain the **Discover VMs by IP address** option.

    2.  Choose the method of selecting the MID Server from the **MID Selection Type** drop-down list.

12. Select **Next**.

13. On the Create Schedule page, determine when and how often to run your discovery.

    1.  Activate the Discovery schedule by turning the **Active** option on.

    2.  Choose the discovery frequency from the **Frequency** drop-down list.

    3.  Set the **Start time** for the discovery schedule.

    4.  Automatically cancel discovery if it exceeds a specified time limit by selecting the **Cancel discovery if longer than:** check box and setting the time limit.

14. Determine whether to create the schedule or to create the schedule and run discovery.

    -   To create the schedule but not run discovery, select **Finish** from the Finish and Run drop-down list.
    -   To create the schedule and run discovery, select **Finish and Run.**

**Parent Topic:**[Discovery for Alibaba Cloud](../concept/alibaba-cloud-discovery.md)

