---
title: Schedule and retrieve LogRhythm alarms
description: After you preview the security incident with the LogRhythm alarms that you have selected and mapped, you are ready to schedule alarm retrieval. After you complete this step, the alarm profile is ready to be activated.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Creating an alarm profile for LogRhythm, LogRhythm Overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Schedule and retrieve LogRhythm alarms

After you preview the security incident with the LogRhythm alarms that you have selected and mapped, you are ready to schedule alarm retrieval. After you complete this step, the alarm profile is ready to be activated.

## Before you begin

Role required: sn\_si.admin

## About this task

Scheduling permits you to modify the scheduling and the types of alarms selected for retrieval. You filter the alarms you ingest based on a date range or on specific alarm IDs. With this step, you determine whether you want to ingest historical alarms, and how often you poll for future alarms that match the alarm profile configuration.

## Procedure

1.  Click the **Scheduling** step on the progress bar.

    ![Scheduling highlighted on progress bar.](../image/logrhythm_scheduling.png)

2.  Choose from the following options to configure your alarm retrieval.

<table id="choicetable_lvr_kdr_f2b"><thead><tr><th align="left" id="d124547e87">

Option

</th><th align="left" id="d124547e90">

Description

</th></tr></thead><tbody><tr><td id="d124547e96">

**Enable incremental alarm retrieval**

</td><td>

Default is selected. Select this option to retrieve incremental alarms.

</td></tr><tr><td id="d124547e105">

**Polling interval \(in minutes\)**

</td><td>

The ServiceNow AI Platform instance pulls from the LogRhythm Client Console for new alarms every one minute. If mapped alarms are found, and filtering criteria are matched, security incidents are created.

 This setting can be changed, however, the default setting balances alarm ingestion against server load and retrieves the most current data.

</td></tr><tr><td id="d124547e126">

**Next Alarm ingestion time \(estimated\)**

</td><td>

Displays when the next scheduled ingestion would occur for the current alarm profile. This is only an estimated time.

</td></tr><tr><td id="d124547e135">

**Enable historical alarm retrieval**

</td><td>

Default is cleared. No historical data is pulled.If selected, the following fields are displayed. Choose one to configure retrieval either by date or alarm ID.

-   **Enable pulling start date**

Default is cleared. Select this option to enable the pulling date.

-   **Pulling start date**

Default is cleared. Select this option to set the pulling start date. Click the calendar icon to enter a date and time. Alarms are pulled from the date and time you enter to the current date.

-   **Ingest specific alarm Alarm ID\(s\)**

Default is cleared. Select this option to ingest specific alarm Alarm IDs.

-   **AlarmID\(s\)**

Enter specific alarm IDs. You pull the specified alarms, and you can enter multiple alarm IDs separated by commas.

**Note:** After a historical, one-time pull of alarms is completed, this check box is cleared. You will need to select this check box again before you execute another one-time pull of historical alarms.

</td></tr></tbody>
</table>3.  To edit Historical alarm retrieval, follow these steps to enter a date for alarm retrieval or a specific Alarm ID.

    1.  Select **Enable pulling start date**, and then select **Pulling start date**.

    2.  In the **Pulling start date** field, click on the calender that is displayed, select the date followed by the green check mark to save your entry.

        ![Task: Select the date in the calendar and save it with green check mark.](../image/logrhythm-scheduling-ingestion.gif)

        The date is displayed.

    3.  Alternatively, select **Ingest specific Alarm ID\(s\)** option, and in the **AlarmID\(s\)** field, enter the specific Alarm IDs for the historical data to retrieve specific alarm IDs.

        You can enter up to five alarms separated by commas.

    4.  Click **Update**.

4.  Choose one of the following options to continue editing or complete the configuration.

    |Option|Description|
    |------|-----------|
    |**Update**|Save your data and remain on the form.|
    |**Additional Options \(in the progress bar\)**|To go to the Additional Options step.|
    |**Previous**|Return to Preview step.|
    |**Delete**|Delete this alarm profile and the Alarm Profile list is displayed.|


## What to do next

After you configure the Ongoing Alarm Ingestion and One Time Retrieval details, the next step is to [Additional options for LogRhythm alarms](verify-alarm-closure-logrhythm.md).

**Parent Topic:**[Creating an alarm profile for LogRhythm](create-alarm-profile-logrhythm.md)

