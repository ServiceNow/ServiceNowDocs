---
title: Enable integration with ServiceNow DevOps in Split tool
description: Enable integration with ServiceNow DevOps in Split tool and restrict approvers to only the enabled integration for your environment.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/devops-change-velocity/enable-integration-servicenow-devops-split.html
release: zurich
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Split, Integrate, DevOps Change Velocity, IT Service Management]
---

# Enable integration with ServiceNow DevOps in Split tool

Enable integration with ServiceNow DevOps in Split tool and restrict approvers to only the enabled integration for your environment.

## Before you begin

Role required: admin in Split organization

## Procedure

1.  In Split tool marketplace, navigate to **Admin Settings &gt; Integrations**.

2.  Add ServiceNow DevOps in the **Integration Name** field, and select **Save**.\[Omitted image "split-admin-settings.png"\] Alt text: ServiceNow admin settings in Split tool

    A token is generated, which must be used while onboarding the Split.io tool.

3.  Navigate to **Admin Settings &gt; Workspaces &gt; Choose the required workspace &gt; Edit the Environment**.

4.  In the **Change permissions** field, select **Require approvals for changes &gt; Restrict who can approve**.

5.  Select **Integrations** from the drop-down and select the integration configured in step 2 as, and select **Save**.\[Omitted image "split-restrict-approver.png"\] Alt text: Restrict approvers for environment


**Parent Topic:**[Split.io integration with DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/devops-change-velocity/split-integration-devops-classic.md)

