---
title: Classify xNFs for Telecom Juniper MX SSH Router Pattern
description: To access a full list of OIDs that will be classified.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use Telecom Discovery patterns, Use, Telecommunications Service Operations Management]
---

# Classify xNFs for Telecom Juniper MX SSH Router Pattern

To access a full list of OIDs that will be classified.

## Before you begin

Role required: admin

Classifier name: **Standard Network Router**.

## Procedure

1.  Navigate to **All** &gt; **Discovery Definition** &gt; **CI Classification** &gt; **SNMP**.

2.  From the list, select **Standard Network Router**.

3.  Open the tab **SNMP OID Classifications** and see the list of OIDs.

    **Note:**

    For more information on how to add additional OIDs to the classifier, see [Direct Discovery using Discovery Patterns](../concept/telecom-discovery-using-telecommunication-discovery-pattern.md).

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

**Parent Topic:**[Use Telecom Discovery patterns](../concept/using-telecom-discovery-patterns.md)

