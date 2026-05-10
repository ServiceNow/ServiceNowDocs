---
title: Create a pattern and a schedule for standard serverless Discovery
description: To find application CIs that reside on an unknown host, create an infrastructure pattern for standard serverless discovery. After creating the pattern, create a Discovery schedule that triggers the pattern.After you create a pattern for standard serverless discovery, create a Discovery schedule and specify the pattern. Discovery triggers the pattern from the schedule rather than from a classifier.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: task
last_updated: "2026-05-09"
reading_time_minutes: 3
breadcrumb: [Serverless Discovery, Running discoveries in your network, Using Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Create a pattern and a schedule for standard serverless Discovery

To find application CIs that reside on an unknown host, create an infrastructure pattern for standard serverless discovery. After creating the pattern, create a Discovery schedule that triggers the pattern.

## Before you begin

Role required: cloud\_admin, service\_mapping\_admin, or admin

## About this task

In the pattern, you must specify input parameters to explore the CI.

## Procedure

1.  Navigate to **All** &gt; **Pattern Designer** &gt; **Discovery Patterns**.

2.  Click **New**.

3.  Specify an **Infrastructure** type pattern with the correct CI type that applies to the CIs you want to discover.

    See [Create or customize patterns](../../service-mapping/task/t_CreatePatternPatDef.md) for an explanation of all form fields.

4.  Create an identification section and save the pattern.

5.  Click the **Input Parameters** tab, and then click **New**.

6.  Enter the parameters that are required to reach the serverless CIs.

    For example, you could enter `url` to reach a remote resource via an HTTP request.

    **Note:** You specify the actual URL in a serverless discovery schedule.

7.  Save the pattern.

8.  Click the **Basic** tab, and then click the identification section name to open the pattern designer.

9.  Create the steps you need to explore serverless CIs.

    For example, create an **Http Get Call** operation to reach a remote resource through a URL. In this case, you would specify the `$url` parameter in the **URL** field.

10. To test the pattern, click **Debug Mode** and fill in values for the input parameters.

    You do not need to enter a value for **Proxy Host**. In the this example, we are connecting to a website that serves up an XML file. The XML file parsing method is already defined in the Http Get Call operation. To test the pattern operation, click **Debug Mode**, enter the URL, and click **Connect**.

11. After you connect and run the operation, the **Output** field displays the content.


## Create a schedule for standard serverless Discovery

After you create a pattern for standard serverless discovery, create a Discovery schedule and specify the pattern. Discovery triggers the pattern from the schedule rather than from a classifier.

### Before you begin

Ensure you have [basic authentication credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/r_BasicAuthCredentialsForm.md) for HTTP calls in the pattern.

Role required: cloud\_admin, service\_mapping\_admin, or admin

### About this task

You can reuse this schedule to run the same pattern using different parameters.

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Schedules**.

2.  Click **New**.

3.  Select **Serverless** in the **Discovery** field.

    See [Schedule a horizontal discovery](t_CreateADiscoverySchedule.md#) for explanation of other fields.

4.  Right-click the form header and select **Save**.

5.  In the **Serverless Execution Pattern** related list, click **New**.

6.  Fill out the form fields \(see table\):

    |Field|Description|
    |-----|-----------|
    |Name|Provide a descriptive name.|
    |Pattern|Select the pattern you created for standard serverless discovery or for proxy host-based discovery.|
    |Proxy Host|Leave this field empty. This field applies to the host proxy-based scenario.|
    |Active|Keep this check box selected to use the pattern execution definition.|

7.  Right-click the form header and select **Save**.

8.  In the **Discovery Pattern Launcher Parameters** related list, add the parameters required by the pattern and provide a value for each one in the **Value** column.

9.  Click **Submit**.

10. Define as many serverless execution pattern records as needed.

    You can launch the same pattern, but they should have different parameters.

11. Execute discovery by clicking **Discover Now** or wait until the schedule triggers the discovery.


### Result

Check the Discovery status to see the Discovery log, the devices list, which holds the discovered CIs, and the ECC queue records. Note that the Shazzam probe did not launch and Discovery did not trigger any classification probes.

**Related topics**  


[Discovery status](../concept/c_DiscoveryStatus.md)

