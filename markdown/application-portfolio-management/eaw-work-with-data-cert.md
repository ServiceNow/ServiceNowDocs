---
title: Working with data certification
description: In the Enterprise Architecture Workspace, enterprise architects can manage certifications alongside requests, assessments, and portfolio health insights without switching to separate modules. You can define rules for validating data \(for example, application lifecycle, technology standards\), automate recurring checks \(daily, monthly, quarterly\), assign certifiers to review and approve data. You can highlight overdue certifications and compliance gaps.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Working with data certification

In the Enterprise Architecture Workspace, enterprise architects can manage certifications alongside requests, assessments, and portfolio health insights without switching to separate modules. You can define rules for validating data \(for example, application lifecycle, technology standards\), automate recurring checks \(daily, monthly, quarterly\), assign certifiers to review and approve data. You can highlight overdue certifications and compliance gaps.

![Getting started with data certification](../../image/eaw-image/eaw-data-cert-intro.png)

## Action and required role mapping for certification policies in the Enterprise Architecture Workspace

|Action|System admin|cmdb admin + analyst|com.snc\_apm\_analyst|
|------|------------|--------------------|---------------------|
|View list of policies|Yes|Yes|Yes|
|View track progress|Yes|Yes|Yes|
|View policy by clicking a link to the policy|Yes|Yes|No|
|Create policy|Yes|Yes|No|
|Edit policy|Yes|Yes|No|
|Delete policy|Yes|Yes|Yes|
|Activate policy|Yes|Yes|Yes|
|Deactivate policy|Yes|Yes|Yes|
|Run certification|Yes|Yes|Yes|
|Complete certification through Track progress page|Yes|Yes|No|

-   **[Create a certification policy](../../task/eaw-task/eaw-create-policy.md)**  
Creating a data certification policy serves as a governance mechanism to ensure that the data used in enterprise architecture models and visualizations is accurate, complete, and trustworthy.
-   **[Edit a certification policy](../../task/eaw-task/eaw-data-cert-edit-policy.md)**  
Update an certification existing policy details. You can edit the draft or inactive certification policies.
-   **[View certification policy](../../task/eaw-task/eaw-data-cert-view-policy.md)**  
View details of a published policy.
-   **[Publish a certification policy](../../task/eaw-task/eaw-data-cert-publish-policy.md)**  
Publish a draft policy to activate it and enable certifications to be issued under that policy.
-   **[Run certification for a policy](../../task/eaw-task/eaw-data-cert-run-certification.md)**  
Run certification for published policies to generate a new certification instance for an active policy.
-   **[Track progress of a certification policy](../../task/eaw-task/eaw-data-cert-track-progress.md)**  
Monitor and review the certification policy status to track completion progress and view details such as total tasks, completed tasks, open tasks, and unassigned tasks.
-   **[Review and certify data certification tasks](../../task/eaw-task/eaw-approve-data-cert-tasks.md)**  
You can review and complete data certification tasks to confirm that records meet the standards defined in a certification policy. Certification tasks are generated when a policy is run and are assigned based on the policy's assignment configuration.
-   **[Activate a certification policy](../../task/eaw-task/eaw-data-cert-activate.md)**  
Activate a certification policy to add it to the active certification runs. This process ensures that the policy is active and can be used for certifications.
-   **[Deactivate a certification policy](../../task/eaw-task/eaw-data-cert-deactivate.md)**  
Deactivate a published policy to remove it from active certification runs. This process ensures that the policy is no longer active and can't be used for certifications.
-   **[Delete a certification policy](../../task/eaw-task/eaw-delete-data-cert.md)**  
Delete an unwanted certification policy permanently.

**Parent Topic:**[Managing Enterprise Architecture Workspace](eaw-managing-ea-workspace.md)

