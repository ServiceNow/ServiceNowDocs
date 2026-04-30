---
title: Configure filter for audit
description: Define filtering conditions to control the scope of Telecom Discrepancy audits. These filters ensure that audits run only on the desired set of CIs, improving performance and targeting accuracy.
locale: en-US
release: zurich
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Activate Discrepancy and Reconciliation, Set up Telecom Visibility, Configure, Telecommunications Service Operations Management]
---

# Configure filter for audit

Define filtering conditions to control the scope of Telecom Discrepancy audits. These filters ensure that audits run only on the desired set of CIs, improving performance and targeting accuracy.

## Before you begin

Role required: admin

## About this task

Understanding Filtering Conditions in Telecom Discrepancy Audits

-   Audits use filtering conditions to narrow the scope of CIs being evaluated.
-   Filtering conditions are essential for narrowing down audit targets.
-   You can define and modify conditions per audit instance to meet specific audit requirements.
-   Filtering by `discovery_source` is a common condition to filter records associated with particular integration sources \(e.g., TSOM and Altiplano\). Additionally, you can customize the filter according to the audit requirements.
-   Each version of the audit can have a different filtering condition.

The following are the audit filters:

1.  Telecom Logical Connections Discrepancy Audit: This audit runs at the logical connection table. The default filter condition is defined as `discovery_source` like TSOM. This condition is applied on each CI in the logical connection table.
2.  Telecom Network Topology Discrepancy Audit: This audit runs at the network topology table. The default filter condition is defined as `discovery_source` like TSOM. This condition is applied on each CI in the network topology table.
3.  Telecom Discrepancy Audit: This audit runs at the relationships table. The default filter condition is defined as `discovery_source` like TSOM. This condition is applied on each CI at the equipment level.

The following screenshot helps to understand the user interface of the certification filter ![The user interface of TSOM certification and logical connection discrepancy audit filter](../images/certification-filter.png).

## Procedure

1.  Navigate to **All** &gt; **Certification** &gt; **Filters**.

2.  Select **New**.

    The certification filter interface appears.

3.  Fill in the fields.

    For more guidance, see [Create a filter](https://www.servicenow.com/docs/access?context=t_CreatingFilters&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

4.  Add the filter conditions.

    For example, Discovery source contains TSOM.

5.  Select **Submit**.

    The filter is created.


## Result

You can use the filter in the logical connection audit.

**Related topics**  


[Run Telecom Discrepancy audit](run-audits.md#)

[Example for Telecom Discrepancy Audit and Remediation](run-audits.md#)

[System components installed with Telecom Discrepancy Identification &amp; Reconciliation](../concept/system-properties-affecting-telecom-discrepancy-identification-reconciliation.md)

[Configure attribute value discrepancy in CMDB 360](configure-attribute-value-discrepancy-in-cmdb-360.md)

[Control CI attribute updates using Reconciliation rules](control-ci-attribute-updates-using-reconciliation-rules.md)

