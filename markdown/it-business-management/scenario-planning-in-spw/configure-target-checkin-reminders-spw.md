---
title: Configure check-in due date reminders for targets
description: Set how many days before a target's review due date the owner and contributors are reminded, based on the target's check-in frequency.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/scenario-planning-in-spw/configure-target-checkin-reminders-spw.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-10-28"
reading_time_minutes: 1
audience: admin
breadcrumb: [Configuring goals in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Configure check-in due date reminders for targets

Set how many days before a target's review due date the owner and contributors are reminded, based on the target's check-in frequency.

## Before you begin

Role required: sn\_gf.goal\_admin

## About this task

Reminders are sent a set number of days before the review due date of a target. The number of days depends on the check-in frequency of the target. Targets without a check-in frequency use the `none` setting.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **System Properties**.

2.  Search for and open the **sn\_apw\_advanced.target\_checkin\_due\_date\_reminder\_config** system property.

3.  In the **Value** field, set the number of days before the review due date for each check-in frequency.

    The value is a JSON object. Each key is a check-in frequency and each value is a whole number of days. The default value is:

    ```
    {
      "none": 7,
      "weekly": 2,
      "monthly": 5,
      "period": 5,
      "quarterly": 7,
      "yearly": 10
    }
    ```

4.  Select **Update** to save the changes.


## Result

When a target's review due date is the number of days in the configuration away, its owner and contributors receive a reminder. If the property is empty, the default values are used.

**Parent Topic:**[Configuring goals in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/configuring-goal-framework-apw.md)

**Related topics**  


[Fiscal calendar support for targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/scenario-planning-in-spw/fiscal-calendar-support-targets.md)

