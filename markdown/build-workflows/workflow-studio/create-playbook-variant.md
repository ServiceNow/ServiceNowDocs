---
title: Create a playbook variant
description: Create variations of a playbook for different use cases.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2024-11-05"
reading_time_minutes: 3
breadcrumb: [Playbook variants, Playbooks in Workflow Studio, Building playbooks, Using Workflow Studio, Workflow Studio, Build workflows]
---

# Create a playbook variant

Create variations of a playbook for different use cases.

## Before you begin

Role required: admin or playbook.admin

## Procedure

1.  Navigate to **All** &gt; **Workflow Studio**.

2.  Open the playbook that you want to create variant for.

3.  Select the variant icon \(![](../images/playbook-variants-icon.png)\) to open the variant panel on the left.

4.  Select **Add a variant**.

5.  Fill in the following fields.

<table id="choicetable_oqd_gxb_hdc"><tbody><tr><td id="d108457e92">

**Variant name**

</td><td>

Enter a unique, user-facing name for your playbook variant. This name appears to agents and fulfillers when this variant runs.

</td></tr><tr><td id="d108457e104">

**Conditions**

</td><td>

In the condition builder, select or enter a field, operator, and value.**Note:** To learn more about condition builders, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Add more conditions for this variant to run, as needed.

</td></tr></tbody>
</table>    In this example, we want to create different versions of a base recruitment process playbook for individual contributors \(IC\) and managers. In the condition builder, we indicate whether the variant is for management roles or not.

    ![Conditions for the IC variant of a recruitment playbook](../images/playbook-variant-conditions.png "IC variant")

    ![Conditions for the manager variant of a recruitment playbook](../images/playbook-variant-conditions-2.png "Manager variant")

6.  Select **Create variant**.

    You have two new variants of the base recruitment playbook, one for ICs and one for managers.

    ![Playbook variants panel with variants of a base playbook](../images/playbook-variants-panel.png)

    The color of the canvas border corresponds to the color of the variant that is open.

    **Important:** The order of your variants is important. Variants are evaluated in the order that they are listed in the panel, from top to bottom. To learn more about reordering your variants, see [Re-order playbook variants](reorder-playbook-variants.md).

7.  As you make changes to your variants, make sure all activity properties are still configured as needed.

    Override properties for an activity if they should be different from the parent playbook.

    ![Override activity property button](../images/override-activity-property.png)

    Activities that are the same as in a parent playbook are grayed out. If you change or add an activity, it is shown in full color.

    **Note:** For more general guidelines, see [General Guidelines](../concept/playbook-variants.md#general-guidelines-playbook-variants).

8.  Add a child variant to a variant.

    1.  **Note:** You can nest child variants up to 6 levels.

        Hover over the variant in the variant panel, and select the kebab menu to open the action menu.

    2.  Select **Add child variant**.

    3.  Fill in the following fields.

<table id="table_rzt_rxc_hdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Variant name**

</td><td>

Enter a unique, user-facing name for your playbook variant. This name appears to agents and fulfillers when this variant runs.

</td></tr><tr><td>

**Conditions**

</td><td>

In the condition builder, select or enter a field, operator, and value. To learn more about condition builders, see [Condition builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

Add more conditions for this variant to run, as needed.**Note:** Child variants automatically inherit the conditions of the parent variant.

</td></tr></tbody>
</table>        In this example, we want to create a child variant of the Manager variant for recruiting senior managers and above. We add an extra condition to specify that this particular Manager child variant runs for levels M4 to M6 manager roles.

        ![Adding a child variant for senior managers under the Manager variant](../images/playbook-child-variant-conditions.png)

9.  Follow step 8 to add a variant at the same level as another variant \(a sibling variant\), but choose the **Add sibling variant** option instead.

    ![Playbook variants action menu with Add sibling variant option highlighted](../images/playbook-variants-action-menu.png)

10. Edit a playbook variant's conditions.

    1.  Hover over the variant in the variant panel, and select the kebab menu to open the action menu.

    2.  Select **Edit properties**.

11. To save a variant as a favorite, see [Save a playbook variant as a favorite](bookmark-playbook-variant.md).


## What to do next

Re-order your playbook variants. To learn more about reordering your variants, see [Re-order playbook variants](reorder-playbook-variants.md).

**Parent Topic:**[Playbook variants](../concept/playbook-variants.md)

