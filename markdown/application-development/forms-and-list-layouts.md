---
title: Forms and list layouts
description: Forms and list layouts control how an app's data appears to users. A form displays a single record so users can view or edit it. A list displays multiple records so users can browse, filter, and find the data they need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/forms-and-list-layouts.html
release: australia
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 2
keywords: [getting started guide, low-code development]
breadcrumb: [Build your first app, Standard app development, Getting Started guide for developers, Building applications]
---

# Forms and list layouts

Forms and list layouts control how an app's data appears to users. A form displays a single record so users can view or edit it. A list displays multiple records so users can browse, filter, and find the data they need.

## What are forms and list layouts?

-   Forms show one record at a time and determine which fields a user sees.
-   List layouts show many records at once and determine which columns appear.
-   Customizing both helps ensure users only see data that is relevant to their role and task.
-   Every table in your app has a default form and list layout that you can modify.

## What is a form layout?

When a user opens a record, a form layout determines which fields appear on the page, in what order, and how they are grouped. You define the form layout so that users see only the fields they need, reducing confusion and data entry errors.

For example, if your app tracks IT requests, your form layout might show the requester name, description, priority, and status fields, but hide internal fields that only administrators need.

Every table in ServiceNow has at least one form layout. You can create multiple layouts for the same table to serve different audiences, such as one view for requesters and another for fulfillment teams.

## What is a list layout?

A list layout determines which columns appear when users view multiple records from a table. When a user searches for a record or browses your app's data, the list layout controls what information is visible at a glance.

For example, a list layout for IT requests might show the request number, requester, status, and date opened columns. This lets users quickly scan and find the record they need without opening each one individually.

## Why do both matter for your app?

Forms and list layouts work together to shape the user experience of your app. A well-designed form layout guides users through data entry. A well-designed list layout helps users find and triage records efficiently.

Configuring both helps ensure your app presents data in a way that matches your users' actual workflow, rather than exposing every field on every table by default.

**Parent Topic:**[Build your first application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/build-your-first-app.md)

