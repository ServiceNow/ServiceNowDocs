---
title: CSM Configurable Workspace form ribbon and components
description: The form ribbon provides includes components that display relevant information about a case and provide agents with a quick overview of the case details. These components can include a contact or consumer summary, a timeline, and SLA details.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-12-16"
reading_time_minutes: 8
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Configurable Workspace form ribbon and components

The form ribbon provides includes components that display relevant information about a case and provide agents with a quick overview of the case details. These components can include a contact or consumer summary, a timeline, and SLA details.

In addition to viewing case information, agents can use links in the ribbon components to place phone calls or create email messages. Agents can also show or hide the ribbon as needed by clicking a button at the top of the ribbon.

## Customer Service Management ribbon components

For Customer Service Management, you can configure the ribbon for the Case form to include one or more of the available ribbon components:

-   Customer 360
-   Timeline
-   Active SLAs
-   Time to resolve component

## Customer 360 ribbon component

The Customer 360 component displays customer information such as the contact or consumer name, email address, and phone numbers.

![Component showing customer contact information, including name, email address, and phone numbers.](../../../product/customer-service-management/image/csm-workspace-customer360-component.png "Customer 360 ribbon component")

You can configure the Customer 360 component to display different fields, such as the fields described in the following table.

<table id="table_idt_zmj_npb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Header

</td><td>

The header includes customer information. -   For B2B customers: Displays either the **Primary Contact** or **Contact**.
-   For B2C customers: Displays the **Consumer**.
-   For internal contacts with the proxy contact role \(sn\_customerservice.proxy\_contact\): Displays the **Internal contact**.

**Note:** Requires the CSM Extension for Proxy Contacts \(com.snc.csm\_proxy\_contacts\) plugin.


</td></tr><tr><td>

Avatar

</td><td>

A graphic representation of the customer's identity, such as an image or icon.

</td></tr><tr><td>

Name

</td><td>

The customer's name.

</td></tr><tr><td>

Title

</td><td>

The customer's title.

</td></tr><tr><td>

Account

</td><td>

For B2B customers, the account associated with the contact.

</td></tr><tr><td>

Phone numbers

</td><td>

-   For contacts: **Mobile phone** and **Business phone**
-   For consumers: **Mobile phone** and **Home phone**

</td></tr><tr><td>

Email address

</td><td>

The customer's email address.

</td></tr></tbody>
</table>The Customer 360 component supports dot walking on selected reference tables. You can display fields from these tables:

-   User \[sys\_user\]
-   Contact \[customer\_contact\]
-   Consumer \[csm\_consumer\]

If you configure the Customer 360 component to display information from a dot-walked field, the label for that field shows the `Column` name instead of the `Table.Column` name.

**Note:** For B2B customers, the Customer 360 component can also include colored tags that indicate Very Important Person \(VIP\) accounts and escalated accounts.

From the Customer 360 component, agents can perform the following actions.

<table id="table_kbv_c1t_rdb"><thead><tr><th>

Action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email a contact or consumer

</td><td>

Agents click the address in the **Email** field to send an email to the contact or consumer. This action opens a new email in the email editor with the following fields auto-populated:-   **To**: the contact or consumer email address
-   **Subject**: the case number and short description

</td></tr><tr><td>

Call a contact or consumer

</td><td>

If phone integration is enabled, agents click a number in one of the phone number fields to call the contact or consumer. The OpenFrame window displays information about the contact or consumer name and the account.

</td></tr><tr><td>

View the account record

</td><td>

Agents click the **Account** link to open the account record.

</td></tr></tbody>
</table>## Timeline ribbon component

The timeline component displays a chronological summary of case activities, including case state changes and interactions between the agent and the requester \(typically the customer\). It also shows how much time that the fulfiller and requester spent on the case.

**Note:** The workspace administrator can select the agent role when configuring the timeline component attributes.

![Timeline component displaying a summary of case activities and the time spent on each case. For the color code information, refer to the legend row in the Timeline features table.](../image/timeline-ribbon-component.png "Timeline ribbon component")

The timeline uses icons to display events and colors to show ranges of time, such as when the case is with the agent or the customer. Agents can point to event icons in the timeline to display tooltips with additional information.

**Note:** The timeline component uses the resolution shaper configuration for the selected entity table, for example, the Case table.

The timeline includes the following features:

<table id="table_h5t_xxj_sjb"><thead><tr><th>

Timeline feature

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Global start and end dates

</td><td>

The global start date is the date that the case was created. The global end date is the date that the case was closed.

</td></tr><tr><td>

Start and end dates

</td><td>

The start and end dates that identify a specific window of time on the timeline. The default window is one week. -   The default end date is the current date.
-   The default start date is the current date minus 7 days.

</td></tr><tr><td>

Header

</td><td>

A configurable title for the timeline. With the system administrator role, you can add a title in the **Name** field on the Ribbon Setting form.

</td></tr><tr><td>

Legend

</td><td>

Click **Show Details** to display event and range summary information. ![Legend summary displaying events and the range of time spent on activities.](../image/timeline-ribbon-component-details.png "Legend summary information")

</td></tr><tr><td>

Events

</td><td>

