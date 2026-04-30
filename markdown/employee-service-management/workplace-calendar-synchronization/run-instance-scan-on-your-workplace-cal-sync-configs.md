---
title: Run Instance scan to check Microsoft Exchange Online synchronization configuration
description: Execute an Instance scan on your ph keyref="var.workplace-calendar-sync"/&gt; configuration with Microsoft Exchange Online. The Instance Scan application diagnoses the configurations with the calendar provider by running a series of checks using suites.
locale: en-US
release: xanadu
product: Workplace Calendar Synchronization
classification: workplace-calendar-synchronization
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage calendar synchronizations, Workplace Calendar Synchronization, Workplace Service Delivery, Employee Service Management]
---

# Run Instance scan to check Microsoft Exchange Online synchronization configuration

Execute an Instance scan on your ph keyref="var.workplace-calendar-sync"/&gt; configuration with Microsoft Exchange Online. The Instance Scan application diagnoses the configurations with the calendar provider by running a series of checks using suites.

## Before you begin

Role required: sn\_wsd\_rsvsync.admin

## About this task

Run the instance scan using the Instance Scan application to check if there are any incorrect configurations while configuring the Microsoft Exchange Online calendar provider. The scan runs and notifies about any incorrectness.

The ph keyref="var.workplace-calendar-sync"/&gt; application provides you the **Workplace Calendar Synchronization Configurations** suite in the Instance Scan application. For more information about Instance scan, refer to [Instance Scan](https://www.servicenow.com/docs/access?context=hs-landing-page&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US). You can run the suite at any time to diagnose the configurations. The suite runs the following configuration checks:

-   **Reservable Sync Configurations Check**: Checks if the reservation sync configurations are correct.
-   **Calendar Sync Active Providers Check**: Checks if there are no active providers as the sync can’t be configured.
-   **Webhook Registry Configurations Check**: Checks for callback URL and the client state in the webhook registry.
-   **Calendar Provider Configurations Check**: Checks if the active calendar provider configurations are correct.

## Procedure

1.  Navigate to **All** &gt; **Instance Scan** &gt; **Suites**.

2.  Select **ph keyref="var.workplace-calendar-sync"/&gt; Configurations**.

    The form opens. On the form, view the above checks in the Checks Related list.

3.  To run the scan, select **Execute Suite Scan**.

4.  In the Scan Suites Now window, select **Full instance**.

5.  Select **Execute Scan**.

    The scan executes and you can view the progress.

6.  On the Execute Suite Scan progress window, select **Go to Result** to view the scan results.

7.  On the Scan Result form, review the findings in the Scan Findings related list.

    In the Scan Findings related list, you can view the following information:

    -   The **Check** column displays the check that diagnosed the issue.
    -   The **Source Table** and **Source** column displays the source where the issue was found.

        The **Source** displays the record that caused the issue.

    -   The **Finding Details** column displays the details of the finding, that is, the issue and its details. Hover on the finding to view the full details. For information about the finding messages, refer to [Instance scan findings](../reference/sacn-finding-messages.md).
8.  Fix the scan findings.

9.  After fixing the issues listed in the Scan Findings related list, select **Rescan** on the Scan Result form.

    The scan displays the latest results with the implemented fixes.


**Parent Topic:**[Manage calendar synchronizations](../concept/manage-calendar-synchronizations.md)

**Related topics**  


[View synchronization details](view-synchronization-details.md)

[Events in Workplace Calendar Synchronization](../reference/events-in-workplace-calendar-synchronization.md)

[Synchronization - Prerequisites and implementation](../reference/synchronization-troubleshooting-and-conditions.md)

