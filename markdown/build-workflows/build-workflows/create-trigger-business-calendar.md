---
title: Create a scheduled trigger using business calendar
description: Schedule a recurring trigger to run based on a business calendar, so your automation run only when your business is actually operating, on working days, active shifts, or custom production schedules.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Create a scheduled trigger using business calendar

Schedule a recurring trigger to run based on a business calendar, so your automation run only when your business is actually operating, on working days, active shifts, or custom production schedules.

## About this task

When you create a scheduled recurring trigger, the trigger runs based on the specified calendar dates. The schedule does not consider if the scheduled date falls on a weekend or a public holiday. This can cause errors, missed tasks, unwanted notifications, and broken integrations. To address this problem, you can use an existing business calendar to schedule the trigger so that the automation run only during business hours.

**Note:** The trigger does not create a business calendar, it only refers an existing business calendar. To learn about business calendars, see [Creating business calendars](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/time-configuration/business-calendars.md).

## Before you begin

Role required: trigger\_designer, flow\_designer, or admin.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **New** &gt; **Trigger**.

    The New Trigger page appears![Screen to enter the details of your trigger.](../images/scheduled-trigger-biz-calendar.png).

3.  Fill in the details for your trigger.

<table id="table_vgt_tld_5fc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Trigger name

</td><td>

Unique name to identify the trigger.

</td></tr><tr><td>

Trigger type

</td><td>

Type of trigger to start your flow. Select **Scheduled** &gt; **Recurrence**

</td></tr><tr><td>

Description

</td><td>

Description of the trigger.

</td></tr><tr><td>

Application

</td><td>

Application to create the trigger. The default is Global.The application scope determines which data your trigger can access and what data it can share.

</td></tr><tr><td>

Domain

</td><td>

Domain scope of the flow. For more information about domain separation, see [Domain separation explained](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-what-is-domain-separation.md).

</td></tr></tbody>
</table>4.  Select **Show additional properties** and fill any additional properties.

    |Field|Description|
    |-----|-----------|
    |Accessible from|Choice between whether the trigger data should be accessible only from the specified application or all application scopes.|
    |Protection|Option to make the trigger read-only.|
    |Category|Category where your trigger is displayed.|
    |Trigger annotation|Annotation for your trigger that the user can see before they select it.|

5.  Select **Build trigger**.

6.  On the Trigger definition form, specify the **Scheduling Details**.

    ![Form to specify the scheduling details for the trigger](../images/business-calendar-scheduling.png)

<table id="table_umj_g3l_k3c"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

**Business calendar**

</td><td>

Select the business calendar that you want to use.

</td></tr><tr><td>

**Business calendar type**

</td><td>

Specify if you want the trigger to run at the start or end of an entry in the business calendar. For example, start of the week or end of the week.

</td></tr><tr><td>

**Offset option**

</td><td>

Select if you want to differ the trigger schedule from the business calendar entry.The options are:

-   **No offset**
-   **after**
-   **before**
If you select **before** or **after**, the form displays an **Offset number** field.

![Specify the offset time in the offset number field.](../images/buniess-calendar-trigger-offset.png)

Specify the offset time in the **Offset number** field. For example, run the trigger 60 minutes before the shift starts.

</td></tr><tr><td>

**Business calendar condition**

</td><td>

Specify the condition if you want to exclude certain business calendar entries from the trigger schedule.

</td></tr></tbody>
</table>7.  To make the trigger available, select **Publish**.


## Result

The trigger is created and published. You can use the trigger in any of your flows. For information about adding a trigger to a flow, see [Use a saved trigger](use-saved-trigger.md).

**Parent Topic:**[Create a saved scheduled trigger](create-scheduled-trigger.md)

