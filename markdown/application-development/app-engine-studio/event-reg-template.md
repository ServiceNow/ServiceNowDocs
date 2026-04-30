---
title: Event Registration template
description: Build an application in App Engine Studio \(AES\) using the Event Registration template to manage scheduling, booking, and registration for company events.The following tables, experiences, automated workflows, and roles are included in the Event Registration template for App Engine Studio \(AES\).
locale: en-US
release: zurich
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Available templates, Use an app template, Create your app, Build, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Event Registration template

Build an application in App Engine Studio \(AES\) using the Event Registration template to manage scheduling, booking, and registration for company events.

To use the Event Registration template, install this application from the ServiceNow Store.

An internal event registration app allows your event organizers to publish a list of events to employees and collect attendees in a centralized database. The app helps streamline the event discovery and registration process.

Event organizers can manage events and wait-lists, publish new events, and view registered users’ details. Employees and attendees can view a list of events, view event info, and register to attend in a portal. Organizers can set the size of the event, and requesters will automatically be added to a wait-list.

For more information on creating an application using a template, see [Use an application template](../task/use-app-template.md).

**Parent Topic:**[Available templates](template-library.md)

## Event Registration template contents

The following tables, experiences, automated workflows, and roles are included in the Event Registration template for App Engine Studio \(AES\).

### Tables in the Event Registration app template

<table id="table_idd_hgt_j4b"><thead><tr><th>

Table label \[name\]

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attendee Table\[x\_&lt;company-code&gt;\_&lt;attendee&gt;\]

</td><td>

Track event attendee information such as name, status, and date of submission.

</td></tr><tr><td>

Event Table\[x\_&lt;company-code&gt;\_&lt;event&gt;\]

</td><td>

Track event information such as event name, date of the event, and capacity.

</td></tr><tr><td>

Event Location Table\[x\_&lt;company-code&gt;\_&lt;event\_location&gt;\]

</td><td>

Track event location details such as capacity and location.

</td></tr></tbody>
</table>### Experiences in the Event Registration app template

|Experience|Experience type|Description|
|----------|---------------|-----------|
|Event Location \| Workspace|Form|Workspace where organizers and admins can configure events, create event applications, and view lists.|
|*App name*Portal|Portal|Main portal for organizers to create and view details about the event.|
|Attendee \| Default view|Form|Form that attendees can use to view the event name, change their status, and take notes about the event.|
|Event \| Default view|Form|Form that organizers can use to create events.|
|*App name* Workspace|Workspace|Workspace where users can register for an event and where admins/organizers can manage registration information.|
|Event Location \| Default view|Form|Form for organizers to add event location name, location address, status, and capacity.|
|Event \| Workspace|Form|Form for organizers to add event name, location details, timelines, and comments.|
|Attendee \| Workspace|Form|Form for attendees to register for events and add notes about the event.|
|Mobile app for organizers|Mobile experience|Organizers can view or edit events and view attendees using your organization's iOS or Android app.|

### Automated workflows in the Event Registration app template

|Workflow name|Workflow type|Description|
|-------------|-------------|-----------|
|Event Details Have Changed|Email|Notifies users/attendees of changes to the event.|
|Event Reminder - Confirmed attendees|Email|Sends a reminder about the event to confirmed attendees.|
|Attendee registered confirmed|Email|Notifies attendees of confirmed registration.|
|Send Event Reminder Email|Flow|Sends a reminder email to event attendees.|
|Send Event Details Changed Email|Flow - record|Sends an email to all confirmed and waitlisted attendees when details of an event have changed or the event was cancelled.|
|Send Waitlist Confirmation Email|Flow - record|Sends an email to attendees when they are added to the waitlist of an event.|
|Event Registration cancelled events|Flow - record|Updates attendee records when an event is cancelled.|
|Update Event Registration attendee records|Flow|Updates attendee records when an event is cancelled or is past the end date.|
|Attendee waitlisted confirmed|Email|Confirms attendees on event waitlist.|
|Event Registration expired events|Flow|Sets the **Event state** field to Expired and the **Attendees** field to Event ended after the event ends.|
|Send On Hold Confirmation|Flow - record|Allows for organizers to send an email to attendees when they are on-hold to attend an event.|
|Event Registration Confirmation Email|Flow - record|Sends an email to attendees when they are confirmed to attend an event.|
|Attendee registration on hold|Email|Informs attendees that their registration is on hold.|
|Event Has Been Cancelled|Email|Informs users of event cancellation.|
|Event Registration Process Flow|Flow|Processes all pending requests.|

### Roles in the Event Registration app template

<table id="table_wdt_jht_j4b"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Organizer\[x\_&lt;company-name&gt;\_&lt;my events app&gt;.organizer\]

</td><td>

Organizers create and manage events.

</td><td>

Create, Read \(all\), Update \(all\).

</td></tr><tr><td>

Attendee\[x\_&lt;company-name&gt;\_&lt;my events app&gt;.attendee\]

</td><td>

Attendees can search, sign up, and RSVP to events.

</td><td>

Create, Read \(all\), Update \(own\).

</td></tr><tr><td>

Admin\[x\_&lt;company-name&gt;\_&lt;my events app&gt;.admin\]

</td><td>

Admins configure event locations and applications.

</td><td>

Create, Read \(all\), Update \(all\), Delete.

</td></tr><tr><td>

Public\[x\_&lt;company-name&gt;\_&lt;my events app&gt;.public\]

</td><td>

No login is required to access features or functions with the public role.

</td><td>

No access by default.

</td></tr></tbody>
</table>