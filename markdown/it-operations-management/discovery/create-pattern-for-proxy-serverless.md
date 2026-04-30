---
title: Create a pattern and a schedule for host-based serverless Discovery
description: To find application CIs that reside on a known host in your CMDB, create an infrastructure pattern for host-based serverless discovery. After creating the pattern, create a Discovery schedule that triggers the pattern.Discovery triggers the pattern for host-based, serverless Discovery from the schedule rather than from a classifier.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Serverless Discovery, Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Create a pattern and a schedule for host-based serverless Discovery

To find application CIs that reside on a known host in your CMDB, create an infrastructure pattern for host-based serverless discovery. After creating the pattern, create a Discovery schedule that triggers the pattern.

## Before you begin

Role required: cloud\_admin, service\_mapping\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Discovery Patterns**.

2.  Click **New**.

3.  Specify an **Infrastructure** type pattern with the correct CI type that applies to the CIs you want to discover.

    See [Create or customize patterns](../../service-mapping/task/t_CreatePatternPatDef.md) for an explanation of all form fields.

4.  Create an identification section and save the pattern.

5.  Add operations to the pattern to discover the CI that you can access via the host.

6.  To test the pattern, click **Debug Mode** and enter the IP address of the host.


## Create a schedule for host-based serverless Discovery

Discovery triggers the pattern for host-based, serverless Discovery from the schedule rather than from a classifier.

### Before you begin

Ensure you have credentials for the host device that acts as the proxy.

Role required: cloud\_admin, service\_mapping\_admin, or admin

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Schedules**.

2.  Click **New**.

3.  Select the **Serverless** in the Discovery field.

    See [Schedule a horizontal discovery](t_CreateADiscoverySchedule.md#) for explanation of other fields.

4.  Right-click the form header and select **Save**.

5.  In the **Serverless Execution Pattern** related list, click **New**.

6.  Fill out the form fields \(see table\):

    |Field|Description|
    |-----|-----------|
    |Name|Provide a descriptive name.|
    |Pattern|Select the pattern you created for host-based discovery.|
    |Proxy Host|If you are using host-based discovery, specify an existing CMDB CI. Discovery uses the credentials of this CI when exploring the CIs on the host.|
    |Active|Keep this check box selected to use the pattern execution definition.|

7.  Right-click the form header and select **Save**.

    Define as many serverless execution pattern records as needed. You can launch the same pattern, but they should have different parameters.

    **Note:** You do not need to create entries in the **Discovery Pattern Launcher Parameters** related list.

8.  Execute discovery by clicking **Discover Now** or wait until the schedule triggers the discovery.


### Result

Check the Discovery status to see the Discovery log, the devices list, which holds the discovered CIs, and the ECC queue records. Note that the Shazzam probe did not launch and Discovery did not trigger any classification probes.

