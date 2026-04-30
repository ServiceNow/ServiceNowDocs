---
title: Properties related to remediation of duplicate CIs
description: Use de-duplication properties to configure how remediation of duplicate CIs works when using the Duplicate CI Remediator or the De-duplication dashboard in CMDB Workspace and in Service Graph Workspace.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Duplicate CIs remediation, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Properties related to remediation of duplicate CIs

Use de-duplication properties to configure how remediation of duplicate CIs works when using the Duplicate CI Remediatoror the De-duplication dashboard in CMDB Workspaceand in Service Graph Workspace.

To view and edit these properties, the admin role is required.

Although the properties below reference the [Duplicate CI Remediator](../task/reconcile-dup-task.md), these properties have an equivalent effect in [duplicate CI remediation in CMDB Workspace](../concept/dedup-ci-exp-cmdb-workspace.md).

<table id="table_thf_j3w_5gb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attributes in which **max\_length** exceeds this property value \(4000 by default\) are excluded from the **Select Main CI**, **Merge Attribute Values**, and **Determine Duplicate CI Actions** tabs in the Duplicate CI Remediator wizard.

 glide.duplicate\_ci\_remediator.max.field\_length

</td><td>

If the **max\_length** for an attribute is equal to the property value, and the size of the data exceeds the property value, then the data is truncated to the property value and the attribute appears in attribute lists.-   Type: integer
-   Default value: 4000
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Duplicate CI Remediator Properties**

 **Note:** This property impacts the performance of de-duplication tasks, therefore be cautious about setting this value.

</td></tr><tr><td>

Comma separated list of related tables in the format '&lt;table&gt;.&lt;reference column&gt;', that are excluded from merging during duplicate CI remediation.

 glide.duplicate\_ci\_remediator.related\_items\_blacklist

</td><td>

-   Type: string
-   Default value: cert\_task.cmdb\_ci,cert\_audit\_result.configuration\_item,discovery\_log.cmdb\_ci,alm\_hardware.ci,alm\_asset.ci,fm\_expense\_line.ci
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Duplicate CI Remediator Properties**

</td></tr><tr><td>

Threshold for the number of duplicate CIs, which if exceeded, support for reconciliation in the Duplicate CI Remediator is limited \(1,000 by default\).

 glide.duplicate\_ci\_remediator.max.cis

</td><td>

-   Type: integer
-   Default value: 1000
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Duplicate CI Remediator Properties**
-   Learn more: See 'Large number of duplicate CIs' in [Remediate a de-duplication task \(manual\)](../task/reconcile-dup-task.md).

This threshold never exceeds 5,000, even if you set the property to a value greater than 5,000.

</td></tr><tr><td>

Determines whether the Duplicate CI Remediator actually remediates CI duplication by updating records in the CMDB, or not.

 glide.duplicate\_ci\_remediator.dry\_run

</td><td>

When set to false \(default value\), updates specified in the wizard are actually performed.

 You can set this property to true and then test run through the Duplicate CI Remediator without any records actually being updated. In this case, the work notes for the task describe the changes that will happen in an actual remediation.

 -   Type: true \| false
-   Default value: false
-   Location: **Configuration** &gt; **CMDB Properties** &gt; **Duplicate CI Remediator Properties**

</td></tr><tr><td>

glide.duplicate\_ci\_remediator.enable\_restricted\_mode

</td><td>

Enables restricted mode remediation in the Duplicate CI Remediator. This option restricts the use of related items in de-duplication remediation and allows a blocked remediation to proceed using the **Use the Duplicate CI Remediator \(Restricted Mode\)** option. For more information, see [Using restricted mode within the Duplicate CI Remediator \[KB1542272\]](https://support.servicenow.com/kb_view_customer.do?sysparm_article=KB1542272).

 -   Type: true \| false
-   Default value: false
-   Location: [Add to System Properties \[sys\_properties\]](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)
-   Learn more: [Remediate a de-duplication task \(manual\)](../task/reconcile-dup-task.md)

 Set to **true** to enable restricted mode remediation.

</td></tr></tbody>
</table>**Parent Topic:**[Duplicate CIs remediation](../concept/de-duplication-tasks.md)

