---
title: Provide document access to policy users
description: Grant access to the users who have assigned roles to collaborate on the redlining-enabled policy.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Policy authoring and redlining in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Provide document access to policy users

Grant access to the users who have assigned roles to collaborate on the redlining-enabled policy.

## Before you begin

Role required: sn\_compliance\_ws.corporate\_compliance\_analyst; mp\_document\_user

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.

2.  In the Compliance Workspace, select the list icon \(![](../../grc-cam-workspace/image/ws-list-icon.png)\).

3.  Navigate to **Compliance library** &gt; **My policies**.

4.  Select a policy to open.

5.  To view all the users of this policy and their respective roles who can access the document, select the **Document access** related list.

    The **Document access** related list is visible only when policy redlining is enabled for the policy. The Document access \[sn\_irm\_shared\_cmn\_document\_access\] table stores the created and updated information of the policy record whenever there were corresponding changes to the user roles such as approvers, contributors, reviewers, or owners who have access to the redlining-enabled policy.

    The users identified in the **Policy Assignment** section of the Details related list as Owners, Approvers, Reviewers, and Contributors are users listed in the Document access related list for the redlining-enabled policy. A user can also have multiple roles.

    The **Status** column reveals the status of access each user has on the policy.

    A valid email address of the user, configured in the sys\_user table, is required to access the document hosted in cloud from the Document Access related list.

    **Note:** Although users of Microsoft OneDrive are granted edit access, not all of them can edit the document. The edit access depends on the state of the policy.

    -   If the policy is in Draft state, the Owner and Contributors have edit access. The Approvers and Reviewers get read access only.
    -   If the policy is in Review state, the Owner and Reviewers have edit access to the document. Contributors at this state do not contribute to the policy and can only read the document. Approvers also have only read access.
    -   If the policy is in Awaiting approval, Published, or Retired states, then all users have read access only.

