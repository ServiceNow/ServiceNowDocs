---
title: Configure Field Service Management Virtual Conferencing Integration
description: Install and set up the Field Service Management Virtual Conferencing Integration application to interact with customers and peer agents using Zoom or Microsoft Teams meetings initiated from the Now Agent mobile application.
locale: en-US
release: australia
product: Field Service Integrations
classification: field-service-integrations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integration with Virtual Conferencing, Integrating Field Service Management with other applications, Configure, Field Service Management]
---

# Configure Field Service Management Virtual Conferencing Integration

Install and set up the Field Service Management Virtual Conferencing Integration application to interact with customers and peer agents using Zoom or Microsoft Teams meetings initiated from the Now Agent mobile application.

## Before you begin

Role required: admin

## About this task

This task provides general steps to set up the Field Service Management Virtual Conferencing Integration application to initiate conference calls using Zoom and Microsoft Teams from the Now Agent mobile application.

## Procedure

1.  Configure the conference call bridge.

<table id="choicetable_jgg_bsy_t4b"><thead><tr><th align="left" id="d51396e89">

To

</th><th align="left" id="d51396e92">

Do this

</th></tr></thead><tbody><tr><td id="d51396e98">

**Set up the Zoom meeting**

</td><td>

1.  Integrate the Zoom account of your company with your ServiceNow instance using the Zoom spoke.

For more information, see [Setup Zoom spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-zoom.md).

2.  Set up the Notify Zoom connector in Zoom for associating the Notify communication channel with Zoom meetings.

The conference call details of the Zoom meetings are stored in the Notify Conference Calls \[notify\_conference\_call\] table. For more information, see [Notify Zoom connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/notify-zoom-connector.md).

3.  Configure a conference provider or a phone number to be used as choices for initiating a conference call.

For more information, see [Configure a provider in Notify](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/notify/configure-providers-for-provider-selectors.md).

</td></tr><tr><td id="d51396e168">

**Set up the Microsoft Teams meeting**

</td><td>

1.  Integrate the Microsoft Teams account of your company with your ServiceNow instance using the Microsoft Teams Communication spoke.

For more information, see [Set up the Microsoft Teams Communications spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-msteams-comm.md) .

2.  Set up the Notify connector for Microsoft Teams in Microsoft Teams for associating the Notify communication channel with Microsoft Teams meetings.

The conference call details of Microsoft Teams meetings are stored in the Notify Conference Calls \[notify\_conference\_call\] table.

</td></tr></tbody>
</table>2.  Install the Field Service Management Virtual Conferencing Integration application.

    For more information, see [Install Field Service Management Virtual Conferencing Integration](install-virtual-conferencing-fsm.md).

3.  Add the **Conferences** related list to the work order task form.

    If the related list does not already appear, right-click the **Work Order Task** form header and select **Configure** &gt; **Related Lists**. Use the dual listbox to add the Conferences-&gt;Work Order Task related list.

    **Note:** You must personalize the Conferences related list to get detailed information about the conference recordings for work order tasks. For more information, see [Customize the display of conference recording information](personalize-conference-list.md).


-   **[Customize the display of conference recording information](personalize-conference-list.md)**  
Customize the Conferences related list to display specific information about conference recordings for work order tasks.

**Parent Topic:**[Integration with Virtual Conferencing](../concept/virtual-conference-integration-fsm.md)

