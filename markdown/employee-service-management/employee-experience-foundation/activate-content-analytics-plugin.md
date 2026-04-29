---
title: Activate Content Analytics
description: Activate Content Analytics if you have an admin role to use the default analytics solution that provides web portal traffic analytics, as well as Content Experiences \(aka Campaigns\) related engagement statistics.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Content Analytics, Setup continuous improvement, Configuring Employee Center Pro, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Activate Content Analytics

Activate Content Analytics if you have an admin role to use the default analytics solution that provides web portal traffic analytics, as well as Content Experiences \(aka Campaigns\) related engagement statistics.

## Before you begin

Role required: admin

## About this task

Content Analytics requires the following plugins to collect data and generate dashboards:

|Plugin|Description|
|------|-----------|
|Content Analytics \[sn\_cda\]|Collects data and provides basic metrics on page views and user sessions|
|Content Publishing \[sn\_cd\]|Provides data from content published through Content Publishing|
|Content Experiences \[sn\_ca\]|Provides data from content published through Content Experiences|
|Performance Analytics - Portal Analytics \[sn\_cdap\]|Enhances dashboards with content profiling and time window filters|
|Performance Analytics - Content engagement Analytics \[sn\_ca\_pa\]|Enhances dashboards with campaign filters enabling users to view campaign-specific analytics and engagement over time for to-do content|

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from the ServiceNow Store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select a version from the list and select **Install**.

    In the Install dialog that is displayed, any dependencies that are installed along with your application are listed.

4.  If you are prompted, follow the links to the ServiceNow Store to get any additional entitlements for dependencies.

5.  If demo data is available and you want to install it, select the **Load demo data** check box.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Select **Install**.


## What to do next

[Content Analytics](../concept/ecpro-content-automation-analytics.md)

**Related topics**  


[Components installed with Content Analytics](../reference/ecpro-installed-content-analytics-1.md)

