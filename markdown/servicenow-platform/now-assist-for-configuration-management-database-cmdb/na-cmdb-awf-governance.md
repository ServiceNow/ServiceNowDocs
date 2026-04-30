---
title: CMDB governance agentic workflow
description: Data governance can be an overwhelming task. The Provide advice on CMDB governance agentic workflow supports data admins and owners by methodically working through the many-faceted process of improving CMDB data accuracy, completeness, and health. The objective is to ensure that users can trust the data that they use for their work.
locale: en-US
release: xanadu
product: Now Assist for Configuration Management Database \(CMDB\)
classification: now-assist-for-configuration-management-database-cmdb
topic_type: concept
last_updated: "2025-04-22"
reading_time_minutes: 2
breadcrumb: [Using Now Assist for CMDB, Now Assist for Configuration Management Database \(CMDB\), CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB governance agentic workflow

Data governance can be an overwhelming task. The Provide advice on CMDB governance agentic workflow supports data admins and owners by methodically working through the many-faceted process of improving CMDB data accuracy, completeness, and health. The objective is to ensure that users can trust the data that they use for their work.

## CMDB governance agentic workflow

You must have the sn\_cmdb\_admin role to use the CI creator agentic workflow.

The CMDB Governance agentic workflow supports admins and owners with information on data health and ongoing guidance for governance as data models and integrations grow. The workflow proceeds along the following path:

1.  Provide guidance on which classes are best for you to tag as principal classes. Tagging a CI as a principal class is a practical way to save time because you can configure ServiceNow AI Platform products to display only principal classes in lists. The workflow helps you to decide which CIs you are most likely to work with day-to-day and then provides a link to enable you to tag CIs as principal classes.
2.  Ensure that life-cycle policies are in place for the principal classes. If the workflow detects that life-cycle policies are not in place, it provides a link to the appropriate page so you can manage the policies. For more information, see [Working with CMDB Data Manager](../../configuration-management/concept/cmdb-data-management.md).
3.  Ensure that data certification policies are in place for the principal classes. If the workflow detects that data certification policies are not in place, it provides a link to the appropriate page so you can manage the policies. For more information, see [Working with CMDB Data Manager](../../configuration-management/concept/cmdb-data-management.md)
4.  Determine whether the CMDB Health application is activated and the CMDB Health Dashboard jobs are configured. If the jobs are not configured, the workflow provides a link to the setup instructions.
5.  Assess the quality of CI ownership data for the principal classes. The following attributes are canvassed:
    -   Is CI ownership specified? That is, is the **Owned by** value set for the CI?
    -   If the owner is a single user: Does the **Owned by** value point to an active record? That is, is the specified user correctly configured and active?
    -   If the owner is a user group: Does the **Owned by** value point to an active record? That is, is the specified user group correctly configured and active?

