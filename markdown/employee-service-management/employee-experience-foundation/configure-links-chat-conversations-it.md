---
title: Configure the system property to open the unfurled links
description: Configure the property to view the content when the user clicks the adaptive card shared in the Microsoft Teams chat conversation.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Unfurl the web links in Microsoft Teams chat, IT Service Management integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Configure the system property to open the unfurled links

Configure the property to view the content when the user clicks the adaptive card shared in the Microsoft Teams chat conversation.

## Before you begin

Role required: admin

## About this task

Setting the property to true opens all the configured portal-related links within the application. All the non-portal links are opened in the browser.

By default, this property is set as true. If you set the property as false, all the links shared in the chat conversations will be opened in the browser.

## Procedure

1.  In your ServiceNow instance, search for sys\_properties.list.

2.  In the Name column, search for `sn_now_teams.link_unfurl.view_action_choice` property.

    ![Unfurl link property](../images/unfurl-link-option.png)

3.  Click the property.

    If the record is uneditable, click here to edit the record.

    ![Edit the record](../images/edit-link-unfurl-property.png)

4.  Update the **Value** field as `false` to view the links in a browser.

    ![Update unfurl link record](../images/update-link-unfurl-property2.png)

5.  Click **Update**.


**Parent Topic:**[Unfurl the web links in Microsoft Teams chat](../concept/enable-link-unfurling-it.md)

