---
title: Approve and publish a policy
description: When a policy is approved, it is automatically published.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage, Classic UI, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Approve and publish a policy

When a policy is approved, it is automatically published.

## Before you begin

Role required: sn\_compliance.user or sn\_compliance.manager

**Note:** For more information:

-   About a policy, see [An overview of policy life cycle in Policy and Compliance Management](../concept/pc-policy-life-cycle-ovrvw.md).
-   About GRC application, see [Governance, Risk, and Compliance](../../grc-common/reference/r_WhatIsGRC.md).

## About this task

Prior to Version 11.0.2 of the GRC: Policy and Compliance Management application, a new knowledge base article overwrote the previous version whenever you made changes to a policy. Starting with Version 11.0.2, when you again approve a policy, a new version of the KB article is created and listed in the **Policy Versions** tab, along with a history of previous versions.

This feature requires that you manually install and activate the Knowledge Management Advanced Installer \[com.snc.knowledge\_advanced.installer\] plugin. For more information, see Activate a plugin.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Policies and Procedures** &gt; **Policies**.

2.  Open the policy record.

3.  Review the policy details.

4.  Click the **Request Approval** button.

    Reviewers cannot request approval for a policy. To request approval, the policy owner must have at least the **sn\_compliance.user** role, which is the minimum role required. Users with the **sn\_compliance.manager** role can also request approval.

    After the approval is granted, the policy is published, and a knowledge base \(KB\) article is automatically created with the policy details.

5.  Any time you need to make changes to the policy, you can click **Edit policy** and enter a message in the pop-up, and click **Request Approval**. Add a comment in the pop-up. When approval is granted, a new version of the knowledge base article is created.

    **Note:** As described above, if you activated the Knowledge Management Advanced Installer \[com.snc.knowledge\_advanced.installer\] plugin, a new version of the KB article is created and listed in the **Policy Versions** tab, along with a history of previous versions as shown below.

    ![Policy versions](../image/policy-versions.png "Policy versions")

    So, if you create links to this policy from the Service Portal or elsewhere, the latest version of the KB article is always displayed.


**Parent Topic:**[Manage control objectives and policies](../reference/r_PoliciesAndProcedures.md)

