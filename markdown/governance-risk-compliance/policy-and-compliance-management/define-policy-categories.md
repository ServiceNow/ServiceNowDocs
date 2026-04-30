---
title: Define policy categories
description: You can filter policies by specific criteria to limit the number of policies displayed when you are creating policy exceptions.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Allow policy exception requests, Enhancement steps, Implement, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Define policy categories

You can filter policies by specific criteria to limit the number of policies displayed when you are creating policy exceptions.

## Before you begin

Role required: sn\_compliance.manager

## Procedure

1.  When defining the [Policy Exception Integration Registry](enable-other-apps-to-request-policy-exceptions.md), click the lock icon on the **Policy categories** field.

    ![Policy category](../image/policy-cat.png)

2.  In the Policy categories form, click **New**.

3.  Enter the name and description of the category you want to define.

4.  Repeat for any other categories you want to define.

5.  When you have finished defining categories, click the lock icon again.

    When you save the registry, the policy categories you defined are available on the Policy form for filtering policies.


## Example

Assume you defined registry entries for the Incident and Problem applications and selected Incident \[incident\] and Problem \[problem\] as the policy exception target tables. Also assume you created policy categories of **incident** and **problem**.

You have defined five policies and they are tagged as follows.

-   Policy 1 is tagged **incident**.
-   Policy 2 is tagged **incident** and **VR**.
-   Policy 3 is tagged **VR**.
-   Policy 4 is tagged **Problem**.
-   Policy 5 is untagged

You open the Problem form and click the **Request Policy Exception** button. You are prompted to enter specific details about the exception \(for example, the policy, control objective, and so forth\).

When you click the search icon in the **Policy** field, only Policy 1, Policy 2, and Policy 4 appear. If you select one of the three policies and click the search icon on the **Control objective** field, only control objectives related with that policy appear.

If none of your policies are tagged, all 5 appear. If you have only one policy tagged, that policy appears in the **Policy** field by default.

**Parent Topic:**[Allow policy exception requests from other applications](../concept/allow-other-app-policy-except.md)

