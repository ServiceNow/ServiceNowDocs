---
title: Install Enterprise Architecture integration with Risk Management and Enterprise Architecture integration with Policy and Compliance - Legacy
description: Install Application Portfolio Management integration with Risk Management and Application Portfolio Management integration with Policy and Compliance from the ServiceNow Store.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate - Legacy, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Install Enterprise Architecture integration with Risk Management and Enterprise Architecture integration with Policy and Compliance - Legacy

Install Application Portfolio Management integration with Risk Management and Application Portfolio Management integration with Policy and Compliance from the ServiceNow Store.

## Before you begin

Role required: admin

Before installing Application Portfolio Management integration with Risk Management and Application Portfolio Management integration with Policy and Compliance, download and activate the Governance, Risk, and Compliance \(GRC\) application from the ServiceNow Store. For more information, see the [Download a GRC application from the ServiceNow Store for the first time](https://www.servicenow.com/docs/access?context=download-grc-first-time&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US) topic.

## About this task

Activate the following plugins:

|Name|Description|
|----|-----------|
|Application Portfolio Management integration with Risk Management \(com.snc.apm\_risk\_assessment\)|Activates the Application Portfolio Management integration with the GRC Risk Management plugin.|
|Application Portfolio Management integration with Policy and Compliance \(com.snc.apm\_control\_management\)|Activates the Application Portfolio Management integration with the GRC Controls plugin.|

## Procedure

1.  Navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the application using the filter criteria and search bar.

    You can search for the application by its name or ID. If you cannot find an application, you may have to request it from ServiceNow store.

    Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

3.  Click **Install**.

4.  In the Application installation dialog box, review the application dependencies.

    Dependent plugins and applications are listed if they will be installed, are currently installed, or need to be installed. If any plugins or applications need to be installed, you must install them before you can install GRC - Application Risk Assessment.

5.  If demo data is available and you want to install it, click **Load demo data**.

    Demo data comprises sample records that describe application features for common use cases. Load demo data when you first install the application on a development or test instance.

    **Important:** If you don't load the demo data during installation, it's unavailable to load later.

6.  Click **Install**.


-   **[Governance, Risk, and Compliance \(GRC\) roles required for Enterprise Architecture \(formerly Application Portfolio Management \(APM\)\) - Legacy](../concept/grc-roles-for-apm.md)**  
Add roles to the sn\_apm.apm\_user role to be able to access GRC information from Enterprise Architecture.

**Parent Topic:**[Integrating Enterprise Architecture \(formerly Application Portfolio Management\) with other applications - Legacy](../../application-portfolio-management/concept/apm-integration.md)

