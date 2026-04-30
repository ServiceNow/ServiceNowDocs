---
title: Install Virtual Agent for PPM
description: Install Virtual Agent for PPM from the ServiceNow store.
locale: en-US
release: xanadu
product: Project Management
classification: project-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Virtual Agent for PPM, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Install Virtual Agent for PPM

Install Virtual Agent for PPM from the ServiceNow store.

## Before you begin

Role required: admin

## About this task

To install Virtual Agent for PPM, activate the following plugins:

|Name|Description|
|----|-----------|
|PPM Standard \(com.snc.financial\_planning\_pmo\)|Activates the PPM Standard basic plugin for the PPM \(Project Portfolio Management\) applications.|
|Glide Virtual Agent \(com.glide.cs.chatbot\)|Activates the Virtual Agent framework and other necessary plugins.|
|Virtual Agent for PPM \(com.sn\_ppm\_va\)|Activates a conversational bot platform for providing user assistance through conversations within a messaging interface for PPM.|

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from ServiceNow store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If there are any plugins or applications that need to be installed, you must install them before you can install Virtual Agent for PPM.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Click **Install**.


