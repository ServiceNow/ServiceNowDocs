---
title: Configure Walk-up Experience locations
description: Administrators define walk-up locations while setting up the walk-up experience for an organization. Requesters see this information when they schedule appointments or check in at a service location.
locale: en-US
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Walk-up Experience for Customer Service Management, Set up self-service, Configure, Customer Service Management]
---

# Configure Walk-up Experience locations

Administrators define walk-up locations while setting up the walk-up experience for an organization. Requesters see this information when they schedule appointments or check in at a service location.

## Before you begin

Role required: sn\_csm\_walkup.walkup\_admin

## About this task

Administrators can configure the following for locations:

-   Create or modify walk-up location queues or mark locations as inactive.
-   Allocate schedules for appointments, AWA conditions.
-   Set conditions to automatically route work items.
-   Location unavailable temporarily.
-   Location address and picture.
-   Specify reasons-for-visit options.
-   Configure how interactions display for each walk-up location.

## Procedure

1.  Navigate to **All** &gt; **CSM Walk-up Experience** &gt; **Administration** &gt; **Walk-up Locations**.

2.  Select **New**.

3.  Complete the form.

<table id="choicetable_zss_y2m_wlb"><thead><tr><th align="left" id="d269165e109">

Fields

</th><th align="left" id="d269165e112">

Description

</th></tr></thead><tbody><tr><td id="d269165e118">

**Name**

</td><td>

Provide a detailed name for the location, such as the city or building.

</td></tr><tr><td id="d269165e127">

**Description**

</td><td>

Provide a description of the location, if desired.

</td></tr><tr><td id="d269165e136">

**Schedule**

</td><td>

Select a schedule for operation days and hours.

</td></tr><tr><td id="d269165e145">

**Appointment Booking**

</td><td>

Add and configure an appointment booking schedule for the walk-up location.

</td></tr><tr><td id="d269165e158">

**Service Channel**

</td><td>

Search for and choose the **Walk-up** service channel.

</td></tr><tr><td id="d269165e170">

**Define condition here**

</td><td>

Select whether to route work items to this queue automatically using a condition.

</td></tr><tr><td id="d269165e179">

**Condition mode**

</td><td>

Choose either **Simple** mode or **Advanced** mode to route work to the queue automatically. Simple mode is the default. With simple mode, you can select from prebuilt conditions. For example, select **Location is X** \[search and select location\]. With advanced mode, you can provide your own scripting and code.

</td></tr><tr><td id="d269165e200">

**Work item routing condition**

</td><td>

Configure and specify who would provide customer support at a walk-up location. Location is determined by physical address.

</td></tr><tr><td id="d269165e209">

**Active**

</td><td>

Check to make this queue location active.

</td></tr><tr><td id="d269165e218">

**Enable away state**

</td><td>

Check to allow an away state.

</td></tr><tr><td id="d269165e228">

**Away message**

</td><td>

Specify a display message for when the location is temporarily closed. Specify this for hours other than the scheduled closed times.

</td></tr><tr><td id="d269165e237">

**Stockroom**

</td><td>

Select a stockroom to supply assets for the location.

</td></tr><tr><td id="d269165e246">

**Location**

</td><td>

Select the physical address of your location.

</td></tr><tr><td id="d269165e255">

**Location image**

</td><td>

