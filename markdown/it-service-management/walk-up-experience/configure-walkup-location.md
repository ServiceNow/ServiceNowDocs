---
title: Create or modify Walk-up Experience locations
description: Create or customize the predefined Walk-up Experience location. Walk-up Experience locations contain all the information about the walk-up support venue. You can define the way each location or support venue works.
locale: en-US
release: yokohama
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Configure, Walk-up Experience, IT Service Management]
---

# Create or modify Walk-up Experience locations

Create or customize the predefined Walk-up Experience location. Walk-up Experience locations contain all the information about the walk-up support venue. You can define the way each location or support venue works.

## Before you begin

Role required: sn\_walkup.walkup\_admin, sn\_walkup.walkup\_manager, or admin

## About this task

You can configure walk-up locations for work schedules, appointment bookings, assignment groups, and associate stockrooms. Set up management and administrative rules for your walk-up location. Specify reasons-for-visit options and configure how interactions display for each walk-up location.

## Procedure

1.  Navigate to **All** &gt; **Walk-up Experience** &gt; **Administration** &gt; **Walk-up Locations**.

2.  To create or modify an existing walk-up location, do one of the following:

    -   To create a new walk-up location, click **New**.
    -   To modify an existing location, select the walk-up location from the list.
3.  On the form, fill in the fields.

<table id="table_kyn_gfv_ndb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the location. For example, `Santa Clara tech lounge`.

</td></tr><tr><td>

Description

</td><td>

Description of the location.

</td></tr><tr><td>

Schedule

</td><td>

Schedule of work operation days and hours that the walk-up location follows.

</td></tr><tr><td>

Appointment Booking

</td><td>

Appointment booking plan for the walk-up location. For more details, see [Booking walk-up appointment](../concept/walkup-appointment-booking.md).

</td></tr><tr><td>

Service channel

</td><td>

Service channel that the agents work on. Select the **Walk-up** service channel.

</td></tr><tr><td>

Define condition here

</td><td>

Option to route work items to a queue using a condition.

</td></tr><tr><td>

Condition mode

</td><td>

Condition modes to define the routing of work items. The available options are as follows:-   **Simple**
-   **Advanced**
 This field appears only when the option **Define condition here** is selected.

</td></tr><tr><td>

Work item routing condition

</td><td>

Condition that defines who provides customer support at a walk-up location. Location is determined by physical address.This field appears only when **Simple** is selected from the **Condition mode** field.

</td></tr><tr><td>

Active

</td><td>

Option to set the walk-up location as active.

</td></tr><tr><td>

Enable away state

</td><td>

Option to set the location in a non-operational or closed state.

</td></tr><tr><td>

Away message

</td><td>

Display message to indicate that the location is temporarily closed for the specified time. The message is specified for work hours other than the scheduled closed times.

</td></tr><tr><td>

Stockroom

</td><td>

Stockroom that supplies assets to the location.

</td></tr><tr><td>

Location

</td><td>

Physical address of the location.

</td></tr><tr><td>

Location image

</td><td>

Picture of the location. For example, a picture of the city, building, or work-desks of the walk-up location.

</td></tr></tbody>
</table>4.  Select the **Management** tab and fill in the fields.

<table id="table_xgr_chv_ndb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Position notification

</td><td>

Queue position at which a requester is sent a notification. For example, if the position notification is set to **3**, the requester receives a notification that is third in line to be assisted.

</td></tr><tr><td>

Last check-in

</td><td>

Last available check-in time in minutes. For example, 30 minutes before closing.

</td></tr><tr><td>

Enable online check-in

</td><td>

Option to set this location for online checking in. Allow requesters to check in to the location remotely from a laptop or mobile phone.

</td></tr><tr><td>

Enable kiosk

</td><td>

Option to enable the kiosk feature at the location.

</td></tr><tr><td>

Show kiosk

</td><td>

Option to show the kiosk on the portal and on the on-site display monitor.

</td></tr><tr><td>

Enable appointment delegation

</td><td>

Option to enable agents and requesters to book an appointment on behalf of someone else.

</td></tr><tr><td>

Appointment delegation group

</td><td>

Group of people who can book an appointment on behalf of the requester or agent. Add a new group of requesters if an appropriate group does not exist.This field appears only when the **Enable appointment delegation** field is selected.

</td></tr><tr><td>

Maximum appointments per user

</td><td>

Maximum number of appointments that a requester can book at a location. This field is automatically set to 1.**Note:** If maximum number of appointments per user is changed or modified, existing appointments are not affected. The change is applied to all future appointment bookings.

</td></tr><tr><td>

Name configuration

</td><td>

Option to display the information of the requesters on the on-site queue display monitor and on the online check-in screen. You can display the names in any of the following manners: -   First name \(by default\)
-   First name and last name
-   First name with initials of last name


</td></tr><tr><td>

Appointment routing time

</td><td>

Time defined, in minutes, to route the work item to an agent prior to an appointment.

</td></tr><tr><td>

Hold time

</td><td>

Time defined, in minutes, that you want to put an interaction on hold before attempting to route it again to an agent. For example, if this field is set to **5**, then the interaction is put on hold for 5 minutes before rerouting it to the other agent.

</td></tr><tr><td>

Show estimated wait time

</td><td>

Option to display the estimated wait time for a requester in walk-up queues. The wait time is calculated from the average wait time of the queue and how many requesters are currently in the queue. All estimated wait times are rounded to the nearest whole minute.

 The estimated wait time calculation requires the use of the Advanced Work Assignment queueing system to calculate the average wait time.

 Estimated wait times are displayed at the following places:

