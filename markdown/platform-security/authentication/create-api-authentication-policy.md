---
title: Create an API authentication policy
description: Authentication policies allow you to enforce access restrictions on the APIs based on the specified filter criteria.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API Authentication Policies, API access policy, Authentication, Access Management]
---

# Create an API authentication policy

Authentication policies allow you to enforce access restrictions on the APIs based on the specified filter criteria.

## Before you begin

Role required: api\_service\_admin, adaptive\_auth\_policy\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **API Authentication Policy**.

2.  Click **New**.

3.  On the form, fill in these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the policy.|
    |Description|Short description of the policy.|
    |Application|Scope of the application.|

4.  Right-click the form header and select **Save**.

5.  From the Policy Inputs tab, select **Edit** to add the existing Filter Criteria.

    You can also create a new Policy Input. For more information, see [Create policy inputs](https://www.servicenow.com/docs/access?context=create-policy-input&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

6.  Move one or more filter criteria from the Collections list to the Policy Inputs List.![Adding one or more filter criteria to an authentication policy.](../images/authentication-filter-criteria.png)

7.  Select **Save**.

8.  From the Policy Conditions tab, select **New**.

9.  On the form, fill in these fields.

    |Field|Description|
    |-----|-----------|
    |Label|Name of the policy condition.|
    |Description|Short description of the policy condition.|
    |Application|Scope of the application.|
    |Condition|One or more conditions that are combined with **OR** filter.|

    ![Example policy condition with multiple criteria.](../images/policy-conditions-authentication.png)

10. Select **Submit**.


