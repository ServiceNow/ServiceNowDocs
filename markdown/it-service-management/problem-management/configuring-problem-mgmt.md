---
title: Configuring Problem Management
description: Create or redesign problem form layouts to align them with the business process workflow of your organization. Categorize problems for monitoring and reporting. Use data lookup and assignment rules to automatically assign a task to a user or group based on predefined conditions.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Problem Management, IT Service Management]
---

# Configuring Problem Management

Create or redesign problem form layouts to align them with the business process workflow of your organization. Categorize problems for monitoring and reporting. Use data lookup and assignment rules to automatically assign a task to a user or group based on predefined conditions.

**Note:**

-   Use data lookup and assignment rules to automatically assign a task to a user or group based on predefined conditions. For more information, see [Data lookup for prioritizing problems](prioritise-problems.md).
-   Configure the Problem Management properties to control features such as creating a problem task on a closed problem and reanalyzing a closed or canceled problem. For more information, see [Problem management properties](../reference/problem-mgmt-properties.md).
-   Use quick start tests to check if the Problem Management application still works after you make any configuration change such as applying an upgrade or developing an application. For more information, see [Quick start tests for Problem Management](../../../administer/atf-quick-start-tests/reference/quick-start-tests-pm.md).


## Redirection of UI16 module links to Service Operations Workspace

If the UI16 module link redirection feature is enabled in Service Operations Workspace \(SOW\) and the Problem Management module supports the redirect configuration, navigating through UI16 paths automatically redirects you to the equivalent list or record pages in SOW instead of displaying the UI16 forms or lists. For more information, see [Redirect UI16 module links to Service Operations Workspace](../../service-operations-workspace/task/redirect-ui16-module-links-sow.md).

**Note:** For new instances, this redirection configuration is automatically available in the base system. For upgrade instances, administrators can configure the redirection behavior from the SOW Admin Center.

1.  [Problem Management plugins](problem-mgmt-plugins.md)  
Many of the Problem Management plugins are activated in the base system. Others, you can activate when you are ready to use them. Some plugins include demo data.
2.  [Configure the problem form](../task/problem-configure-forms.md)  
Configure the problem form layout to conform to the workflow and the process of your organization. Add, remove, and customize fields and related lists, create problem categories, and modify links as needed.
3.  [Define an assignment rule for problems](../task/t_DefineAnAssignRuleForPRBs.md)  
After a problem is logged, it must be assigned to the appropriate group or individual to handle the problem. You can define assignment rules to automate the assignment process.
4.  [Categorize a problem as a major problem](../task/categorize-major-problem.md)  
You can prioritize a problem and highlight that it needs a review.
5.  [Enable Problem Management models](../task/enable-problem-mgmt-models.md)  
Enable the Problem Management models system property so that you can create and use custom models.
6.  [Create a problem model](../task/create-problem-model.md)  
Create custom Problem Management models with states and transitions tailored to your use cases.
7.  [Create a problem task model](../task/create-problem-task-model.md)  
Create custom Problem Management models with states and transitions tailored to your use cases.
8.  [Applying CSDM guidelines to Problem Management](pm-use-case-product-view.md)  
Problem Management helps identify the cause of an error in the IT infrastructure, reported as occurrences of related incidents. The goal of this product view is to help you to understand how Problem Management key entities work with the core CSDM framework.

**Parent Topic:**[Problem Management](c_ProblemManagement.md)

