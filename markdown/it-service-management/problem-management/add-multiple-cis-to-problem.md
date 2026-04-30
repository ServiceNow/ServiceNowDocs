---
title: Associate CIs with Problem
description: Associate multiple affected or impacted configuration items \(CIs\) to a problem to find out all the CIs that are affected by the same problem.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Managing Problems, Problem Management, IT Service Management]
---

# Associate CIs with Problem

Associate multiple affected or impacted configuration items \(CIs\) to a problem to find out all the CIs that are affected by the same problem.

## Before you begin

Role required: itil, sn\_problem\_write, admin, problem\_admin, problem\_coordinator or problem\_manager

## About this task

Use the **Configuration Item** field when there is a single, primary CI that is the cause of the problem and the **Affected CIs** or the **Impacted Services/CIs** related list when multiple CIs are affected by the problem.

## Procedure

1.  Navigate to **All** &gt; **Problem** &gt; **Open**.

2.  Open the problem record to which you want to associate CI items.

3.  Perform the following actions:

<table id="table_eh3_nlr_clb"><thead><tr><th>

Options

</th><th>

Procedures

</th></tr></thead><tbody><tr><td>

Configuration item

</td><td>

1.  Click the lookup icon \(![Lookup icon](../../itsm-workspace/image/look-up-icon.png)\).
2.  Select configuration item.

**Note:** By default, Service Offering is filtered out and CIs with Principal Class are selected. The Principal Class filter functionality is applicable to the new customers starting the Paris release.

</td></tr><tr><td>

Affected CIs

</td><td>

1.  Click **Add**.
2.  Select configuration items.

**Note:** By default, Service Offering is filtered out and CIs with Principal Class are selected. The Principal Class filter functionality is applicable to the new customers starting the Paris release.

![Filter in Affected CIs related list](../../incident-management/image/affected-ci-offering-filter.png)

3.  Click **Add Selected**.


</td></tr><tr><td>

Impacted Services/CIs

</td><td>

1.  Click **Add**.
2.  Select configuration items.

**Note:** By default, Service Offering is filtered out.

3.  Click **Add Selected**.
 **Note:** If the Impacted Services/CIs is not visible on the form, [configure the form layout.](https://www.servicenow.com/docs/access?context=configure-form-layout&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

</td></tr></tbody>
</table>
**Parent Topic:**[Managing Problems](../concept/problem-mgmt-lifecycle.md)

