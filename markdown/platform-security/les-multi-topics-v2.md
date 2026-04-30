---
title: Create source type and multi topics in the LES source table
description: Consume logs for each source type by creating multiple topics per source type. You can now leverage the option of customized selection of specific topics for different log sources during the debugging process, without impacting the other log tables.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a log source configuration, Administer, Log Export Service \(LES\), Platform Security]
---

# Create source type and multi topics in the LES source table

Consume logs for each source type by creating multiple topics per source type. You can now leverage the option of customized selection of specific topics for different log sources during the debugging process, without impacting the other log tables.

## Before you begin

**Note:** If you delete a Log Source, the corresponding topic in the sys\_kafka\_topic table is not deleted. If you create the Log Source again, the existing topic can be reused, ensuring continuity and avoiding unnecessary topic recreation.

Role required: admin or sn\_logstoanalytics.admin

## Procedure

1.  Navigate to **All** &gt; **Log Export Service \(LES\)** &gt; **Sources**.

2.  Click **New** to create a new source.

    The Source form shows up. Previously, the **Topic** field was auto-filled once the **Source Type** is selected. Starting Yokohama, each source type can create their own topic. It doesn’t populate by default on selecting the **Source Type** or the **Table** name. They can be created either directly from the Kafka topics or from the reference field.

    **Note:** Since sys\_audit table has multiple log tables, no specific topic is shown in the Topic column of the Sources list. Previously, all the source types had the same topic. Now you can select different topics for different sources.

3.  Select the lookup icon to go to the list of Kafka topics.

    The list of Kafka topics shows up.

4.  Create the new Kafka topic with the following steps.

    **Note:** This step is applicable only if you want to create a new topic for a selected Source Type.

    1.  Select **New** to create a new Kafka topic for the selected Source Type. The Kafka topic form shows up.
    2.  On the form, fill up the fields.

        |Fields|Description|
        |------|-----------|
        |Name|Name of the topic you are creating|
        |Application ID|Enter sn\_logstoanalytics|
        |Namespace|Enter Default Namespace|
        |Partition|The partition field of a topic in Hermes refers to the partitions into which the topic's data is divided. It plays a key role in scalability and parallelism|

    3.  Select **Submit** to create the new Kafka topic.
5.  Select the **Source Type** you want to create for a particular topic.

6.  Select the required topic from the list for the selected **Source Type**.

7.  Select **Submit** to create the source type with the particular selections.

    The source type shows up on the Sources list with the selected topic name and other information.


**Parent Topic:**[Create a log source configuration](les-create-source-configuration.md)

