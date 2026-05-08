---
title: Deploy a replication configuration through an update set in Instance Data Replication
description: Export a replication configuration from one instance and import it on another instance through an update set in Instance Data Replication \(IDR\).
locale: en-US
release: australia
product: Instance Data Replication \(IDR\)
classification: instance-data-replication-idr
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Deploying replication configuration, Administer, Instance Data Replication, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Deploy a replication configuration through an update set in Instance Data Replication

Export a replication configuration from one instance and import it on another instance through an update set in Instance Data Replication \(IDR\).

## Before you begin

Role required: idr\_admin or admin

## About this task

You can copy a replication configuration from one instance to another using an update set. For details on using update sets, see Get started with update sets.

## Procedure

1.  On the source instance, create an update set.

    1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

    2.  Select **New**.

    3.  Enter a name for the update set.

    4.  Select **Submit and Make Current**.

    An update set is created and selected as the current update set on the source instance.

2.  Capture a producer or consumer replication configuration in the update set.

    **Note:** You can capture the following types of configurations on a producer instance:

    -   Producer replication \(one-way\)
    -   Producer replication with bi-directional replication
    -   Producer replication with discrete replication
<table id="choicetable_ap2_cnm_3yb"><thead><tr><th align="left" id="d453956e143">

Option

</th><th align="left" id="d453956e146">

Steps

</th></tr></thead><tbody><tr><td id="d453956e152">

**Capture a producer replication configuration**

</td><td>

1.  Navigate to **All** &gt; **Instance Data Replication** &gt; **Producer Replication Sets**.
2.  Create a producer replication set by selecting **New**.
3.  Select an existing producer replication set.
4.  Capture the replication configuration by selecting **Track in Update Set**.


</td></tr><tr><td id="d453956e194">

**Capture a consumer replication configuration**

</td><td>

1.  Navigate to **All** &gt; **Instance Data Replication** &gt; **Consumer Replication Sets**
2.  Create a consumer replication set by selecting **New**.
3.  Select an existing consumer replication set.
4.  Capture the replication configuration by selecting **Track in Update Set**.


</td></tr></tbody>
</table>    -   The replication set configuration is added to the Entry Sets \[idr\_entry\_set\] table.
    -   The replication entries in the replication set are added to the Replication Entries \[idr\_replication\_entry\] table.
    -   The entry set and its replication entries are captured in the current update set.
3.  Continue modifying the replication configuration as needed.

    Additional changes that you make aren't captured until you select **Track in Update Set** again.

    1.  Modify the producer replication set and select **Update**.

    2.  Capture the latest changes by selecting **Track in Update Set**.

    The latest changes are captured in the update set.

4.  Export the update set to XML.

    1.  Navigate to **All** &gt; **System Update Sets** &gt; **Local Update Sets**.

    2.  Select the current update set.

    3.  In the **State** drop-down list, select **Complete**.

    4.  Select **Update**.

    5.  In the Update Sets list, select the update set that you marked as complete.

    6.  Select the **Export to XML** related link.

    The update set is exported to an XML file on your local machine.

5.  On the target instance, import the update set.

    1.  Navigate to **All** &gt; **System Update Sets** &gt; **Update Sets to Commit**.

    2.  Select the **Import Update Set from XML** related link.

    3.  Select **Choose File** and browse to the XML file that you exported.

    4.  Select **Upload**.

    5.  In the Retrieved Update Sets list, select the update set that you imported.

    6.  Select **Preview Update Set**.

        **Note:** If you receive sys\_record\_transform errors during the preview, select all the error records that are listed in the **Update Set Preview Problems** tab, and then select **Accept Remote Update**. Repeat this action for any additional sys\_record\_transform errors that appear.

    7.  Exit the preview by selecting **Close**.

    8.  On the update set form, select **Commit Update Set**.

    The update set is imported on the target instance, including the entry set and replication entries that you captured from the source instance. If you exported the configuration for a uni-directional producer replication set, a new producer replication set is automatically created on the target instance.

6.  On the target instance, perform the following steps based on the type of replication set that you want to set up.

<table id="choicetable_i5p_kyv_hyb"><thead><tr><th align="left" id="d453956e472">

Type of replication

</th><th align="left" id="d453956e475">

Steps

</th></tr></thead><tbody><tr><td id="d453956e481">

**Producer replication**

</td><td>

1.  Navigate to **All** &gt; **Instance Data Replication** &gt; **Producer Replication Sets**.
2.  Select the new producer replication set that was automatically generated after you imported the update set.
3.  Select **Activate**.


</td></tr><tr><td id="d453956e517">

**Consumer replication**

</td><td>

1.  Navigate to **All** &gt; **Instance Data Replication** &gt; **Consumer Replication Sets**.
2.  Select the new producer consumer set that was automatically generated after you imported the update set.
3.  Subscribe the consumer replication set to a producer by completing the **Producer Instance URL** and **Producer Replication Set Name** fields.
4.  Select **Update**.


</td></tr><tr><td id="d453956e562">

**Bi-directional replication**

</td><td>

1.  Navigate to **All** &gt; **Instance Data Replication** &gt; **Producer Replication Sets**.
2.  Create a producer replication set by selecting **New**.
3.  On the Producer replication Set form, enter a value in the **Name** field.
4.  Select the **Bi-Directional** check box.
5.  In the **Entry Set** field, select the entry set that you imported from the source instance.
6.  Select **Submit**.


</td></tr><tr><td id="d453956e620">

**Discrete replication**

</td><td>

1.  Navigate to **All** &gt; **Instance Data Replication** &gt; **Producer Replication Sets**.
2.  Create a producer replication set by selecting **New**.
3.  On the Producer replication Set form, enter a value in the **Name** field.
4.  Select the **Discrete** check box.
5.  In the **Entry Set** field, select the entry set that you imported from the source instance.
6.  Select **Submit**.


</td></tr></tbody>
</table>
## Result

The replication configuration that you exported from the source instance is imported to the target instance. A new replication set based on the exported configuration is created on the target instance.

## What to do next

-   If you're setting up a producer replication set, create and subscribe one or more consumers.
-   If you're setting up a consumer replication set, approve the consumer's request on the producer instance, and then activate the consumer replication set on the consumer instance.
-   If you're setting up a bi-directional replication set, synchronize the consumer by selecting the **Synchronize Replication Entries** related link in the connected consumer replication set.
-   If you're setting up a discrete replication set, create and subscribe one or more consumers.

**Parent Topic:**[Deploying a replication configuration from one instance to another in Instance Data Replication](../concept/copying-replication-configuration.md)

