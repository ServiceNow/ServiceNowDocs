---
title: Map policies to a deployable
description: Map policies to a deployable to define the validation processes that the config data must pass. You can map policies to a deployable using static mapping or dynamic mapping.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Mapping policies in DevOps Config, Configure, DevOps Config, IT Service Management]
---

# Map policies to a deployable

Map policies to a deployable to define the validation processes that the config data must pass.You can map policies to a deployable using static mapping or dynamic mapping.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_policy\_editor or cdm\_editor or cdm\_admin

## About this task

Policies validate any changes to the mapped deployable. Whenever changes that affect a deployable are committed, the system generates a new snapshot of the deployable and then executes all mapped policies against the snapshot. You can also manually execute a policy at any time \(for example, to test a policy operation\).

## Procedure

1.  On the **Policies** tab for an application, select **Manage static mappings**.

    The Manage static mappings page lists all deployables that have mapped policies. Policies are grouped by the deployable to which they’re mapped.

2.  Select **Add**.

    The Map Policies dialog box displays with a list of available policies.

3.  Select a deployable against which the policies should be executed.

4.  Select the policies in the **Policies** list.

    You can map any number of policies.

5.  Select **Map Policies**.

    On the **Manage static mappings** page, the deployable is updated with the list of mapped policies.

<table id="table_m45_kkk_spb"><thead><tr><th>

Column header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Policy name

</td><td>

Name of the policy. Policies appear grouped under the deployable to which they’re mapped.

</td></tr><tr><td>

Input

</td><td>

Policy settings that are configurable.

</td></tr><tr><td>

Dynamic mapping

</td><td>

Identifier to denote whether the policy is mapped dynamically or statically.-   **true**: The policy is mapped dynamically based on the defined conditions.
-   **false**: The policy is mapped statically.


</td></tr><tr><td>

Condition

</td><td>

Business conditions based on which the policy is mapped dynamically to specific deployables.For example, to dynamically map policies to only deployables that have the environment type as production, you can define the condition as: **\[Environment\]\[is\]\[Production\]**.

For more information on defining a condition, see [Map PaCE policies using Dynamic Mapping](https://www.servicenow.com/docs/access?context=pace-validate-dynamic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

</td></tr><tr><td>

Description

</td><td>

Description of the policy, specifying what it validates.

</td></tr><tr><td>

Category

</td><td>

Identifier that enables policy grouping. For example, `Production Policies`.

</td></tr><tr><td>

Input status

</td><td>

Validation state of the mapping inputs in the policy.**Note:**

-   This information reflects the validity of the input settings \(that is, the readiness of the policy to perform validation\).
-   All mapping inputs are valid on insertion. Inputs become invalid if the policy version is archived or deleted.
-   This value does not indicate whether the snapshot passed validation \(that is, whether the snapshot is compliant\).


</td></tr><tr><td>

State

</td><td>

Mapping state of the policy with the deployable.Only mapped policies that are **active** execute during snapshot validation.

</td></tr><tr><td>

Tags

</td><td>

Tags that are associated with the policy.

</td></tr></tbody>
</table>
**Parent Topic:**[Mapping policies in DevOps Config](../../devops-config/concept/devops-config-mapping-policies.md)

**Related topics**  


[Map PaCE policies using Static Mapping](https://www.servicenow.com/docs/access?context=pace-validate-static&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

[Map PaCE policies using Dynamic Mapping](https://www.servicenow.com/docs/access?context=pace-validate-dynamic&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)

