---
title: Security Incident Response integration with Zscaler
description: You can use the Security Incident Response integration with Zscaler product to connect your Zscaler Internet Access server \(ZIA\) logs with the ServiceNow AI Platform. This integration enables you to view dashboards, create custom alerts, and help you investigate security incidents.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Security Incident Response integration with Zscaler

You can use the Security Incident Response integration with Zscaler product to connect your Zscaler Internet Access server \(ZIA\) logs with the ServiceNow AI Platform. This integration enables you to view dashboards, create custom alerts, and help you investigate security incidents.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Overview

The Zscaler internet and web gateway product is delivered from the cloud. It provides you with the key data points and insights into your enterprise security environment. Security Incident Response integration with Zscaler connects the Zscaler Internet Access product with your ServiceNow AI Platform instance. By using the Zscaler product on the ServiceNow AI Platform, you get more insights into your organization’s internet usage.

## Key features of the integration

This integration includes the following key features:

-   Reputation lookup of observables against the global threat library that the Zscaler product maintains.

    **Note:** The Zscaler global threat library lists threats by trends, country of origin, target destination, volume, and various threat categories. This global threat library enables you to investigate your observables against the global threat landscape.

-   Maintenance of observables in a block list or allow list on the Zscaler product.
-   Ability to fetch and review sandbox reports from the Zscaler product for an MD5 hash. The Cloud Sandbox feature in the Zscaler product runs and analyzes files in a virtual environment to detect malicious behavior.
-   Security alerts from Patient 0 events that are generated in the Zscaler product when a user downloads an unknown malicious file.
-   Multiple URL category lists that act as block lists or allow lists as defined in the Zscaler product.
-   ServiceNow AI Platform security incidents that can be tagged to identify the URL category that the observables are added to.
-   Expiration periods that maintain the size of the URL category list entries by automatically expiring or removing the older entries.
-   Approval workflow for adding and removing observables from the URL category lists.
-   URL category entries that can be linked to observable records and security incidents that include threat intelligence results and details about why an entry is blocked.

## Learn about this integration

|Document identifier|Document title|
|-------------------|--------------|
|Zscaler product documentation website|[ZScaler Product Documentation website](https://help.zscaler.com/)|
|ServiceNow product documentation website|[ServiceNow Product Documentation website](https://servicenow.com/docs)|

