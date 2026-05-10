---
title: Telecom Discrepancy Identification and Reconciliation
description: Use the Telecom Discrepancy Identification and Reconciliation capability to keep your CMDB or Telecommunications Network Inventory \(TNI\) in sync with your live telecom network. By continuously auditing and comparing discovered data with inventory records, this solution helps you detect, classify, and automatically remediate inconsistencies before they impact service quality, assurance, or fulfillment processes.
locale: en-US
release: australia
product: Telecommunications Service Operations Management
classification: telecommunications-service-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Telecom Visibility, Explore, Telecommunications Service Operations Management]
---

# Telecom Discrepancy Identification and Reconciliation

Use the Telecom Discrepancy Identification and Reconciliation capability to keep your CMDB or Telecommunications Network Inventory \(TNI\) in sync with your live telecom network. By continuously auditing and comparing discovered data with inventory records, this solution helps you detect, classify, and automatically remediate inconsistencies before they impact service quality, assurance, or fulfillment processes.

Telecom Discrepancy Identification and Reconciliation is a telecom-specific capability included with the TSOM Visibility plugin. It helps confirm the integrity of your network inventory by identifying mismatches between real-time network data \(from Discovery or external systems\) and inventory records stored in the CMDB or TNI.

This solution uses:

-   CMDB Compliance Certification audits to detect anomalies.
-   Follow-on tasks to log and track issues.
-   Automated remediation subflows to resolve discrepancies.

**Note:** Keeping inventory accurate enables automation, reduces service errors, and supports regulatory compliance. It is also a foundational component of TM Forum’s Autonomous Network Operations \(ANO\) framework.

## Telecom Discrepancy Identification &amp; Reconciliation architecture

## Key features

|Feature|Description|
|-------|-----------|
|Continuous audit checks|Compares discovered network data with inventory records using Certification Audits.|
|Discrepancy detection|Identifies CIs that are missing, misconfigured, or misaligned in terms of hierarchy or attribute values.|
|Follow-On task generation|Automatically creates tasks for each discrepancy to enable tracking and remediation.|
|Automated remediation|Uses Flow Designer subflows to resolve issues such as outdated CIs, invalid relationships, and missing discovery data.|

## How Telecom Discrepancy Identification &amp; Reconciliation works

Once the discovery process is complete, the CMDB Compliance framework identifies mismatches between discovered data and inventory records using scheduled or on-demand compliance audits.

-   Compliance Audits: Compare discovered network data with CMDB inventory records to detect inconsistencies.
-   Follow-On Tasks: Automatically generated for each failed audit. These tasks document and categorize the identified discrepancies.
-   Remediation Subflows: Launched from Follow-On Tasks to resolve discrepancies by updating, decommissioning, or realigning Configuration Items \(CIs\).

**Note:** For more information, see [Discrepancy identification – types of discrepancies](discrepancy-identification-types-of-discrepancies.md).

## CMDB Compliance and Telecom Discrepancy Identification &amp; Reconciliation

CMDB Compliance is a toolset that enables administrators to certify CMDB data for accuracy and identify discrepancies detected during compliance audits. It can also automatically generate and assign Follow-on Tasks for failed audit records, which serve as tasks to trigger an appropriate remediation subflow to correct discrepancies. CMDB Compliance Audits form the foundation of our Telecom Discrepancy Identification &amp; Reconciliation.

-   CMDB Compliance runs audits as a post-processing rule, identifying anomalies \(discrepancies\) in the CMDB.
-   CMDB Compliance creates a Follow-On Task for each Audit Record in a failed state \(the failed state is the result of an audit finding an anomaly or discrepancy in the CMDB\). A remediation flow can be designed and triggered for each Follow-On Task to address and resolve the discrepancy.

The logic for Telecom Discrepancy Identification &amp; Reconciliation, as well as the example remediation subflows, are automatically with the TSOM Visibility plugin. For more information on the general CMDB Compliance toolset, see [CMDB Compliance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_Compliance.md).

## Discrepancy Identification Scenarios \(using Compliance Audits\)

