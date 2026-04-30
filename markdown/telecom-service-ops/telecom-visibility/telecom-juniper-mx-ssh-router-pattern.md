---
title: Telecom Juniper MX SSH Router Pattern
description: The ServiceNow Telecom Discovery application uses the Telecom Juniper MX SSHRouter discovery pattern to find SNMP and CLI -based Juniper MX Series routers in the network. Discovering some of these resources requires updating the Telecommunications Discovery Patterns \(TSOM Patterns\) from the ServiceNow store.To access a full list of OIDs that will be classified.
locale: en-US
release: yokohama
product: Telecom Visibility
classification: telecom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Telecom Discovery using Telecommunications Discovery Patterns, Exploring Telecom Discovery, Telecom Discovery, TSOM Visibility, Telecommunications Service Operations Management]
---

# Telecom Juniper MX SSH Router Pattern

The ServiceNow® Telecom Discovery application uses the Telecom Juniper MX SSHRouter discovery pattern to find SNMP and CLI -based Juniper MX Series routers in the network. Discovering some of these resources requires updating the Telecommunications Discovery Patterns \(TSOM Patterns\) from the ServiceNow® store.

Telecom Discovery uses the Telecommunications Discovery Patterns to run Horizontal Discovery. This Telecommunications Discovery Pattern uses a set of SNMP requests to find and classify CLI over SSH to discover network elements.

Telecom Juniper MX SSH Router pattern is part of the Telecommunications Discovery Patterns application \(sn\_tsom\_patterns\), which is part of TSOM Visibility.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   Subscription to TSOM.
-   Verify that your network router devices have SNMP access.
-   On the ServiceNow instance, configure SNMP credentials. For more information, see [SNMP support for Discovery](https://www.servicenow.com/docs/access?context=c_SNMPSupportForDiscovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).
-   For setting up TSOM Patterns, see [Configure Telecommunications Discovery \(TSOM\) Patterns](configuring-telecommunications-discovery-patterns.md#).

## Impacted CMDB CIs and CI Relationships \(Physical Layer\)

<table id="table_bhm_kxn_zdc"><thead><tr><th>

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

3.  Open the tab **SNMP OID Classifications** and see the list of OIDs.![snmp oid classifications.](../images/telecom-juniper-classification.png)

    **Note:**

    For more information on how to add additional OIDs to the classifier, see [Telecom Discovery using Telecommunications Discovery Patterns](telecom-discovery-using-telecommunication-discovery-pattern.md).

    The List of Specific OIDs to call this Pattern:

<table id="table_cfq_qmf_b2c"><tbody><tr><td>

**Vendor**

</td><td>

**Model**

</td><td>

**OID**

</td><td>

**Pattern**

</td></tr><tr><td>

Juniper

</td><td>

MX80

</td><td>

1.3.6.1.4.1.2636.1.1.1.2.57

</td><td>

Telecom Juniper MX SSH Router

</td></tr><tr><td>

Juniper

</td><td>

MX104

</td><td>

1.3.6.1.4.1.2636.1.1.1.2.97

</td><td>

Telecom Juniper MX SSH Router

</td></tr><tr><td>

Juniper

</td><td>

MX240

</td><td>

1.3.6.1.4.1.2636.1.1.1.2.29

</td><td>

Telecom Juniper MX SSH Router

</td></tr><tr><td>

Juniper

</td><td>

MX480

</td><td>

1.3.6.1.4.1.2636.1.1.1.2.25

</td><td>

Telecom Juniper MX SSH Router

</td></tr></tbody>
</table>    MiB Tables Used on an xNF: SystemMIB.

    CLI Commands Used.

    -   show chassis hardware \| no-more \| display xml
    -   show interface media \| no-more \| display xml

