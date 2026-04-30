---
title: Exception management workflow versus flow designer in Configuration Compliance
description: Starting with Configuration Compliance \(CC\) v13.0, if you are deploying CC for the first time, the flow designer for approving exception requests in exception management is enabled by default. If you are an existing CC user, the default option is workflow.
locale: en-US
release: xanadu
product: Configuration Compliance
classification: configuration-compliance
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure approval rules for Exception Management in Configuration Compliance, Setting up, installing, and configuring the Configuration Compliance application, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Exception management workflow versus flow designer in Configuration Compliance

Starting with Configuration Compliance \(CC\) v13.0, if you are deploying CC for the first time, the flow designer for approving exception requests in exception management is enabled by default. If you are an existing CC user, the default option is workflow.

<table id="table_qmm_sbw_sqb"><thead><tr><th>

Considerations

</th><th>

Workflow

</th><th>

Flow designer

</th></tr></thead><tbody><tr><td>

Version

</td><td>

Prior to v13.0 of CC.

</td><td>

Starting from v13.0 of CC.

</td></tr><tr><td>

Default option

</td><td>

Default option if you are an existing CC user.

</td><td>

Default option for new CC users starting from v13.0.

</td></tr><tr><td>

Setting the approval process

</td><td>

Exception management includes exception requests along with exception rules.

</td><td>

Includes defining various levels and adding different approvers for different use cases. Easier to implement than the workflow. Exception management includes exception requests along with exception rules.

</td></tr><tr><td>

Upgrading to flow designer

</td><td>

You can upgrade to flow designer from workflow. However, existing requests can only be approved using the workflow.

</td><td>

Flow designer is enabled by default.

</td></tr><tr><td>

System property **sn\_vulc.flow\_designer\_activation**

</td><td>

If you have been using the workflow for exception management prior to v13.0, the system property is set to false. To activate the flow designer, set this property to true.**Note:** You cannot revert to using the workflow after activating the flow designer.

</td><td>

If you are using CC for the first time for v13.0 or later, the system property value is set to true by default.

</td></tr><tr><td>

Approval rules module

</td><td>

After setting the system property to true, the **Enable module approval rules** scheduled job runs within 24 hours. This scheduled job enables the **Approval rules** module. To activate this module instantly, run this job manually.

</td><td>

If you have deployed CC for the first time from CC v13.0, this module is available by default.

</td></tr><tr><td>

Approval levels

</td><td>

Provides the option to set only two levels of approvers.

</td><td>

Provides multiple options such as setting any number of configurations, approver levels, and dynamically adding approvers for each rule.

</td></tr></tbody>
</table>**Parent Topic:**[Configure approval rules for Exception Management in Configuration Compliance](../task/cc-exception-mgt-approval-rules.md)

