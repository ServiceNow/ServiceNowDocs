---
title: Install Multi-Instance Setup and AMF Core
description: You can install the Multi-Instance Setup application and AMF Core plugin if you have the admin role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/install-multi-instance-setup.html
release: brazil
topic_type: task
last_updated: "2026-09-17"
reading_time_minutes: 1
keywords: [install, store application, Multi Instance Setup, AMF Core]
breadcrumb: [Multi-Instance Setup, Multi-Instance Management, Get started, Administer the ServiceNow AI Platform]
---

# Install Multi-Instance Setup and AMF Core

You can install the Multi-Instance Setup application and AMF Core plugin if you have the admin role.

## Before you begin

Review the [Multi-Instance Setup](https://store.servicenow.com/store/app/8999793cc31f831028305230a001315d) application listing in the ServiceNow Store for information on dependencies, licensing or subscription requirements, and release compatibility.

Role required: admin

## About this task

On the production instance that you want to set as the controller, you must install the Multi-Instance Setup application \(sn-app-amf\) and the AMF Core plugin \(com.glide.amf\). To detect non-production instances to manage, you must install the AMF Core plugin \(com.glide.amf\) on any non-production instance that you want a controller to manage.

Roles and tables are installed with the AMF Core plugin \(com.glide.amf\). For more information, see [Components installed with AMF Core](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/installed-with-amf-core.md).

## Procedure

1.  From a production instance, navigate to **All** &gt; **Application Manager**.

2.  Find the Multi-Instance Setup application \(sn-app-amf\) using the filter criteria and search bar.

    You can search for the application by its name or ID. If you can't find the application, you might have to request it from the ServiceNow Store.

    A list of the versions available to you are displayed.

3.  Select a version from the list and select **Install**.

    In the Review Installation Details dialog box, any dependencies installed with your application are listed.

4.  If you're prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  Select **Install**.

6.  Repeat the previous steps to install the AMF Core plugin \(com.glide.amf\) on the controller instance and each non-production instance that you want it to manage.


## What to do next

Set the production instance as the controller so you can begin managing non-production instances. For more information, see [Connecting controller and managed instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/connecting-controller-managed-instances.md).

