---
title: Telecom Router Pattern
description: The ServiceNow Telecom Discovery application uses the Telecom Router discovery pattern to find SNMP-based routers in the network. Discovering some of these resources requires updating the Telecommunications Discovery Patterns \(TSOM Patterns\) from the ServiceNow Store.To access a full list of OIDs that will be classified.
locale: en-US
release: yokohama
product: Telecom Visibility
classification: telecom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Telecom Discovery using Telecommunications Discovery Patterns, Exploring Telecom Discovery, Telecom Discovery, TSOM Visibility, Telecommunications Service Operations Management]
---

# Telecom Router Pattern

The ServiceNow® Telecom Discovery application uses the Telecom Router discovery pattern to find SNMP-based routers in the network. Discovering some of these resources requires updating the Telecommunications Discovery Patterns \(TSOM Patterns\) from the ServiceNow Store.

Telecom Discovery uses the Telecommunications Discovery Patterns to run Horizontal Discovery. This Telecommunications Discovery Pattern uses a set of SNMP requests to find, classify, and discover network elements.

Telecom Router pattern is part of the Telecommunications Discovery Patterns application \(sn\_tsom\_patterns\), which is part of TSOM Visibility.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Subscription to TSOM.
-   Confirm that your network router devices have SNMP access.
-   On the ServiceNow instance, configure SNMP credentials. For more information, see [SNMP support for Discovery](https://www.servicenow.com/docs/access?context=c_SNMPSupportForDiscovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).
-   For setting up TSOM Patterns, see [Configure Telecommunications Discovery \(TSOM\) Patterns](configuring-telecommunications-discovery-patterns.md#).

## Impacted CMDB CIs and CI Relationships \(Physical Layer\)

<table id="table_p2q_zmk_zdc"><thead><tr><th>

CIs

</th><th>

CI Relationships

</th></tr></thead><tbody><tr><td>

IP Router CI

</td><td>

IP Router Device is represented by the IP Router CI.

 Table name: **cmdb\_ci\_ip\_router**

 IP Router CI contains Slots or Network Interfaces.

</td></tr><tr><td>

Slot CI

</td><td>

Slots are represented by the Slot CI.

 Table name: **cmdb\_ci\_container\_slot**

 Slot is contained by the IP Router.

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

 Network Interface is contained by Interface Card, IP Router.

</td></tr></tbody>
</table>**Parent Topic:**[Telecom Discovery using Telecommunications Discovery Patterns](telecom-discovery-using-telecommunication-discovery-pattern.md)

## Classifying xNFs for this Pattern

To access a full list of OIDs that will be classified.

### Before you begin

Role required: admin

Classifier name: **Standard Network Router**.

### Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **CI Classification** &gt; **SNMP**.

2.  From the list, select **Standard Network Router**.

3.  Open the tab **SNMP OID Classifications** and see the list of OIDs.![snmp-classification.](../images/telecom-router-pattern-classification.png)

    **Note:**

    For more information on how to add additional OIDs to the classifier, see [Telecom Discovery using Telecommunications Discovery Patterns](telecom-discovery-using-telecommunication-discovery-pattern.md).

    MiB Tables Used on an xNF:

    -   SystemMIB
    -   EntityPhysicalMIB
    -   IfMIB
    -   IfXMIB
    -   IpMIB