Discrepancy identification in TSOM Visibility relies on using CMDB Compliance \(Certification Audits\) and has extended it by adding specific logic that uses model relationships and information to identify mismatches. To support remediation, the system generates specific reconciliation task types for each issue found, such as:

-   Slots occupied discrepancy
-   Most recent discovery date not set
-   Most recent discovery date not within configured threshold
-   Model relationships not defined
-   CI model not found
-   Incorrect number of relationships
-   Reference to Logical Interface not found

You can use the following audits to identify the discrepancies in the discovered physical and logical entities

-   Telecom Discrepancy Audit
-   Telecom Logical Connections Discrepancy Audit
-   Telecom Network Topology Discrepancy Audit

**Note:** For more information on the general compliance audits, see [Certification audits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/c_CertificationAudits.md).

## Automation and UI Integration

-   Every failed audit automatically creates a Follow-On Task.
-   Tasks can trigger prebuilt or custom subflows using Flow Designer.
-   Manual remediation can be initiated using a "Remediate" UI action button in the task form.
-   Remediation steps are recorded in work notes for visibility and auditing.

**Note:** For more information on how to build a subflow, see [Building subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/subflows.md).

## Follow-On Task types created for failed Audit Result Records

The following discrepancy types \(Audit Results\) can be found for Parent CI and child CIs for each relationship record in the CI Relationship table \(cmdb\_rel\_ci\) that matches the conditions, and the following Follow-On Tasks can be created for each of the failed Audit Results:

1.  The most recent discovery date not set- generated in case the Most recent discovery date field in CI is missing.
2.  The most recent discovery date not within configured threshold- generated in case the difference in the Most recent discovery date field value between a Parent CI and child CI is more than 2.5 days. For example, By default, it is set to 2.5 days in the sn\_tsom\_core.discovered\_date.diff.threshold.in.days system property and can be changed.
3.  CI model not found–\(the ‘Model ID’ field isn’t set or data is invalid\). Generated in case a corresponding CI model isn’t found. If a CI model isn’t found, the next validations \(4-6\) are irrelevant because they rely on CI models. In case a CI model is found, the audit will continue to the next validations \(4-6\).
4.  Slots occupied discrepancy-Generated in case a card occupies an incorrect number of Slots.
5.  Model relationships not defined-relevant only if TNI is installed. Generated if the audit is unable to find a relationship between Parent and child CI models in the Network Model Relationships table.
6.  Incorrect number of relationships - relevant only if TNI is installed. Generated if the audit finds that the number of discovered child CI records exceeds the maximum number of its corresponding Parent CI record in the model relationship Count field in the Network Model Relationship table.
7.  Incorrect number of relationships - generated during the Logical Connection Discrepancy Audit when a logical interface is associated with more than one logical connection, violating the expected one-to-one mapping.
8.  Incorrect number of relationships - generated during the Network Topology Discrepancy Audit when a network topology record does not meet the required relationship criteria. Specifically:
    -   The record must have at least one "Contains:Contained By" relationship with an equipment CI.
    -   The record must also have at least one "Members:Member Of" relationship with a logical connection CI.
9.  Reference to Logical Interface not found - generated during the Logical Connection Discrepancy Audit when a logical connection is missing one of the end points \(Port A or Port z, or both\).

## Telecom Reconciliation

Automate reconciliation of network inventory discrepancies and enhance operational efficiency. Telecom Reconciliation helps to:

-   Identify and resolve discrepancies between live network inventory and CMDB inventory to ensure alignment and boost productivity​
-   Empower users with auto generated discrepancy reports detailing the type of discrepancy​
-   Provide users with recommended corrective actions and the flexibility and control to choose between manual or automated methods to resolve discrepancies ​
-   Improve operations by automatically aligning the operational status of network resources with the same status in the inventory CMDB​

**Related topics**  


[Discrepancy identification – types of discrepancies](discrepancy-identification-types-of-discrepancies.md)

[Activate Telecom Discrepancy Identification and Reconciliation](../task/configure-telecom-reconciliation.md)

[Run Telecom Discrepancy audit](../task/run-audits.md#)

[System components installed with Telecom Discrepancy Identification &amp; Reconciliation](system-properties-affecting-telecom-discrepancy-identification-reconciliation.md)

