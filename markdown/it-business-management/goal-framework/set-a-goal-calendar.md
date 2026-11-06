---
title: Setting a goal calendar
description: The goal calendar decides which periods your targets use for their check-in frequency and breakdowns. You can use the Gregorian calendar or a fiscal calendar.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-business-management/goal-framework/set-a-goal-calendar.html
release: australia
product: Goal Framework
classification: goal-framework
topic_type: concept
last_updated: "2026-11-02"
reading_time_minutes: 1
audience: admin
breadcrumb: [Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Setting a goal calendar

The goal calendar decides which periods your targets use for their check-in frequency and breakdowns. You can use the Gregorian calendar or a fiscal calendar.

The goal calendar is set for the whole instance. It decides the check-in frequencies that the form displays and how their breakdowns are generated. The calendar mode is either Gregorian, which is the default, or fiscal.

With the fiscal mode, targets use the fiscal periods of your organization. The fiscal periods come from one of three fiscal calendar types: `Regular`, `445` \(4-4-5\), or `13 Period`.

Changing the calendar can make targets stale. Only targets that have breakdowns can become stale, when their stored breakdowns no longer match the goal calendar set in the system property. This happens when the check-in frequency isn't supported by the new calendar, and also when the breakdowns don't match the calendar's periods, for example after the calendar mode or the fiscal calendar type changes, or after the fiscal periods are regenerated or deleted. A target can become stale even when its check-in frequency is supported by both calendars. Targets with the check-in frequency set to **None** don't become stale. A stale target is locked until its check-in frequency is cleared. For details, see [Managing stale targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/managing-stale-targets-gf.md).

To set up a calendar, see:

-   [Switch from the Gregorian calendar to a fiscal calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/switch-from-gregorian-to-fiscal-calendar.md)

-   [Switch between fiscal calendars](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/switch-between-fiscal-calendars.md)


-   **[Switch from the Gregorian calendar to a fiscal calendar](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/switch-from-gregorian-to-fiscal-calendar.md)**  
Change the calendar mode of the instance from Gregorian to fiscal, so that targets use the fiscal periods of your organization.
-   **[Switch between fiscal calendars](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/switch-between-fiscal-calendars.md)**  
Change the fiscal calendar type of the instance, for example from a standard fiscal calendar to a 4-4-5 calendar, and regenerate the fiscal periods.

**Parent Topic:**[Configuring Goal Framework and Goal Framework for SPM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-business-management/goal-framework/configuring-goal-framework.md)

