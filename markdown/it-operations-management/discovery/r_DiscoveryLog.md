---
title: Logs for horizontal discovery
description: The system collects logs to reflect the activity that takes place during a horizontal discovery based on both patterns and probes. Use the logs to fine-tune or troubleshoot the discovery process.Access the logs to understand the discovery process and fine-tune the discovery process.You can configure the amount of time that Discovery retains log entries for the probe-based horizontal discovery.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Logs for horizontal discovery

The system collects logs to reflect the activity that takes place during a horizontal discovery based on both patterns and probes. Use the logs to fine-tune or troubleshoot the discovery process.

For horizontal discovery the system generates logs of the following types:

-   **Probe-based**

    The logs for probe-based horizontal discovery cover classification failures, CMDB updates, and authentication failures. A Discovery Log record is created for each action associated with a discovery status.

    **Note:** The Discovery log also displays errors that occur during identification by taking log entries from the Identification Engine log. See [Examine run logs](https://www.servicenow.com/docs/access?context=identification-simulation&version=zurich&pubname=zurich-servicenow-platform&section=examine-identification-engine-logs&ft:locale=en-US) for more information about the identification engine and possible errors.

-   **Pattern-based**

    The logs for pattern-based horizontal discovery include the information about discoveries that were performed with patterns. A horizontal discovery log record is created for an entire horizontal discovery run, which includes the results of all the operations specified in the pattern.


## Review the logs for horizontal discovery

Access the logs to understand the discovery process and fine-tune the discovery process.

### Before you begin

Role required: discovery\_admin

### Procedure

1.  Navigate to **All** &gt; **Discovery** &gt; **Status**.

2.  Open a [Discovery Status](../concept/c_DiscoveryStatus.md) record.

    The **Discovery Log** related list displays the logs for probe-based discovery. See [Discovery log details](discovery-log.md).

    ![Discovery Log Records](../image/DiscoveryLog2.png)

3.  Find out the information related to the relevant log entry:

    -   Select the link in the **CI** column to open the record for that CI.
    -   Select the link in the **Created** column to view the log record.
    -   Select the IP address link in the **Device** column to view the log records for a particular device.
4.  To view logs for pattern-based discovery, select the **Here** link for a log entry that has **HorizontalDiscoveryProbe** in the **ECC queue input**.

    ![The link to the pattern-based discovery log.](../image/discovery-log-link-pattern-based-log.png)

    The Horizontal Discovery Log window opens showing the list of pattern-based log entries. For information on logged discovery phases, see [Discovery log details](discovery-log.md).

    ![Horizontal Discovery log](../image/horizontal-pattern-log.png "Horizontal Discovery log")

5.  Select an item in the left-hand column to see more information about it in the right-hand column.

6.  To debug the pattern, select the name of the Identification Section, and then select the **Debug** button.

7.  To return to the log record, select **Close**.


### What to do next

-   To fine-tune or troubleshoot the pattern-based discovery, retrieve the payload as described in [KB0998923: Retrieve Payload Feature](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0998923).
-   [Validate commands used in pattern-based discovery](../../it-operations-management/task/validate-discovery-commands.md), if there is one of the following errors:
    -   Authentication issue
    -   Authorization/Permission issue
    -   No Valid credentials present
    -   IP not reachable from mid
    -   Command with wrong syntax
-   If there is an error in payload processing, select the **IRE Error Documentation** button to learn about the Identification and Reconciliation Engine \(IRE\) error that occurred and how to resolve it.![Horizontal Discovery Log window showing a payload processing error](../image/discovery-log-payload-error-IRE.png)

**Related topics**  


[Identification and Reconciliation engine \(IRE\)](https://www.servicenow.com/docs/access?context=ire&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)

[KB0854603: Pattern Debugger Session Timed Out](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0854603)

## Change retention time for probe-based discovery logs

You can configure the amount of time that Discovery retains log entries for the probe-based horizontal discovery.

### Before you begin

Role required: admin

### About this task

By default, the probe-based discovery log retains information for 30 days, or 2,592,000 seconds.

### Procedure

1.  Open the Auto Flushes table by typing `sys_auto_flush.list` in the navigation filter.

2.  Open the **discovery\_status** record.

3.  Change the value in the **Age in seconds** field.

4.  For the change to take effect immediately, run the Table Cleaner Job in the Schedule \[sys\_trigger\] table.

5.  Click **Update**.


