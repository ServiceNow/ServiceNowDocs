---
title: Configure proactive case flows for business organizations
description: Automate workflows for proactive case creation to improve your operational efficiency and respond to business organizations issues faster.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/configure-flow-designer-bo.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure Proactive Customer Service, Extend capabilities, Configure, Customer Service Management]
---

# Configure proactive case flows for business organizations

Automate workflows for proactive case creation to improve your operational efficiency and respond to business organizations issues faster.

## Before you begin

**Note:** To use Proactive Customer Service Operations for business organizations, the Business Location \(com.snc.business\_location\) and Proactive Customer Service Operations with Event Management \(sn\_pro\_cs\_itom\) plugins are required.

Role required: admin

## About this task

Digital services used by businesses organizations, referred as Install Base Items, are supported as affected install base items in the proactive and major cases.

Modify the default configuration of processing a proactive case according to your business requirement. You can automate that a proactive case is proposed to a major case or is directly promoted to a major case. If promoted directly to a major case, child cases are automatically created when multiple customers are impacted. For more information on the major issue management, see [Major issue management overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/major-issue-management.md).

**Note:** When using proactive customer service with business organizations, keep the install base items for business organizations separate from the install base items for accounts. In other words, don’t use a single configuration item for both accounts and business organizations.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Proactive Case Flows**.

2.  Select the **Process Proactive Cases Created from Alerts** flow.

3.  Select the **Process Proactive Cases for Single and Multiple Business Organizations** subflow.

4.  In the **Major Case Status** field, set the initial status of the major case for multiple business organizations.

    By default, this field is set to **Proposed**. Based on your selection, the proactive case is either **Proposed**, **Accepted**, or **None**. If you set the status to **Accepted**, child cases are created automatically.

    For more information on the major issue management, see [Major issue management overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/major-issue-management.md).

5.  In the **Affected Business Organization Threshold field** field, enter the number of affected business organizations required for a proactive case to be eligible for major case processing.

    The default is two. If the count of Business Organizations is greater than or equal to the affected business organization threshold, and major case status is set to proposed, then the case is proposed as a major case and a work note is added about the same in the case.

6.  Select the **Process Case for Single Business Organization** check box to update impacted business organization in the **Requestor Organization** field on the proactive case.

    This also applies if multiple install base items from the same Business Organization are affected.

7.  Select **Done**.


**Related topics**  


[Proactive Customer Service Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/proactive-service-operations.md)

[Major issue management overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/major-issue-management.md)

