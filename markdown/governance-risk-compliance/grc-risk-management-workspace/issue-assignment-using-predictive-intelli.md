---
title: Issue assignment using the Governance, Risk, and Compliance Predictive Intelligence plugin
description: Train a similarity solution model that uses machine learning so that the system can automatically suggest how to route issues to the correct assignee. Automatic routing suggestion reduces the time spent on deciding who should own the issue.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manually create GRC issues, Use, Risk Management, Governance, Risk, and Compliance]
---

# Issue assignment using the Governance, Risk, and Compliance Predictive Intelligence plugin

Train a similarity solution model that uses machine learning so that the system can automatically suggest how to route issues to the correct assignee. Automatic routing suggestion reduces the time spent on deciding who should own the issue.

The Governance, Risk, and Compliance: Predictive Intelligence plugin utilizes Artificial Intelligence \(AI\) and Machine Learning \(ML\) to make GRC issue management smarter. On the GRC issue form, users are given suggestions for the assignment of issues to appropriate candidates. These suggestions are based on the platform similarity solution model.

Users must train the solution definition after they install the GRC: Predictive Intelligence plugin along with its dependencies. The Platform Machine Learning Administrator \(ml\_admin\) can also customize the solution definition. This modification is based on the data in tables. Some of the critical fields, such as the filter condition **Assigned to \[is\] \[not empty\]**, must not be modified because modification may impact how the UI shows the prediction results.

-   **[Train and use the similarity solution definition for issue assignment prediction](../task/create-retrain-similarity-solution-issue-assignment.md)**  
Train and use the machine learning solution by activating the Governance, Risk, and Compliance Predictive Intelligence plugin. The solution enables the system to automatically suggest correct assignees to route issues. These suggestions reduce the time spent on deciding who should own the issue.

**Parent Topic:**[Manually create GRC issues](../../grc-common/task/t_CreateAnIssue.md)

