---
title: Configure CMS sites to use single sign-on \(SSO\)
description: To configure CMS to use SSO, make the view\_content page private.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/content-management-system/t\_CMSSitesAndSingleSignOn.html
release: zurich
product: Content Management System
classification: content-management-system
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Content sites, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Configure CMS sites to use single sign-on \(SSO\)

To configure CMS to use SSO, make the view\_content page private.

## Before you begin

Role required: content\_admin or admin

## About this task

Because public pages do not require login, and CMS sites are public by default, CMS pages do not use SSO. Use the following procedure to turn off public-facing content pages and enable SSO.

## Procedure

1.  Navigate to Public Pages \[sys\_public.list\].

2.  For the view\_content page, set **Active** to **false**.


**Parent Topic:**[Content sites](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/content-management-system/c_ContentSite.md)

