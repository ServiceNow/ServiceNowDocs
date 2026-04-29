---
title: Configure a risk assessment methodology
description: Configure a risk assessment methodology \(RAM\) in the Advanced Risk application so that you can assess the risks or objects in your organization.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Perform Advanced Risk Assessment, Use, Risk Management, Governance, Risk, and Compliance]
---

# Configure a risk assessment methodology

Configure a risk assessment methodology \(RAM\) in the Advanced Risk application so that you can assess the risks or objects in your organization.

## Before you begin

Role required: sn\_risk\_advanced.ara\_admin

## About this task

A RAM is a configuration or record in the new risk assessment engine in the Advanced Risk application.

You can use a RAM to assess either the risks or objects in your organization. For example, you can configure a RAM to specify the types of risk assessments and the entities on which a risk assessment is performed. By using a RAM, your organization can have different methodologies for assessing risks.

After you move a RAM to the **Retired** state, you can also move it back to the **Draft** state if you want to make some changes later. You can only move a RAM to the **Draft** state if it doesn’t have any assessments in the **Monitor** state or the **Closed** state. When you move a RAM back to the **Draft**, the on-going assessments and the associated scopes are deleted.

## Procedure

1.  Navigate to **All** &gt; **Advanced Risk Assessment** &gt; **Administration** &gt; **Risk Assessment Methodologies**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For a description of the field values on the risk assessment methodology form, see [Risk Assessment Methodology form](../reference/risk-assessment-methodology-form.md).

4.  Right-click and save the form.

5.  To configure the various assessments, select one of the following options.

    |Choice|Related link|
    |------|------------|
    |**Configure inherent assessment**|See [Configure an inherent assessment](configure-inherent-assessment.md).|
    |**Configure control effectiveness**|See [Configure a control effectiveness assessment](configure-control-assess.md)|
    |**Configure residual assessment**|See [Configure a residual assessment](configure-residual-assessment.md)|
    |**Configure target assessment**|See [Configure a target assessment](configure-target-assessment.md)|

6.  Select **Publish**.

    **Note:** After a new assessment is created on the same risk and the assessment is in the **Monitor** state, the other assessments automatically move to the **Completed** state. When an assessment instance is in the **Monitor** state, you can’t move the RAM back to the **Draft** state. A RAM can only be moved back to the **Draft** state if there are no assessment instances.


-   **[Risk Assessment Methodology form](../reference/risk-assessment-methodology-form.md)**  
Use the Risk Assessment Methodology form in the Advanced Risk application to specify the types of risk assessments and the entities on which the risk assessment is performed.

**Parent Topic:**[Perform Advanced Risk Assessment](../concept/use-advanced-risk-assessment.md)

