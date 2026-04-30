---
title: Create a Risk Assessment Methodology
description: Configure a risk assessment methodology \(RAM\) in the Privacy Management application so that you can assess the risks in your organization.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Create a Risk Assessment Methodology

Configure a risk assessment methodology \(RAM\) in the Privacy Management application so that you can assess the risks in your organization.

## Before you begin

Role required: sn\_privacy.manager or sn\_privacy.admin

## About this task

Create a standardized method to support risk-based decision-making across departments, projects, and systems. By using a RAM, your organization can have different methodologies for assessing risks.

After you move a RAM to the **Retired** state, you can also move it back to the **Draft** state if you want to make some changes later. You can only move a RAM to the **Draft** state if it doesn’t have any assessments in the **Monitor** state or the **Closed** state. When you move a RAM back to the **Draft**, the on-going assessments and the associated scopes are deleted.

## Procedure

1.  Navigate to **All** &gt; **Privacy Management** &gt; **Risk Assessments** &gt; **Risk assessment methodologies**.

2.  On the Risk Assessment Methodology page, select **New**.

3.  On the form, fill the details.

    For a description of the field values on the risk assessment methodology form, see [Risk Assessment Methodology form](../../grc-risk/reference/risk-assessment-methodology-form.md).

4.  Right-click and save the form.

5.  To configure the various assessments, select one of the following options.

    |Choice|Related link|
    |------|------------|
    |**Configure inherent assessment**|See [Configure an inherent assessment](../../grc-risk/task/configure-inherent-assessment.md).|
    |**Configure control effectiveness**|See [Configure a control effectiveness assessment](../../grc-risk/task/configure-control-assess.md)|
    |**Configure residual assessment**|See [Configure a residual assessment](../../grc-risk/task/configure-residual-assessment.md)|
    |**Configure target assessment**|See [Configure a target assessment](../../grc-risk/task/configure-target-assessment.md)|

6.  Select **Publish**.

    **Note:** After a new assessment is created on the same risk and the assessment is in the **Monitor** state, the other assessments automatically move to the **Completed** state. When an assessment instance is in the **Monitor** state, you can’t move the RAM back to the **Draft** state. A RAM can only be moved back to the **Draft** state if there are no assessment instances.


## Result

A new Risk Assessment Methodology is created and is available for use.

-   **[Risk assessment methodology form](../reference/risk-assessment-methodology-form-prm.md)**  
Use the Risk Assessment Methodology form in the Core UI to create a risk assessment methodology \(RAM\).

**Parent Topic:**[Using Privacy Management](../concept/using-privacy-mgmt.md)

