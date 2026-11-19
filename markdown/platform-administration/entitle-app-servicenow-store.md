---
title: Block application entitlements from the ServiceNow Store
description: As a service provider, block one or more instances from receiving application entitlements through the ServiceNow Store. An application can be installed in any entitled instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/entitle-app-servicenow-store.html
release: zurich
topic_type: task
last_updated: "2026-08-26"
reading_time_minutes: 1
keywords: [application entitlements, entitle instance, msp, managed service provider]
breadcrumb: [Configure, ServiceNow Store, Administering applications, Get started, Administer]
---

# Block application entitlements from the ServiceNow Store

As a service provider, block one or more instances from receiving application entitlements through the ServiceNow Store. An application can be installed in any entitled instance.

## Before you begin

-   Your company must be a service provider.
-   The application must already be licensed to your company, or be available to install without a license.
-   You must be logged into the ServiceNow Store with your Now Support account credentials.

Role required: none

## About this task

Entitled instances can install applications. By default, all instances you manage are entitled to your licensed applications and free applications. Service providers can block application entitlement for any instance they manage.

If your organization isn't a service provider, all eligible instances within the organization are entitled and can install licensed and free applications.

## Procedure

1.  Log in to the ServiceNow Store using your Now Support credentials.

2.  Find and select the application in the ServiceNow Store to navigate to the listing details.

3.  Select **Manage entitlements**.

4.  Move instances from the **Available to install** column to the **Install blocked** column to prevent them from installing the application.

5.  Select **Save changes**.


## Result

Blocked instances can't install the application.

