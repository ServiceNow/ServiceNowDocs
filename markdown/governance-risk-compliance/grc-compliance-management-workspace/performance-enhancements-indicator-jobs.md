---
title: Performance enhancements for Indicator nightly job
description: To support parallel processing capabilities, two additional custom queues such as the Indicator Data Queue for processing indicators, and the Supporting Data Queue for handling events related to control, risk, and issue updates and to collect the supporting data, have been introduced.
locale: en-US
release: yokohama
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Manage control indicators using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Performance enhancements for Indicator nightly job

To support parallel processing capabilities, two additional custom queues such as the Indicator Data Queue for processing indicators, and the Supporting Data Queue for handling events related to control, risk, and issue updates and to collect the supporting data, have been introduced.

## New architecture for effective processing of indicators

The execution of indicators has been optimized by implementing a three-step process, utilizing two custom queues for efficient processing.

In the initial step, a set of indicators requiring processing is queued up in the Batch Indicator Data Queue. The Batch Indicator Data Processor then runs the indicators, sets the status, and creates the indicator results or tasks. The indicators are then moved to another custom queue for supporting data collection and updating dependent objects like controls, risks, and issues.

In the second step, the Indicator Supporting Data Processor picks up the indicator records from the Indicator Supporting Data Queue and updates the control or risk status, also creating or updating issues based on the configuration. Then the indicator is pushed to the Indicator Statistics Table for support data collection.

Finally, the Supporting Data Collection Job picks up the indicator records from the Supporting Data Statistics Table, starts collecting supporting data for the indicators, and leverages both the default queue and additional custom queues for efficient processing.

**Note:** Indicator result business rules are not executed during the indicator job run. However, the same business rules are used while completing the indicator task. The indicator business rules are moved to the indicator job for achieving better performance during the execution.

![Workflow illustrating the processing of indicator jobs using additional queues](../image/indicator-enhance-architect.png "Processing indicator jobs using additional queues")

This architecture supports execution of a large number of indicators in significant time. The Supporting Data Collection Job introduced to collect supporting data improves the data handling process considerably. Moreover, the time taken to execute the data is considerably less.

**Note:** The Supporting Data Collection Job assigns the batches of indicator records to the default queue initially for supporting data collection. Depending on the availability of the batch processing queue and supporting data queue, the scheduled job assigns the subsequent batches of indicator records to these queues in a round-robin fashion, that is, only if these queues are free to process them.

## Data model changes

The **Sample collection type** field added in the Indicator template form, has options either **Count** or **Percentage**. The default value is Count. If you select Percentage, you can provide the percentage value to collect the supporting data.

The **Due date duration \(days\)** field is added for manual indicator in the Indicator template and Indicator forms to capture the indicator task due date. Based on this due date, reminder emails are sent to the indicator task owners.

A new field introduced in the indicator supporting data table, which is of type JSON, helps in efficient data management.

-   For more information related to the table changes, see [Tables installed with Governance, Risk, and Compliance](../../grc-common/reference/tables-installed-with-grc.md).
-   For more information on the additional system properties, see [Governance, Risk, and Compliance properties](../../grc-common/reference/grc-properties.md).
-   For Indicator form changes, see [Create a GRC indicator](../../grc-indicators/task/t_CreateAnIndicator.md).
-   For the Indicator template form changes in Compliance Workspace, see [Create a GRC indicator template using the Compliance Workspace](../task/create-grc-indicator-template-ws.md).
-   For the Indicator template form changes in the classic UI, see [Create a GRC indicator template](../../grc-indicators/task/t_CreateIndicatorTemplate.md).

