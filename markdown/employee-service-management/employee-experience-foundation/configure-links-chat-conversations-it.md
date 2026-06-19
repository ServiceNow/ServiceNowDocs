---
title: Configure the system property to open the unfurled links
description: Configure the property to view the content when the user clicks the adaptive card shared in the Microsoft Teams chat conversation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/employee-experience-foundation/configure-links-chat-conversations-it.html
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2025-07-31"
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

    \[Omitted image "unfurl-link-option.png"\] Alt text: Unfurl link property

3.  Click the property.

    If the record is uneditable, click here to edit the record.

    \[Omitted image "edit-link-unfurl-property.png"\] Alt text: Edit the record

4.  Update the **Value** field as `false` to view the links in a browser.

    \[Omitted image "update-link-unfurl-property2.png"\] Alt text: Update unfurl link record

5.  Click **Update**.


**Parent Topic:**[Unfurl the web links in Microsoft Teams chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/employee-experience-foundation/enable-link-unfurling-it.md)

