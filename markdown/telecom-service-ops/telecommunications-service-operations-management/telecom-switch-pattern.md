---
title: Telecom Switch Pattern
description: The ServiceNow Telecom Discovery application uses the Telecom Switch discovery pattern to find SNMP-based Telecom switches in the network. Discovering some of these resources requires updating the Telecommunications Discovery Patterns \(TSOM Patterns\) from the ServiceNow Store.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Direct Discovery with Discovery Patterns, Telecom Discovery, Telecom Visibility, Explore, Telecommunications Service Operations Management]
---

# Telecom Switch Pattern

The ServiceNow® Telecom Discovery application uses the Telecom Switch discovery pattern to find SNMP-based Telecom switches in the network. Discovering some of these resources requires updating the Telecommunications Discovery Patterns \(TSOM Patterns\) from the ServiceNow® Store.

Telecom Discovery uses the Telecommunications Discovery Patterns to run Horizontal Discovery. This Telecommunications Discovery Pattern uses a set of SNMP requests to find, classify, and discover network elements.

Telecom Switch pattern is part of the Telecommunications Discovery Patterns application \(sn\_tsom\_patterns\), which is part of TSOM Visibility.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Subscription to TSOM.
-   Confirm that your network router devices have SNMP access.
-   On the ServiceNow® instance, configure SNMP credentials. For more information, see [SNMP support for Discovery](https://www.servicenow.com/docs/access?context=c_SNMPSupportForDiscovery&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).
-   For setting up TSOM Patterns, see [Install Horizontal Discovery and set up Discovery Patterns](../task/install-horizontal-telecommunication-discoverypatterns.md).

## Impacted CMDB CIs and CI Relationships \(Physical Layer\)

<table id="table_abh_xx5_zdc"><thead><tr><th>

CIs

</th><th>

CI Relationships

</th></tr></thead><tbody><tr><td>

IP Switch CI

</td><td>

IP Switch Device is represented by the IP Switch CI.

 Table name: **cmdb\_ci\_ip\_switch**

 IP Switch CI contain Slots or Network Interfaces.

</td></tr><tr><td>

Slot CI

</td><td>

Slots are represented by the Slot CI.

 Table name: **cmdb\_ci\_container\_slot**

 Slot is contained by the IP Switch.

 Slot CI contains the Interface Card.

</td></tr><tr><td>

Subslot CI

</td><td>

Subslots are represented by the Subslot CI.

 Table name: **cmdb\_ci\_container\_subslot**

 Subslot is contained by Interface Card CI.

 Subslot CI contains the Interface Card CI.

</td></tr><tr><td>

Interface Card CI

</td><td>

Different types of cards are represented by the Interface Card CI.

 Fan and Power Supply Units are also represented by the Card CI.

 Table name: **cmdb\_ci\_interface\_card**

 Interface Cards are contained by Slots or Subslots.

 Interface Cards can contain Network Interface or Subslots.

</td></tr><tr><td>

Network Interface CI

</td><td>

Any type of Network Interface is represented by the Network Interface CI.

 Table name: **cmdb\_ci\_ni\_interface**

 Network Interface is contained by Interface Card, IP Switch.

</td></tr></tbody>
</table>