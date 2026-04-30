---
title: Exploring Telecom Discrepancy Identification and Reconciliation
description: Telecom Discrepancy Identification &amp; Reconciliation solution is designed to confirm the accuracy and consistency of network resource data between network systems and inventory management databases, such as CMDB/TNI.These system properties are part of the TSOM Visibility plugin \(sn\_tsom\_core\) and control the Telecom Discrepancy Identification &amp; Reconciliation log \(TSOM CMDB Audit\). The TSOM Visibility plugin serves as an enabler for the TSOM Visibility applications, containing logic that is shared across the Telecom Discovery and Telecom Discrepancy Identification &amp; Reconciliation solution.
locale: en-US
release: yokohama
product: Telecom Visibility
classification: telecom-visibility
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Telecom Discrepancy Identification and Reconciliation, TSOM Visibility, Telecommunications Service Operations Management]
---

# Exploring Telecom Discrepancy Identification and Reconciliation

Telecom Discrepancy Identification &amp; Reconciliation solution is designed to confirm the accuracy and consistency of network resource data between network systems and inventory management databases, such as CMDB/TNI.

Telecom Discrepancy Identification &amp; Reconciliation relies on Telecom Discovery and platform capabilities to perform its functions.

## Telecom Discrepancy Identification &amp; Reconciliation Overview

![telecom discrepancy identification and reconciliation framework.](../images/telecom-discrepancy-identification-reconciliation.png)

## TSOM Visibility plugin

The Telecom Discrepancy Identification &amp; Reconciliation logic is a component of the TSOM Visibility plugin \(sn\_tsom\_core\). This plugin encompasses shared logic essential for both Telecom Discovery and Telecom Discrepancy Identification &amp; Reconciliation processes. It includes telecom-specific discrepancy detection and remediation capabilities, along with other foundational logic designed to support current and future telecom application functionalities.

## Identification &amp; Reconciliation Engine \(IRE\)

IRE offers a centralized framework for identifying and reconciling data from multiple sources. It confirms the integrity of the CMDB and some non-CMDB tables when various data sources are used to create or update CI records.

-   IRE matches existing CIs based on Identification Rules.
-   IRE creates CIs if no match is found.
-   IRE updates are attributed based on the Reconciliation Rules.

