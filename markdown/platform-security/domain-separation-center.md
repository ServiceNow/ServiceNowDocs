---
title: Domain Separation Center
description: Audit your domains regularly to reveal problems.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Domain separation for service providers, Access Management]
---

# Domain Separation Center

Audit your domains regularly to reveal problems.

## overview

The Domain Separation Center is a dashboard where you can schedule and configure audits for all of the domains stored in your domain\_audit\_definition table. The dashboard enables you to review audit results and dig deeper into domain errors and warnings. You can find the Domain Separation Center dashboard at `<ServiceNow-instance-name>/domaincenter`.

The Domain Separation Center provides many audits. You cannot create your own. You can, however, configure how often they run. Audits run on all of the domains stored in the domain\_audit\_definition table.

![Domain separation center dashboard](../image/domain-separation-center-landing-page.png)

## Configure audits

You can configure whether an audit is active and how frequently it runs.

1.  In the Domain Separation Center, select **Configure Audits**.

    The **Configure Audits** page displays.

2.  Configure each audit you want to be active. Audits are inactive by default.
    1.  Select an audit.
    2.  Select the **Active** box to activate the audit.
    3.  Specify how often the audit runs in the **Frequency** field.

        The Domain Separation Center runs all audits marked with the same frequency at the same time. Do not select **Daily** for audits run on large tables.

    4.  Repeat these steps for each audit you want to activate.
3.  Select **Save**.

## Audit schedules

Configure one or more audits to run daily, weekly, or monthly. The scheduler specifies what days and times to run those audits. All audits with the same scheduling frequency run sequentially staring at the time you configure.

1.  In the Domain Separation Center, select **Audit Schedules**.

    The **Audit Schedule** page displays.

2.  Configure the audit schedules.
    1.  Select a schedule name.
    2.  Specify the time of day to run the audit.

        Time units are measured with the 24 hour clock, that is, 14 equals 2 PM.

    3.  For weekly schedules, select the day of the week to run the audit, where 1 is Sunday.
    4.  For monthly schedules, select the day of the month to run the audit.
    5.  Repeat the procedure for the other schedules.
3.  Select **Save** to save the configuration changes.
4.  Select **Execute Now** to run all of the audits scheduled to run at the frequency shown at the top of the right pane, for example, if the pane title is, **Domain Audit Schedule - Daily**, all of the audits that run daily are run.

To see the status of a running audit, in the Domain Separation Center, select the number in the **Running Audits** box.

## Execute audits immediately

Audits typically run as scheduled. You can, however run all audits on command.

1.  In the Domain Separation Center, select **Audit Schedules**.

    The **Audit Schedule** page displays.

2.  Select the name of the audit schedule you want to run, for example, daily, weekly, or monthly.
3.  Select **Execute Now**.

To see the status of a running audit, in the Domain Separation Center, select the number in the **Running Audits** box.

## Configure the Domain Separation Center

1.  In the Domain Separation Center, select **Configure Domain Center**.
2.  On the **Configure Domain Center** page, for **Enables detail domain logging**, select **Yes** to store detailed logs that help diagnose domain-related issues. Detailed logging might cause performance issues.

    These logs refer to server-side logs in the syslog\_domain table. For information about viewing the logs, see View audits with warnings and failures.

3.  In the slushbucket, select and move all of your large tables into the **Selected** column.

    Daily audits should not run on large tables. Grayed-out table names in the **Selected** column are large and cannot be moved to the **Available** column.

4.  Select **Update**.

## View audits with warnings and failures

On the dashboard, **Errors** and **Warnings** provide detailed information about audits that encountered problems. Logs related to domain separation reside on your server in the syslog\_domain table.

1.  In the Domain Separation Center, select the number in the **Errors** or **Warnings** box.

    The **Errors** or **Warnings** page displays, respectively.

2.  Select one of the audits in the list.

    The page displays detailed information about problems with the audit you selected. The messages in **Audit Result Details** refer to values in the syslog\_domain table for table audits that revealed errors or warnings.

3.  To see the logs on the server that provide information about warning or error audits:
    1.  Copy the **Detail ID** value in the left panel of a warning or error.
    2.  In the Filter Navigator of HI, enter `syslog_domain.do`.

        The Domain Log page displays.

    3.  In the **Source** search field, enter `=<Detail-ID>` \(no space after the equals sign\), for example, =f6a00fd29a85b300a9503a81b9169678.

        The Domain Log page displays only the logs related to the audit with the Detail ID you specified. Each row in the table specifies a different record the audit found problems in. Notice that the **Message** field on this page matches the values displayed in the Domain Service Center's **Message** column. The format of the message matches the audit type.

4.  Select:
    -   **Rerun Audit**—Rerun an audit to see if it still encounters a warning or error.
    -   **Deactivate Audit**—Inactivate an audit.
    -   **Copy Details**—Copy audit details to the clipboard.

## View running and pending audits

Active audits periodically run or are queued to run, as scheduled. You can view their status as they run.

1.  Select the number in the **Running Audits** box to view audits that are currently running or pending running.

    The **Running Audits** page displays.

2.  Select an audit for more information about it.

## View inactive audits

1.  Select the number in the **Inactive Audits** box.

    The **Inactive Audits** page displays all of the audits that are currently deactivated.

2.  Select one of the audits to display more information about it.
3.  To activate an audit, select the **Active** box and use the **Frequency** field to specify how often the audit runs.
4.  Select **Update**.

