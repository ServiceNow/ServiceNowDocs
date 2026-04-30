---
title: Calendar integration
description: With email notifications, you can use import export maps to leverage information about records and integrate with Outlook or another calendar.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Email templates, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Calendar integration

With email notifications, you can use import export maps to leverage information about records and integrate with Outlook or another calendar.

For example, an email notification can create a calendar event based on the planned start and end dates of a change request. To enable integration with a calendar, the following iCalendar variables are available to be added to an email template message and reference the email template from the notification. The variables must be added to the **Message Text** field.

|Variable|Description|
|--------|-----------|
|*$\{dtstart\}*|Start Date|
|*$\{dtend\}*|End Date|
|*$\{location\}*|Location|
|*$\{alarm\_time\}*|Alert or reminder time|

By default, the instance computes the value of iCalendar variables using import and export maps for the Appointment \[itil\_appointment\] and Change Request \[change\_request\] tables. The instance also uses import and export maps for other tables, depending on which plugins you activate. For example, if you activate the Incident \(com.snc.incident\) plugin, the instance uses the import and export maps of the Incident \[incident\] table.

Each import export map can specify a different set of iCalendar fields. For example, the icalendar.change\_request import export map only maps two iCalendar fields.

The instance uses the **External Name** value as the variable name in the email template. For example, the icalendar.change\_request import export map defines the *dtstart* and *dtend* variables.

|External name|Associated variable name|Table|Field mapped|Field label|
|-------------|------------------------|-----|------------|-----------|
|dtstart|*$\{dtstart*\}|change\_request|start\_date|Planned start date|
|dtend|*$\{dtend*\}|change\_request|end\_date|Planned end date|

-   **[Map date fields to iCalendar variables](../task/t_MapDateFieldsToiCalVariables.md)**  
You can specify what fields provide the date information in calendar invitation notifications by changing the field mappings of the *dtstart* and *dtend* variables in the import export map for the iCalendar invitation.
-   **[Create iCalendar invitations for custom tables](../task/t_CRiCalendarInvCustomTables.md)**  
To generate iCalendar invitations that use field values from custom tables, create an import export map that computes the values of the iCalendar fields.

**Parent Topic:**[Email templates](../concept/c_EmailTemplates.md)

