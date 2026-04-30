---
title: NLU Workbench roles
description: NLU Workbench is installed with these roles.Users who have read access to models in NLU Workbench.Users who can edit NLU models assigned to them in NLU Workbench.Users who can use NLU Workbench to manage NLU models.Data labelling \(NLU feedback\) Admin role - to manage data labelling across models also ability to optimize models.
locale: en-US
release: xanadu
product: NLU Service
classification: nlu-service
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Exploring Natural Language Understanding, Natural Language Understanding, Enable AI experiences]
---

# NLU Workbench roles

NLU Workbench is installed with these roles.

To learn more about managing per-user subscriptions, see [Managing per-user subscriptions in Subscription Management](https://www.servicenow.com/docs/access?context=managing-user-subscriptions-v2&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US) and contact your account representative.

**Parent Topic:**[Exploring Natural Language Understanding](../concept/nlu-explore.md)

## NLU user \[nlu\_user\]

Users who have read access to models in NLU Workbench.

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

This role is installed with NLU Workbench - Core. This role does not have access to NLU Model Performance.

## NLU editor \[nlu\_editor\]

Users who can edit NLU models assigned to them in NLU Workbench.

### Contains Roles

List of roles contained within the role.

-   import\_admin
-   sn\_ace.ace\_user
-   nlu\_user

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

This role is installed with NLU Workbench - Core.

## NLU administrator \[nlu\_admin\]

Users who can use NLU Workbench to manage NLU models.

### Contains Roles

List of roles contained within the role.

-   sn\_ace.ace\_user
-   sn\_nlu\_workbench.nlu\_feedback\_admin
-   nlu\_editor
-   nlu\_user

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

This role is installed with NLU Workbench - Core.

## NLU feedback admin \[sn\_nlu\_workbench.nlu\_feedback\_admin\]

Data labelling \(NLU feedback\) Admin role - to manage data labelling across models also ability to optimize models.

### Contains Roles

List of roles contained within the role.

-   sn\_ace.ace\_user
-   platform\_ml\_write
-   platform\_ml\_create
-   ml\_labeler

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

**Important:** Avoid granting an admin role when more specialized roles are available.

This role is installed with NLU Workbench - Advanced Features. For more information, see [NLU Workbench - Advanced Features](../concept/nlu-workbench-advanced-features.md).

This role is used in Expert Feedback Loop modules. For more information, see [NLU Expert Feedback Loop](../concept/nlu-expert-feedback-loop.md) or [Issue Auto Resolution Tuning in NLU](../concept/issue-auto-resolution-tuning-nlu.md).

