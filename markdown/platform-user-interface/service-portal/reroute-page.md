---
title: Redirect a reference to a page ID
description: Redirect all references from Service Portal widgets to route to a new page with a single record to avoid manually replacing the hard-coded page ID in widgets.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating portal pages, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Redirect a reference to a page ID

Redirect all references from Service Portal widgets to route to a new page with a single record to avoid manually replacing the hard-coded page ID in widgets.

## Before you begin

Role required: sp\_admin

## About this task

Multiple widgets in Service Portal can link to a single page using a hard-coded page ID. This process allows you to replace page references in widgets without locating and replacing all references to the page ID by cloning and updating each widget.

To redirect all references to a page, create a record in the Page Route Map \[sp\_page\_route\_map\] table. This table enables you to redirect a reference to a page without cloning base system widgets.

Creating a record in the Page Route Map table only redirects references to a page. It doesn’t redirect navigation to a page ID within a URL.

**Note:** You don't need to create a page route map to redirect users to a 404 page. To specify the 404 page for your portal, update the **404 page** field in the Portal \[sp\_portal\] record.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Page Route Maps**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Short Description|Optional short description to describe the redirect.|
    |Service Portal\(s\)|Portals that apply the redirect. If you don't select a portal, the redirect applies to all portals in the instance.|
    |Route from|Original page you’re redirecting from.|
    |Route to|Page you’re redirecting to.|
    |Active|Whether the Page Route Map record is active. The redirect only applies when the record is active.|
    |Roles|Roles to which the page route map applies. Users that don't have any of the roles specified in this field aren't redirected to the new page. If no roles are specified, the page route map is applicable to all users.|
    |Order|Priority of the Page Route Map record. If more than one active record has the same value in the **Route from** field, the record with the lowest order applies. The system evaluates records from lowest to highest. If multiple records have a matching order, the system honors the oldest record.|

4.  Select **Update**.


## Result

All references to the page listed in the **Route from** field redirect to the page in the **Route to** field.

**Parent Topic:**[Creating portal pages](../concept/c_Pages.md)

