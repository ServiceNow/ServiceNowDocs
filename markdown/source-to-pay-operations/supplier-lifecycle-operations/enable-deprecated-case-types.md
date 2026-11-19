---
title: Enable deprecated case types after upgrade
description: After you upgrade to Yokohama, you can enable deprecated case types if you have the admin role.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/source-to-pay-operations/supplier-lifecycle-operations/enable-deprecated-case-types.html
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Post-upgrade tasks for Supplier Case Management, Install Supplier Lifecycle Operations, Configuring Supplier Lifecycle Operations, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Enable deprecated case types after upgrade

After you upgrade to Yokohama, you can enable deprecated case types if you have the admin role.

## Before you begin

Role required: admin

## About this task

In the yokohama release, the **Conduct a risk assessment** and **Conduct a tiering risk assessment** case types have been deprecated. However, you can perform this task to enable and use these case types after upgrade.

## Procedure

1.  Select **All**.

2.  In the navigation filter, enter **sn\_slm\_case\_list.do**.

    The Supplier Cases page opens listing all the supplier cases.

3.  Select **New**.

4.  Right-click the **Case type** field label and select **Configure Choices**.

    The Configuring Case type Choices page opens.

5.  In the Available list, double-click the **Conduct a risk assessment \(Deprecated\)** and **Conduct a tiering risk assessment \(Deprecated\)** case types to move them to the Selected list.

6.  Select **Save**.

    The deprecated case types now appear in the **Case type** field on the Create New Supplier Case form.


**Parent Topic:**[Post-upgrade tasks for Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/source-to-pay-operations/supplier-lifecycle-operations/post-upgrade-tasks-slo.md)

**Related topics**  


[Run fix script to update the KPI weighted score field in the KPI score table]()

[Run fix script to update the Aggregation method field in the KPI table]()

[Run fix script to update the KPI Instruction field in the Supplier Task table]()

[Run fix scripts to enable Automated KPI collection]()

[Run fix script to migrate existing data from the deprecated Action type column after upgrade]()

[Run fix script to use the Supplier Manager Workspace after upgrading to the Yokohama release]()

[Processing the skipped supplier catalog item records after upgrade]()