Events are represented on the timeline using icons. Each type of event has a corresponding unique icon. The time that an event occurred is also captured so that events are displayed on the timeline in chronological order.

</td></tr><tr><td>

Grouped events

</td><td>

Events that occur close together can be grouped and represented using a group icon. When events are grouped, the timeline displays a badge icon with the number of events in the group.

</td></tr><tr><td>

Event summaries

</td><td>

Event summaries appear in the timeline legend. Each summary lists the event and the number of times it occurred. **Note:** An event summary includes occurrences of the event over the life of the object visualized on the timeline.

</td></tr><tr><td>

Time ranges

</td><td>

Time ranges are represented on the timeline using colors. Each range has a corresponding unique color and a start and end time. The following default ranges include:-   Green: with the agent
-   Blue: with the customer

</td></tr><tr><td>

Time range summaries

</td><td>

Time range summaries appear in the timeline legend. Each summary lists the range, the corresponding color, and the total duration. **Note:** A range summary includes occurrences of the range over the life of the object visualized on the timeline.

</td></tr><tr><td>

Tooltips

</td><td>

Point to event icons to display additional information.

</td></tr><tr><td>

Zoom

</td><td>

Zoom in on the timeline to see more details in a smaller time window or zoom out to see more events in a larger time window. -   Click the zoom in or zoom out icons on the timeline.
-   Use the zoom in and zoom out features on the keyboard \(**Ctrl** + **+** and **Ctrl** + **-**\).
-   Use the zoom in and zoom out features on the cursor.

</td></tr><tr><td>

Pan

</td><td>

Pan left and right to view newer or older events. -   Pan left in the timeline to view older events by clicking the left caret icon \(**&lt;**\). Panning to the left stops when the timeline reaches the specified global start date.
-   Pan right in the timeline to view newer events by clicking the right caret icon \(**&gt;**\). Panning to the right stops when the timeline reaches the specified global end date.

</td></tr><tr><td>

Reset the timeline

</td><td>

Click **Now** to reset the timeline to the default view after panning or zooming. The timeline resets using the time that the button was clicked as the end date and time.

</td></tr><tr><td>

Messages

</td><td>

The timeline displays messages for the following events:-   There is no data to be displayed.
-   The timeline experiences a loading error.

</td></tr></tbody>
</table>## Active SLA component

The Active SLA component displays active SLAs for the case, including time remaining, the SLA state, and any breaches. If a case has multiple SLAs, the SLA with the most imminent deadline is shown first. Pointing to the SLA component displays left and right navigation arrows that agents can use to view the other SLAs.

![SLA ribbon displaying the time remaining for the SLA. For the color code description, refer to the text that follows.](../image/SLARibbonComponent.jpg "SLA ribbon component")

Color coding within the component indicates the time remaining for the SLA:

-   Green: 0–50%
-   Yellow: 50–75%
-   Orange: 75–99%
-   Red: 100% or breached

## Time to resolve component

The time to resolve component displays the estimated time required for an agent to resolve the case.

**Note:** The time to resolve component requires the Predictive Intelligence for Customer Service Management plugin \(com.snc.csm\_ml\). For more information, see [Estimated time to resolve a case](../../../product/customer-service-management/concept/ettr.md).

![Ribbon component displaying the estimated time required by an agent to resolve a case.](../image/time-to-resolve.jpg "Time to resolve component")

In this image, the estimated time that the agent will need to resolve the opened case is 0 to 2 days. Hence, the upper bound value is displayed. The estimated time is calculated from the time the case was created. If the range for example, is between 2 to 4 days, both the lower and upper bound values are displayed.

The **Time to resolve** component also displays the prediction for SLA breach if the case is attached to an SLA.

Following are a list of SLA messages displayed and the action required when they appear.

|SLA messages|Task|
|------------|----|
|No resolution SLA exists for this case|Set the value in the **Target** field to **Resolution** in the **SLA Definition** form.|
|Repair resolution SLA to add breach time|Click **Repair** on the Task SLA form.|
|Highly likely to breach resolution SLA|None|
|Highly unlikely to breach resolution SLA|None|
|Likely to breach resolution SLA|None|
|Unlikely to breach resolution SLA|None|

## Configuring ribbon components

You can configure ribbon components as follows:

-   For CSM Agent Workspace, you can configure the ribbon layout if you have the workspace administrator role \(workspace\_admin\). This includes the components to display in the ribbon, the order in which the components appear, and the component width. You can also configure display attributes for some of the components.

    For some of the components, you can also configure attributes, such as the fields to include in the Customer 360 component.

-   For CSM Configurable Workspace, you can create a ribbon setting and add that setting to a ribbon configuration. For more information, see [Set up a ribbon configuration in CSM Configurable Workspace](../../../product/customer-service-management/task/config-csm-config-ws-ribbon.md).

    **Note:** One ribbon configuration, **CSM/FSM Configurable Workspace Ribbon Config**, is included with CSM Configurable Workspace.


You can also display the form ribbon in the Contextual side panel. For more information, see [Display the form ribbon and form header secondary values in the Contextual side panel](../../../product/customer-service-management/task/config-csm-display-header-in-sidebar.md).

Ribbon configurations in CSM workspaces support domain separation.

