---
title: Install Virtual Agent for Sourcing and Procurement Operations
description: Install Virtual Agent for Sourcing and Procurement Operations from the ServiceNow Store.
locale: en-US
release: xanadu
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Virtual Agent for Sourcing and Procurement Operations, Sourcing and Procurement Operations integration with Employee Center, Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Install Virtual Agent for Sourcing and Procurement Operations

Install Virtual Agent for Sourcing and Procurement Operations from the ServiceNow Store.

## Before you begin

Role required: admin, virtual\_agent\_admin

## About this task

Activate the following plugins:

|Name|Description|
|----|-----------|
|Glide Virtual Agent \(com.glide.cs.chatbot\)|Activates the Virtual Agent framework and other necessary plugins. This is a prerequisite for the Shopping Virtual Agent plugin to work.|
|Virtual Agent Experience Pack for Sourcing and Procurement Operations \(com.sn\_shop\_va\)|Activates a conversational bot platform for providing user assistance through conversations for Sourcing and Procurement Operations.|

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from ServiceNow store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Select **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed.

5.  If demo data is available and you want to install it, select **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Select **Install**.


**Parent Topic:**[Virtual Agent for Sourcing and Procurement Operations](../concept/virtual-agent-for-psm.md)

