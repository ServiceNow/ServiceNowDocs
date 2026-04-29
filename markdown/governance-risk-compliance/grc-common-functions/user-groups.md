---
title: User group-based access on the GRC tables
description: You can allow a set of users to access only specific records by creating user groups on the GRC tables. When you have created the user groups, you can segregate your data based on a specific criteria and allow only those users who belong to a user group to view the data.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# User group-based access on the GRC tables

You can allow a set of users to access only specific records by creating user groups on the GRC tables. When you have created the user groups, you can segregate your data based on a specific criteria and allow only those users who belong to a user group to view the data.

**Note:** User group-based access is not enabled on any ServiceNow tables as part of the base system. To implement the feature and to configure the Access groups option on any GRC form, follow the steps listed in the [KB1514113](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1514113).

To view the Access groups option on the respective tables where you have configured user group-based access, you must enable the **Enable access groups** property in the GRC Properties module.

The following example shows the Access groups option in the form that appears when you enable user group-based access. The layout of the form depends on your configuration.

![Access groups option in the form.](../image/access-groups-on-risk-form.png "Access groups option in the form")

When a value is selected for the Access groups list, only the members of the groups that are mentioned in the list can access the data within the same role.

For example, consider this scenario. Within the Risk Managers access group, you have two managers who can work on a financial risk and other managers who can work on an operational risk. By giving the same risk manager role to all the managers in this access group, the first two managers can be assigned to the financial group and the other managers can be assigned to the operational risk group.

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