Click to add an image of your location. For example, the image of the city or building where the walk-up location is located.Image types include .gif, .jpg/.jpeg, or .png. For more information, see [Image field type](https://www.servicenow.com/docs/access?context=t_UsingImageFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td id="d269165e270">

**Access Type**

</td><td>

Select external or both types of users so that the appropriate walk-up locations are visible to users.

</td></tr></tbody>
</table>4.  Select the **Management** tab to complete the Management form section.

<table id="choicetable_xc1_xhm_wlb"><thead><tr><th align="left" id="d269165e291">

Fields

</th><th align="left" id="d269165e294">

Description

</th></tr></thead><tbody><tr><td id="d269165e300">

**Position notification**

</td><td>

Select the queue position that triggers a notification to visitors when they're close to being assisted at the location. For example, when a visitor is third in line to be assisted.

</td></tr><tr><td id="d269165e309">

**Last check-in**

</td><td>

Specify the last available check-in time in minutes. For example, 30 minutes before closing.

</td></tr><tr><td id="d269165e318">

**Enable online check-in**

</td><td>

Allow visitors to check in to the location remotely from a laptop or mobile phone.

</td></tr><tr><td id="d269165e327">

**Enable appointment delegation**

</td><td>

Enable users to book an appointment for someone or else. **Note:** When you enable appointment delegation, the **Appointment delegation group** field appears. Select a group to allow appointment delegation. Add a new group of users if an appropriate group doesn't exist. Only users in this group would have the choice of scheduling for themselves or another user when they book an appointment.

</td></tr><tr><td id="d269165e343">

**Name configuration**

</td><td>

Select a name configuration to display visitor information on the onsite queue TV monitor and online check-in screen. The first name displays. However, you can show first and last name, first name with last name initial only, or first name only.

</td></tr><tr><td id="d269165e352">

**Appointment routing time**

</td><td>

Specify the amount of time, in minutes, to route the work item to an agent prior to an appointment time.

</td></tr><tr><td id="d269165e361">

**Hold time**

</td><td>

Enter an amount of time, in minutes, that you want to put an interaction on hold before attempting to route it again to a technician. For example, entering `5` would put the interaction on hold for five minutes before rerouting.

</td></tr><tr><td id="d269165e373">

**Show estimated wait time**

</td><td>

Enable the estimated wait time to show for walk-up queues. **Note:** The wait time is calculated from the average wait time of the queue and how many users are currently in the queue. All estimated wait times are rounded to the nearest whole minute.

The estimated wait time calculation requires the use of Service Owner Workspace to calculate the average wait time. Service Owner Workspace uses the Advanced Work Assignment queueing system to obtain the average wait time.

Estimated wait times are displayed in the following places:

-   Online check-in.
-   Onsite check-in and onsite queue screen \(TV\).
-   **Status** widget on the Service Portal


</td></tr><tr><td id="d269165e414">

**Audio Playback**

</td><td>

Specify when the audio confirmation plays, for example, when a requester checks into an onsite queue, when a requester checks in online, or both. The default mode is **None**.

</td></tr><tr><td id="d269165e426">

**Audio File**

</td><td>

Specify an audio file to play when a requester checks into a queue. The base system default file is walkup\_checkin.mp3. **Note:** Only mp3 file formats are supported across all browsers.

You may have to provide additional browser permissions to use an audio file on the Safari browser.

</td></tr></tbody>
</table>5.  Select the **Administration** tab to complete the administration section of the form.

<table id="choicetable_mts_y3m_wlb"><thead><tr><th align="left" id="d269165e452">

 

</th><th align="left" id="d269165e454">

 

</th></tr></thead><tbody><tr><td id="d269165e459">

**Queue time display**

</td><td>

Choose from **None**, **Check-in time**, or **Time waited** to be displayed on the location wall monitor.

</td></tr><tr><td id="d269165e477">

**Queue message**

</td><td>

Specify a welcome message for your location wall monitor.

</td></tr><tr><td id="d269165e486">

**Check-in greeting**

</td><td>

Create a check-in message to guide visitors to sign into the queue at the designated check-in monitor.

</td></tr><tr><td id="d269165e495">

**Closed message**

</td><td>

Create a message to alert visitors that it is outside the hours of operation and the location is closed.

</td></tr><tr><td id="d269165e505">

**Closed phone number**

</td><td>

Select your country from the drop-down menu to display the Customer Support phone number.

</td></tr><tr><td id="d269165e514">

**Closed record producer**

</td><td>

Search for and select a record producer to display and link to during closed hours, such as **Create incident**.

</td></tr><tr><td id="d269165e526">

**Closed image**

</td><td>

Click to add an image indicating the walk-up location is closed. The image displays on the wall monitor to alert walk-in visitors that the location is closed.

</td></tr><tr><td id="d269165e535">

**Max search results**

</td><td>

Specify how many search results to provide for contextual searches.

</td></tr><tr><td id="d269165e544">

**Contextual search config**

</td><td>

Configure which search context would provide results at the location.

</td></tr><tr><td id="d269165e553">

**Appointment type**

</td><td>

Option to set the type of appointment the requesters can book for the location. The following options are available. -   In-person
-   Remote
-   Both
 **Note:** This field is not a default field. You can configure the form layout to add this field.

</td></tr><tr><td id="d269165e578">

**Enable unregistered user entry**

</td><td>

Check to allow users who don't have a user name in the system to check in to the location for support. For example, guests visiting the location \(opposed to employees\).

</td></tr><tr><td id="d269165e587">

**Enable lookup user entry**

</td><td>

Check so users can see and select their names from a list as they begin typing their names.

</td></tr><tr><td id="d269165e596">

**Enable technician info**

</td><td>

Check to allow the display of available technician names on the location wall monitor.

</td></tr><tr><td id="d269165e605">

**Enable technician avatar**

</td><td>

Check to allow the display of technician avatars on the location wall monitor.

</td></tr><tr><td id="d269165e614">

**Header logo**

</td><td>

Click to add a header logo. The header logo is location-specific. If no logo is specified, by default, the Walk-up Portal logo is used.

</td></tr><tr><td id="d269165e623">

**Queue logo**

</td><td>

Click to add a logo for the designated walk-up location wall monitor. Design this logo to work correctly with a black background. If no logo is specified for the queue, by default, the Header logo is used. If no Header logo is specified, the Walk-up Portal logo is used.

</td></tr></tbody>
</table>6.  Right-click in the form header and select **Save**.

    Several tabs appear.

    -   **Interactions**
    -   **Walk-up Appointments**
    -   **Reasons for Visit**
    -   **Assignment Eligibility**
    -   **Work Item Sort Order**
7.  Click the **Interactions** tab to view interactions or configure how the walk-up Interactions list should display.

8.  Click the **Walk-up Appointments** tab to view appointments or configure how the Walk-up Appointments list should display.

9.  Click the **Reasons for Visit** tab to view, modify, or create a reason for visit option.

    The base system includes three active reasons:

    -   **I need something**
    -   **Something is not working**
    -   **Laptop refresh**
    -   **Other**
10. Click the **Assignment Eligibility** tab to view, modify, or create an assignment rule for your walk-up queue locations.

    Assignment rules are configured in the Advanced Work Assignment product.

11. Click the **Work Item Sort Order** tab to view, modify, or create a Work Item Sort Orders for your walk-up queue locations.

12. Click **Update** to save the new or modified location queue.