For more information, see [CMDB Identification and Reconciliation \(IRE\)](https://www.servicenow.com/docs/access?context=c_CMDBIdentifyandReconcile&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## CMDB Compliance and Telecom Discrepancy Identification &amp; Reconciliation

CMDB Compliance is a toolset that enables administrators to certify CMDB data for accuracy and identify discrepancies detected during compliance audits. It can also automatically generate and assign Follow-on Tasks for failed audit records, which serve as tasks to trigger an appropriate remediation subflow to correct discrepancies. CMDB Compliance Audits form the foundation of our Telecom Discrepancy Identification &amp; Reconciliation.

-   CMDB Compliance runs audits as a post-processing rule, identifying anomalies \(discrepancies\) in the CMDB.
-   CMDB Compliance creates a Follow-On Task for each Audit Record in a failed state \(the failed state is the result of an audit finding an anomaly or discrepancy in the CMDB\). A remediation flow can be designed and triggered for each Follow-On Task to address and resolve the discrepancy.

The logic for Telecom Discrepancy Identification &amp; Reconciliation, as well as the example remediation subflows, are included in the Yokohama release and will be installed automatically with the TSOM Visibility plugin.

For more information on the general CMDB Compliance toolset, see [CMDB Compliance](https://www.servicenow.com/docs/access?context=c_Compliance&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Discrepancy Identification Scenarios \(using Certification Audits\)

There are two key discrepancy categories that can be detected between Inventory \(CMDB\) and Discovery that are described below:

-   Entities that exist in the Inventory but don’t exist in the Network.
-   Entities that exist both in the network and in the inventory but differ in their hierarchy.

Discrepancy identification in TSOM Visibility relies on using CMDB Compliance \(Certification Audits\) and has extended it by adding specific logic that uses model relationships and information to identify mismatches.

**Note:** The current release focuses on the identification and reconciliation of discrepancies at the physical resource layer. In the upcoming release, this functionality is extended to include support for the logical resource layer and attributes as well.

For more information on the general Certifications Audits feature, see [Certification audits](https://www.servicenow.com/docs/access?context=c_CertificationAudits&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

## Follow-On Task types created for failed Audit Result Records

The following discrepancy types \(Audit Results\) can be found for Parent CI and child CIs for each relationship record in the CI Relationship table \(cmdb\_rel\_ci\) that matches the conditions, and the following Follow-On Tasks can be created for each of the failed Audit Results:

1.  The most recent discovery date not set- generated in case the Most recent discovery date field in CI is missing.
2.  The most recent discovery date not within configured threshold- generated in case the difference in the Most recent discovery date field value between a Parent CI and child CI is more than 2.5 days.

    By default, it is set to 2.5 days in the sn\_tsom\_core.discovered\_date.diff.threshold.in.days system property and can be changed.

3.  CI model not found–\(the ‘Model ID’ field isn’t set or data is invalid\). Generated in case a corresponding CI model isn’t found. If a CI model isn’t found, the next validations \(4-6\) are irrelevant because they rely on CI models. In case a CI model is found, the audit will continue to the next validations \(4-6\).
4.  Slots occupied discrepancy-Generated in case a Card occupies an incorrect number of Slots.
5.  Model relationships not defined-relevant only if TNI is installed. Generated if the audit is unable to find a relationship between Parent and child CI models in the Network Model Relationships table.
6.  Incorrect number of relationships - relevant only if TNI is installed. Generated if the audit finds that the number of discovered child CI records exceeds the maximum number of its corresponding Parent CI record in the model relationship **Count** field in the Network Model Relationship table.

For more information on the general Follow-on Tasks feature, see Building Subflows.

## Discrepancy Remediation Subflows

Once an audit identifies a discrepancy, it’s logged as a Follow-on Task. The system enables users to define a subflow for specific discrepancy scenarios, enabling them to distinguish between various types of discrepancies and create custom flows to remediate them.

For more information on how to build a subflow, see [Building subflows](https://www.servicenow.com/docs/access?context=subflows&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

## Usage Example

The following is an example of a specific scenario on how you can use Telecom Discrepancy Identification &amp; Reconciliation:

Assume that a piece of equipment was initially discovered with a card \(Card40\) in its slot \(Slot40\). Over time, an issue was identified with Card40, and it was replaced by Card41. The inventory \(CMDB\), however, still contains a Card40 CI, while on the network, it has been replaced by Card41. When the next discovery job is executed, the Card41 CI will be discovered and added to the CMDB in the same slot \(Slot40\). As a result, we have two CIs \(the old one—Card40—and the newly discovered one—Card41\) placed in the same Slot40.

Audit identifies this discrepancy, create a Follow-on task, and enable a user to Remediate. \(resolve this discrepancy and decommission Card40\).

When the Service Operation CMDB Compliance Audit runs, it identifies this discrepancy and create an Audit Record in ‘failed’ state \(in our example AUDR0001283\).

1.  Navigate **All** &gt; **Compliance** &gt; **Audits** &gt; **.**
2.  Select **Service Operation CMDB Compliance Audit**.

3.  Select the **Run Audits** to run the audit.

    A Follow-on Task is automatically created for each failed audit record \(in our example, TASK0020215\).

    ![run audit.](../images/telecom-run-audits.png)

4.  Select **TASK0020215**.![follow-on task.](../images/telecom-follow-on-task.png)

    The Follow-On Task contains a detailed description of the discrepancy. As you can see in the description, the Card40 CI is in discrepancy.

    **Note:** This is an example of the TASK0020215 description created for the "Incorrect number of relationships" scenario. Other scenarios and environments might have different descriptions.

    Card40 was last discovered more than 2.5 days ago.

    Relationships between the following CIs:

    |CI|Model|
    |---|-----|
    |Slot40 \(8b2beb4247ceda10f04f83ac416d4398\)|DEMO 20532Tree \(1ba577524c1b3110f8772646dabeb9bb\)|
    |Card40 \(0b2beb4247ceda10f04f83ac416d4399\)|Nokia 7360 FANT-F CARD MODULE \(3af9617de5928110f877657a333391e0\)|
    |Card41 \(832beb4247ceda10f04f83ac416d439a\)| |

5.  Select the **Remediate** button to remediate.

6.  Remark: Remediate is a UI action which can be accessed in the following way:
7.  **All** &gt; **System Definition** &gt; **UI Actions**.
8.  Open the **Remediate** UI action to observe.![UI actions.](../images/telecom-ui-actions.png)

    For more information on UI actions, see [Defining UI actions](https://www.servicenow.com/docs/access?context=c_UIActions&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).


For this example, the Remediate UI action \(triggered by the **Remediate**\) calls the Execute TSOM CI Decommission subflow to address and resolve the discrepancy specified in the Follow-On Task TASK0020215. Additionally, we must decommission an old Card40, which will be executed automatically by calling the subflow ‘TSOM Decommission Card’.

Once the remediation is successfully completed, work notes are generated with the remediation results in the Follow-On Task window \(TASK0020215\).

As you can see in the work notes, we successfully retired Card40 and removed the relationship of Slot40 → Slot40. The discrepancy has been successfully resolved, and the CMDB CI records are now synchronized with the network state.

![example subflow.](../images/telecom-subflow.png)

This example subflow is shipped with the solution. Users can define custom remediation subflows using Flow Designer.

**Parent Topic:**[Telecom Discrepancy Identification and Reconciliation](telecom-reconciliation.md)

## System Properties Affecting Telecom Discrepancy Identification &amp; Reconciliation

These system properties are part of the TSOM Visibility plugin \(sn\_tsom\_core\) and control the Telecom Discrepancy Identification &amp; Reconciliation log \(TSOM CMDB Audit\). The TSOM Visibility plugin serves as an enabler for the TSOM Visibility applications, containing logic that is shared across the Telecom Discovery and Telecom Discrepancy Identification &amp; Reconciliation solution.

<table id="table_c1p_wmd_b2c"><thead><tr><th>

**Property Name**

</th><th>

**Recommended / Default Value**

</th><th>

**Description**

</th></tr></thead><tbody><tr><td>

**sn\_tsom\_core.audit.interface\_card\_tables**

</td><td>

cmdb\_ci\_interface\_card

</td><td>

If the value isn’t set \(that is, the field is empty\), the interface card tables won’t be processed in the TSOM CMDB Audit \(Telecom Discrepancy Identification &amp; Reconciliation\).

</td></tr><tr><td>

**sn\_tsom\_core.audit.discovery\_sources**

</td><td>

SG-Altiplano, ServiceNow

</td><td>

The TSOM CMDB Audit \(Telecom Discrepancy Identification &amp; Reconciliation\) only processes CI records with discovery source values of SG-Altiplano or ServiceNow \(Horizontal Discovery and Patterns\). Additional TSOM service graph connectors will be added in future releases.

</td></tr><tr><td>

**sn\_tsom\_core.audit.relationship\_types**

</td><td>

Contains:Contained by

</td><td>

TSOM CMDB Audit \(Telecom Discrepancy Identification &amp; Reconciliation\) only processes relationship records with the relationship type Contains::Contained by.

</td></tr><tr><td>

**sn\_tsom\_core.audit.slot\_tables**

</td><td>

cmdb\_ci\_container\_slot

</td><td>

If the value isn’t set \(that is, the field is empty\), the slot tables won’t be processed by the TSOM CMDB Audit \(Telecom Discrepancy Identification &amp; Reconciliation\).

</td></tr><tr><td>

**sn\_tsom\_core.audit.log.level**

</td><td>

info

</td><td>

The TSOM CMDB Audit \(Telecom Discrepancy Identification &amp; Reconciliation\) runs with the default log level set to **info**.

 Note: Changing the log level might impact performance.

</td></tr><tr><td>

**sn\_tsom\_core.audit.subslot\_tables**

</td><td>

cmdb\_ci\_container\_subslot

</td><td>

In case the value isn’t set \(that is, the field is empty\), the subslot tables won’t be processed by the TSOM CMDB Audit \(Telecom Discrepancy Identification &amp; Reconciliation\).

</td></tr><tr><td>

**sn\_tsom\_core.audit.interface\_tables**

</td><td>

cmdb\_ci\_ni\_interface

</td><td>

In case the value isn’t set \(that is, the field is empty\), the interface tables won’t be processed by the TSOM CMDB Audit \(Telecom Discrepancy Identification &amp; Reconciliation\).

</td></tr><tr><td>

**sn\_tsom\_core.audit.equipment\_tables**

</td><td>

-   cmdb\_ci\_ni\_telco\_equipmen t
-   cmdb\_ci\_ip\_switch
-   cmdb\_ci\_ip\_router

</td><td>

In case the value isn’t set \(that is, the field is empty\), the equipment tables won’t be processed by the TSOM CMDB Audit \(Telecom Discrepancy Identification &amp; Reconciliation\).

</td></tr><tr><td>

**sn\_tsom\_core.audit.discovered\_date.diff.threshold.in.days**

</td><td>

2.5

</td><td>

The TSOM CMDB Audit \(Telecom Discrepancy Identification &amp; Reconciliation\) only raises discrepancy tasks for CI records with the most recent discovery date values greater than the default threshold value.

</td></tr><tr><td>

**sn\_tsom\_core.audit.max\_number\_of\_records\_to\_process**

</td><td>

100000

</td><td>

The TSOM CMDB Audit \(Telecom Discrepancy Identification &amp; Reconciliation\) is set to process up to 100,000 relationship records.

 **Note:** This value can be increased, but it may impact performance.

</td></tr></tbody>
</table>### Configure Reconciliation

See [Configure Telecom Discrepancy Identification and Reconciliation](../task/configure-telecom-reconciliation.md#).

