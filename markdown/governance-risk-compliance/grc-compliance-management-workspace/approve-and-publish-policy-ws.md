---
title: Approve and publish a policy using the Compliance Workspace
description: When a policy is approved, it is automatically published.
locale: en-US
release: yokohama
product: GRC: Compliance Management Workspace
classification: grc-compliance-management-workspace
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Manage control objectives and policies using the Compliance Workspace, Using the Compliance Workspace, Performing compliance tasks in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Approve and publish a policy using the Compliance Workspace

When a policy is approved, it is automatically published.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst or sn\_compliance\_ws.corporate\_compliance\_manager

## About this task

Prior to Version 11.0.2 of the GRC: Policy and Compliance Management application, a new knowledge base article overwrote the previous version whenever you made changes to a policy. Starting with Version 11.0.2, when you again approve a policy, a new version of the KB article is created and listed in the **Policy Versions** tab, along with a history of previous versions.

This feature requires that you manually install and activate the Knowledge Management Advanced Installer \[com.snc.knowledge\_advanced.installer\] plugin. For more information, see [Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Policies**.

2.  Open the policy record.

3.  Review the policy details.

4.  Click the **Request Approval** button.

    Reviewers cannot request approval for a policy. However, the owner of the policy and users with the Corporate compliance manager role can request approval for a policy. When approval is granted, the policy is published and a knowledge base \(KB\) article is automatically created with the details of the policy.

5.  Any time you need to make changes to the policy, you can click **Edit policy** and enter a message in the pop-up, and click **Request Approval**. Add a comment in the pop-up. When approval is granted, a new version of the knowledge base article is created.

    **Note:** As described above, if you activated the Knowledge Management Advanced Installer \[com.snc.knowledge\_advanced.installer\] plugin, a new version of the KB article is created and listed in the **Policy Versions** tab.

    So, if you create links to this policy from the Service Portal or elsewhere, the latest version of the KB article is always displayed.


