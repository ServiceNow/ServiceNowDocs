---
title: Create iCalendar invitations for custom tables
description: To generate iCalendar invitations that use field values from custom tables, create an import export map that computes the values of the iCalendar fields.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Calendar integration, Email templates, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Create iCalendar invitations for custom tables

To generate iCalendar invitations that use field values from custom tables, create an import export map that computes the values of the iCalendar fields.

## Before you begin

Role required: admin

## Procedure

1.  Create the custom table and fields using the **Date/Time** field type for the fields that map to the *$\{dtstart\}* and *$\{dtend\}* variables.

2.  In the navigation filter, enter `sys_impex_map.list`.

3.  Select **New**.

4.  Set the following fields:

    -   **Name**: Use the following naming convention: `icalendar.<table name>`. For example, **icalendar.u\_my\_custom\_table**.
    -   **Table**: Select the custom table you created.
    -   **Type**: Select **icalendar**.
5.  Right-click the form header and select **Save**.

6.  In the Field Maps related list, click **New**.

7.  In the Mapping Entry Wizard, select **Mapping to a Database Field**.

8.  Create field mappings for *dtstart* and *dtend*.

    For example, map the **External Name** *dtstart* to the**u\_meeting\_start\_time** field in u\_my\_custom\_table.

    **Note:** These variables are required.

9.  Select **Submit**.

10. Create field mappings for any of the following iCalendar fields as necessary.

    -   dstart
    -   dtend
    -   location
    -   alarm\_time
11. Select **Update**.

    Here are sample field mappings between iCalendar variables and custom fields in a custom table, u\_my\_custom\_table:

    |External name|Database field|Type|Map|
    |-------------|--------------|----|---|
    |dtstart|u\_meeting\_start\_time|field|icalendar.u\_my\_custom\_table|
    |dtend|u\_meeting\_end\_time|field|icalendar.u\_my\_custom\_table|

12. Create an email template that defines what to include in the iCalendar invitation.

    1.  Set the **Table** field to the custom table you created.

    2.  In the **Message** text field, use the following format to define the iCalendar invitation.

        ```
        
        BEGIN:VCALENDAR 
        PRODID:-//Service-now.com//Outlook 11.0 MIMEDIR//EN 
        VERSION:2.0
        METHOD:REQUEST 
        BEGIN:VEVENT 
        ATTENDEE;ROLE=REQ-PARTICIPANT;RSVP=TRUE:MAILTO:${to} 
        DTSTART:${dtstart} 
        DTEND:${dtend} 
        UID:${sys_id} 
        DTSTAMP:${dtstamp} 
        SUMMARY:${u_meeting_summary} 
        END:VEVENT 
        END:VCALENDAR
        
        ```

        **Note:** Mail script is not allowed or processed in meeting invitation email templates.

        |iCalendar template line|Required?|Notes|
        |-----------------------|---------|-----|
        |BEGIN:VCALENDAR|Yes| |
        |PRODID:-//Service-now.com//Outlook 11.0 MIMEDIR//EN|Yes| |
        |VERSION:2.0|Yes| |
        |METHOD:REQUEST|Yes| |
        |BEGIN:VEVENT|Yes| |
        |ATTENDEE;ROLE=REQ-PARTICIPANT;RSVP=TRUE:MAILTO:$\{to\}|Yes|The $\{to\} contains the recipients as defined in the notification.|
        |DTSTART:$\{dtstart\}|Yes|You must use the import export map to map dtstart to a start time field on the custom table.|
        |DTEND:$\{dtend\}|Yes|You must use the import export map to map dtend to an end time field on the custom table.|
        |UID:$\{sys\_id\}|Yes|You must provide the name of a field that uniquely identifies the record, such as the sys\_id or the record number field.|
        |DTSTAMP:$\{dtstamp\}|Yes| |
        |SUMMARY:$\{u\_meeting\_summary\}|No|To include a summary from a text field on the custom table, provide the name of the field, such as u\_meeting\_summary. The summary field value must not contain line breaks. You do not need to create a field mapping.|
        |END:VEVENT|Yes| |
        |END:VCALENDAR|Yes| |

13. Create an email notification to trigger the iCalendar invitation and ensure the following fields are set accordingly:

    -   **Table**: Select the custom table.
    -   **Type**: Select **Meeting Invitation**.
    -   **Content type**: Select **Plain text** only.
    -   **Email template**: Select the template you created.

**Parent Topic:**[Calendar integration](../reference/r_CalendarIntegration.md)