-   Online check-in.
-   On-site check-in and on-site queue display monitor.
-   **Status** widget on the Service Portal


</td></tr><tr><td>

Audio Playback

</td><td>

Specify when the audio confirmation will play. For example, when a requester checks into an on-site queue or checks in online or both, the audio is played. This field is automatically set to **None**.

</td></tr><tr><td>

Audio File

</td><td>

Audio to play for the following walk-up queue conditions: -   When a requester checks into a queue, audio is played from the actual check-in location, typically a stationary laptop.
-   When a new requester moves up in the queue, audio is played from the queue display monitor.
-   When a requester makes an appointment online, audio is played from the device of the requester.
 The base-system default file is `walkup_checkin.mp3`.

**Note:** Only `mp3` file formats are supported across all browsers.

You may need to provide additional browser permissions to use an audio file on the Safari browser.

</td></tr></tbody>
</table>5.  Click the **Administration** tab and fill in the fields.

<table id="table_jc4_khv_ndb"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Queue time display

</td><td>

Choice to display the time on the on-site display monitor. Choices are as follows:-   None: If you do not want any display.
-   Check-in time: The check-in time of the requester.
-   Time waited. Time remaining for the requester to check in.


</td></tr><tr><td>

Queue message

</td><td>

Welcome message to display on the on-site display monitor of the location.

</td></tr><tr><td>

Check-in greeting

</td><td>

Greeting message to guide the requester to sign into the queue at the designated check-in monitor.

</td></tr><tr><td>

Closed message

</td><td>

Message to inform the requesters that the location is closed as it is outside the hours of operation.

</td></tr><tr><td>

Closed phone number

</td><td>

Contact phone number for requesters to reach out to, when the location is closed.

</td></tr><tr><td>

Closed phone number label

</td><td>

Label defined for the contact information. For example, `IT Support`, `Customer Support`, or `HR Support`.

</td></tr><tr><td>

Closed record producer

</td><td>

Mode of reaching out to the service providers when the location is closed. For example, if the option is set to **Create Incident**, the requesters are redirected to create incidents.

</td></tr><tr><td>

Badge Check-in Reason

</td><td>

Reason for checking into a walk-up location. This field is automatically set to **Other**.**Note:** Badge scan check-in is not an authentication mechanism.

</td></tr><tr><td>

Badge Check-in reason description

</td><td>

Description of the reason for checking in. This field is automatically set to **Walk-up badge scan check-in**.**Note:** Badge scan check-in is not an authentication mechanism.

</td></tr><tr><td>

Closed image

</td><td>

Picture or an image indicating that the walk-up location is closed. The image is displayed on the on-site display monitor.

</td></tr><tr><td>

Maximum search results

</td><td>

Number of search results to provide for contextual searches.

</td></tr><tr><td>

Contextual search config

</td><td>

Context that the requesters use while checking in or booking an appointment.

</td></tr><tr><td>

Appointment type

</td><td>

Option to set the type of appointment the requesters can book for the location. The following options are available. -   In-person
-   Remote
-   Both


</td></tr><tr><td>

Enable unregistered user entry

</td><td>

Option to allow requesters who do not have a user name in the system to check into the location for support. For example, such requesters can be non-employees who are guests visiting the location.

</td></tr><tr><td>

Enable lookup user entry

</td><td>

Option to enable requesters to quickly see their names on the list when they start typing.

</td></tr><tr><td>

Enable technician info

</td><td>

Option to display the names of the agents on the monitor at the location.

</td></tr><tr><td>

Enable technician avatar

</td><td>

Option to display the avatar of the agent on the wall monitor at the location.

</td></tr><tr><td>

Enable badge check-in notification

</td><td>

Option to show a notification when a requester checks into a queue using a badge scanner.

</td></tr><tr><td>

Header logo

</td><td>

Option to add a header logo. The header logo is location-specific. If no logo is specified, by default, the Walk-up Portal logo is used.

</td></tr><tr><td>

Queue logo

</td><td>

Option to add a logo for the designated on-site display monitor. Design this logo to work with a black background. If no logo is specified for the queue, then the Header logo is used by default. If no Header logo is specified, the Walk-up Portal logo is used.

</td></tr></tbody>
</table>6.  Right-click in the form header and select **Save**.

    The following tabs appear:

    -   **Interactions**: View interactions or configure how the walk-up interactions list is displayed.
    -   **Walk-up Appointments**: View appointments or configure how the Walk-up appointments list is displayed.
    -   **Reasons for Visit**: View, modify, or create a reason for visit.

        **Note:** For configuring variable time slots feature in Walk-up Experience, you must use this tab for mapping the advance configurations with the service configuration rule. For more information, see [Configure variable time slots for appointment booking](config-variable-time-slots.md).

    -   **Walk-up Location Kiosks**: Modify or create a kiosk for the location.
    -   **Assignment Eligibility**: View, modify, or create an assignment rule for your walk-up locations.

        Assignment rules are configured in the Advanced Work Assignment application.

    -   **Work Item Sort Order**: View, modify, or create a work order for your walk-up locations.
    -   **Location Queues Badge Readers**: View, modify, or add a badge reader for your walk-up locations.
7.  To save the new or modified walk-up location, Select **Update**.


**Parent Topic:**[Configuring Walk-up Experience](../concept/walkup-experience-configuration.md)

