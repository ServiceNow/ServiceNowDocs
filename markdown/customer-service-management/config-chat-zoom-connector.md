---
title: Configure Chat Zoom Connector
description: Install and set up the Chat Zoom Connector application to interact with customers using Zoom meetings initiated from a chat.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Chat Zoom Connector, Chat channel, Enable communication channels, Configure, Customer Service Management]
---

# Configure Chat Zoom Connector

Install and set up the Chat Zoom Connector application to interact with customers using Zoom meetings initiated from a chat.

## Before you begin

Role required: admin

## About this task

This task provides general steps to set up the Chat Zoom Connector application for initiating Zoom meetings from a chat.

## Procedure

1.  Integrate the Zoom account of your company with your ServiceNow instance using the Zoom spoke.

    For more information, see [Set up the Zoom spoke](https://www.servicenow.com/docs/access?context=setup-zoom&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

2.  Set up the Notify Zoom connector in Zoom for associating the Notify communication channel with Zoom meetings.

    The conference call details of the Zoom meetings are stored in the Notify Conference Calls \[notify\_conference\_call\] table. For more information, see [Set up Notify Zoom connector](https://www.servicenow.com/docs/access?context=setup-notify-zoom-connector&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

3.  Install the Chat Zoom Connector application.

    For more information, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

    **Note:** The Chat Zoom Connector application installs the CSMZoomInteractionImpl script include, which is preconfigured for the Customer Service application. It also installs the sn\_chat\_zoom.ZoomInteractionExtPoint extension point, which enables the copying of any application-specific fields from the parent chat interaction record to the Zoom interaction record. For more information, see [Configure application-specific field values for Zoom interactions](config-chat-zoom-ext-pt.md).

4.  Activate the Zoom quick action.

    For more information, see [Activate the quick action for Zoom meetings](activate-chat-zoom-quick-action.md).


**Related topics**  


[Chat Zoom Connector](../concept/chat-zoom-connector.md)

[Using Chat Zoom Connector](../concept/using-chat-zoom-connector.md)

