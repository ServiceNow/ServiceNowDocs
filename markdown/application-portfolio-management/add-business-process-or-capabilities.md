---
title: Add or edit an application business process
description: Business processes are a structured sequence of tasks that are grouped, helping to accomplish specific outcomes. You can create business processes or modify an existing one to align it with your business requirements.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Application classification, Configure, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Add or edit an application business process

Business processes are a structured sequence of tasks that are grouped, helping to accomplish specific outcomes. You can create business processes or modify an existing one to align it with your business requirements.

## Before you begin

**Important:**

Starting with the Xanadu release, the legacy business processes module is moved to the Enterprise Architecture Workspace. To learn more, see [Manage business processes](../concept/eaw-concept/eaw-business-processes.md).

Role required: sn\_apm.apm\_admin

## About this task

Based on the requirements, the business capability hierarchy can be modeled using the business process relationship. You can edit the business process records using the CI relationships to create a business process hierarchy.

A business process or capability hierarchy is an ordered grouping of business processes in a hierarchical fashion. L0 processes signify the high-level process encompassing all activities associated with that process. For example, in the IT service management business process, the L0 business process encompasses all activities related to managing IT services within the organization. L1 signifies the specific tasks within the L0 business process. For example, within the IT service management business process, incident management is an L1 business process which specifically deals with logging, categorizing, and resolving incidents.

## Procedure

1.  Navigate to **All** &gt; **Enterprise Architecture** &gt; **Administration** &gt; **Business Processes**.

2.  Select **New** to create a new business process or select the name of an existing process that you want to edit.

3.  Fill in the fields.

    For field information, see [Business Process Form](../reference/business-process-form.md).

4.  Right-click the form header and select **Save**.

5.  If you want to add items to this business process, use the Related Items [CI relations formatter](https://www.servicenow.com/docs/access?context=c_CIRelationsFormatterNG&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US).

6.  Select **Submit** or **Update**.


**Parent Topic:**[Application classification](../concept/setup-appln-class-attrib.md)

**Related topics**  


[Add or edit an application category group](application-category-groups.md)

[Add or edit an application category](add-application-categories.md)

[Add or edit an application family](add-application-families.md)

[Create an application portfolio](add-portfolios.md)

[Add a strategy for managing applications](add-idea-actions.md)

