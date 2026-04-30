---
title: Exploring Firewall Audits and Reporting
description: With Firewall Audits and Reporting, you have the capability to explore and conduct an inventory of your firewall security policies, devices, device groups, and manager information. Additionally, you can utilize it to submit requests for new firewall rules and audit security policies within a specified time frame.
locale: en-US
release: zurich
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2025-07-29"
reading_time_minutes: 2
breadcrumb: [Firewall Audits and Reporting, ITOM Visibility, IT Operations Management]
---

# Exploring Firewall Audits and Reporting

With Firewall Audits and Reporting, you have the capability to explore and conduct an inventory of your firewall security policies, devices, device groups, and manager information. Additionally, you can utilize it to submit requests for new firewall rules and audit security policies within a specified time frame.

## Firewall Audits and Reporting overview

A firewall device acts as a network security system, monitoring and controlling traffic based on specific policies. It establishes a protective barrier between trusted internal and untrusted external networks, incorporating multiple security policies to safeguard against threats. Ongoing maintenance and audits are crucial as security policies evolve, preventing potential loopholes. The firewall audit process streamlines rule tracking and updating, ensuring alignment with company security policies. Firewall vendors, including Panorama, provide centralized managers for efficient control over devices and policies.

## Firewall Audits and Reporting workflow

The Firewall Audits and Reporting application enables the ServiceNow Discovery process to discover firewalls \(currently Palo Alto Networks firewalls\), CMDB CIs for the firewall devices, firewall manager, firewall device groups, and firewall policies using serverless patterns. Firewall policy audit tasks are generated from the firewall managers or devices. You can also request new firewall security policies through the Service Catalog and archive older firewall rule requests, audit requests, and audit tasks to improve system performance. For more information, see [Visibility to Firewall inventory](use-firewall-audit-rep.md). To see various reports to track discovered policies and audit tasks, see [Firewall Admin Workspace dashboard](firewall-admin-workspace-dashboard.md).

## Firewall Audits and Reporting benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Up-to-date inventory of firewall security policies, devices, device groups, and manager information by persistently storing data in the CMDB through regular queries to a firewall manager.|[Visibility to Firewall inventory](use-firewall-audit-rep.md)|Firewall Admin \[sn\_disco\_firewall.firewall\_admin\]|
|Provision for requesting a new firewall rule using the Service Catalog.|[Firewall rule requests](firewall-requests.md#)|Firewall Requester \[sn\_disco\_firewall.firewall\_requester\]|
|Provision for auditing firewall security policies for a specific time period.|[Firewall Admin Workspace dashboard](firewall-admin-workspace-dashboard.md)|Firewall User \[sn\_disco\_firewall.firewall\_user\]|

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

