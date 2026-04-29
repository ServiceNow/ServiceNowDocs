---
title: Service Catalog category
description: Validate single catalog item transactions as well as requester and fulfiller flows in Service Catalog.Open a catalog item.Open a record producer.Set variable values for the current catalog item or the record producer.Set the quantity for the current catalog item.Validate variable values on the current catalog item or record producer.Validate the state of variables. Possible variable states are mandatory, not mandatory, read only, not read only, visible, and not visible.Validate price and recurring price of a catalog item. Use this step after opening a catalog item page using the Open a Catalog Item step, and before using the Order Catalog Item step.Add a catalog item to the shopping cart. Use this step after opening a catalog item page using the Open a Catalog Item step. After this step, you cannot use any other steps on the catalog item.Clicks Order Now for a catalog item. Use this step after opening a catalog item page using the Open a Catalog Item step.Submits the current record producer. Use this step after opening the record producer page using the Open a Record producer step. After this step, you cannot use any other steps on the catalog item.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 13
breadcrumb: [Automated Test Framework \(ATF\) test step categories, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Service Catalog category

Validate single catalog item transactions as well as requester and fulfiller flows in Service Catalog.

## Activation of the Automated Test Framework for Service Catalog

These test steps require activation of the The Automated Test Framework Service Catalog \(com.glide.automated\_testing\_impl.service\_catalog\) plugin, which is active by default on new instances. Administrators may need to activate the plugin on instances upgraded from earlier versions.

## Support for parametrized tests

Service Catalog step configurations support parametrized tests. For more information on parametrized tests, refer to [Parameterized tests](../concept/parameterized-tests.md).

## Variable editor support

After opening a record that supports variable editor \(requested item, catalog task, or incident\), you can add step configurations to set variable values, or validate variable states or values. Use the step configurations in the following order to support variable editor.

1.  Step configurations to order a catalog item or record producer in the **Service Catalog** category.
2.  **Open an Existing Record** step configuration in the **Form** category.
3.  **Set Variable Values**, **Validate Variable Values**, or **Variable State Validation** step configuration in the **Service Catalog** category.

**Note:** Custom variables and custom variable with labels are not supported for Set Variable Values, Validate Variable Values, and Variable State Validation step configurations.

## Open a Catalog Item

Open a catalog item.

<table id="table_czs_hv2_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Catalog Item

</td><td id="atf-catalog-item">

Catalog item that you want to open.**Note:** You should have access to this catalog item.

</td></tr></tbody>
</table>## Open a Record Producer

Open a record producer.

<table id="table_q13_5w2_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Record Producer

</td><td id="atf-record-producer">

Record producer that you want to open.**Note:** You should have access to the record producer.

</td></tr></tbody>
</table>## Set Variable Values

Set variable values for the current catalog item or the record producer.

For a catalog item, use this step after opening a catalog item page using the **Open a Catalog Item** step, and before using the **Order Catalog Item** step. For a record producer, use this step after opening a record producer page using the **Open a Record Producer** step, and before using the **Submit Record Producer** step.

<table id="table_fzv_hz2_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes-condition-builder">

Notes about the test step.**Note:** Use the condition builder to set the field value. The condition builder displays an appropriate control for the field data type. For example, a reference field displays a **Lookup record** control.

</td></tr><tr><td>

Item

</td><td id="atf-item">

Catalog item or record producer for which you want to set variable values.

</td></tr><tr><td>

Variable Values

</td><td id="atf-variable-values">

List of variables and the values that you want to set for them.**Note:** You can set the value for multiple variables.

</td></tr></tbody>
</table>## Set Catalog Item Quantity

Set the quantity for the current catalog item.

<table id="table_lkm_x1f_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Item

</td><td id="atf-item-set-cat-item-quantity">

Catalog item whose quantity you want to set.

</td></tr><tr><td>

Quantity

</td><td id="atf-quantity-set-cat-item-quantity">

Quantity you want to set for the catalog item.

</td></tr></tbody>
</table>## Validate Variable Values

Validate variable values on the current catalog item or record producer.

For a catalog item, use this step after opening a catalog item page using the **Open a Catalog Item** step, and before using the **Order Catalog Item** step. For a record producer, use this step after opening a record producer page using the **Open a Record Producer** step, and before using the **Submit Record Producer** step.

<table id="table_f2q_vbf_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td id="atf-timeout">

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes-condition-builder">

Notes about the test step.**Note:** Use the condition builder to set the field value. The condition builder displays an appropriate control for the field data type. For example, a reference field displays a **Lookup record** control.

</td></tr><tr><td>

Item

</td><td id="atf-item-validate">

Catalog item or record producer whose variables should be validated.

</td></tr><tr><td>

Catalog Conditions

</td><td id="atf-catalog-conditions">

Conditions for variable validation. If the conditions are met, the test passes.**Note:** The label of a variable associated with a variable set reflects the variable set name. The format is *variable\_set\_name » variable\_name*.

</td></tr></tbody>
</table>## Variable State Validation

Validate the state of variables. Possible variable states are mandatory, not mandatory, read only, not read only, visible, and not visible.

<table id="table_tzv_cnk_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td id="atf-timeout">

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Catalog item

</td><td id="atf-cat-item-state-validation">

Catalog item for which you want to validate the state.**Note:** You should have access to this catalog item.

</td></tr><tr><td>

Visible

</td><td id="atf-visible">

List of the catalog item variables that must be visible for the step to pass.

</td></tr><tr><td>

Not visible

</td><td id="atf-not-visible">

List of the catalog item variables that must be hidden for the step to pass.

</td></tr><tr><td>

Read only

</td><td id="atf-read-only">

List of the catalog item variables that must be read-only for the step to pass.

</td></tr><tr><td>

Not read only

</td><td id="atf-not-read-only">

List of the catalog item variables that must not be read-only for the step to pass.

</td></tr><tr><td>

Mandatory

</td><td id="atf-mandatory">

List of the catalog item variables that must be mandatory for the step to pass.

</td></tr><tr><td>

Not mandatory

</td><td id="atf-not-mandatory">

List of the catalog item variables that must not be mandatory for the step to pass.

</td></tr></tbody>
</table>## Validate Price and Recurring Price

Validate price and recurring price of a catalog item. Use this step after opening a catalog item page using the **Open a Catalog Item** step, and before using the **Order Catalog Item** step.

<table id="table_a1r_zpk_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Price

</td><td id="atf-price">

Price of the catalog item for the step to pass.

</td></tr><tr><td>

Recurring price

</td><td id="atf-recurring-price">

Recurring price of the catalog item for the step to pass.

</td></tr><tr><td>

Recurring price frequency

</td><td id="atf-recurring-price-frequency">

Recurring price frequency of the catalog item for the step to pass.

</td></tr></tbody>
</table>## Add Item to Shopping Cart

Add a catalog item to the shopping cart. Use this step after opening a catalog item page using the Open a Catalog Item step. After this step, you cannot use any other steps on the catalog item.

<table id="table_g5z_tqk_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td id="atf-timeout">

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Assert Type

</td><td id="atf-assert-type-add-item">

Criteria for the test to pass.-   **Successfully added item to Shopping Cart**

Test passes only if the catalog item is successfully added to the shopping cart.

-   **Cannot add item to Shopping Cart**

Test passes only if the catalog item cannot be added to the shopping cart.


</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|cart\_item\_id|The sys\_id of the added catalog item.|

## Order Catalog Item

Clicks **Order Now** for a catalog item. Use this step after opening a catalog item page using the Open a Catalog Item step.

After this step, you cannot use any other steps on the catalog item. If the two-step checkout is false, a request is generated for the catalog item. If the two-step checkout is true, you are redirected to the cart preview page.

<table id="table_wtz_hrk_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td id="atf-timeout">

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Assert type

</td><td id="atf-assert-type-order-catalog-item">

Criteria for the test to pass.-   **Successfully ordered Catalog Item**

Test passes only if the catalog item is successfully ordered.

-   **Cannot order Catalog Item**

Test passes only if the catalog item cannot be ordered.


</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|request\_id|The sys\_id of the created catalog request.|
|cart|the sys\_id of the cart holding the catalog item.|

## Submit Record Producer

Submits the current record producer. Use this step after opening the record producer page using the Open a Record producer step. After this step, you cannot use any other steps on the catalog item.

<table id="table_rhb_vrk_xz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Execution order

</td><td id="atf-exec-order">

Integer specifying the order in which the test executes this step.As you create steps, the system automatically assigns each step an incremental value. This value causes the test to execute steps in the order that you created them in. You can change this default order by editing the **Execution order** values.

</td></tr><tr><td>

Active

</td><td id="atf-active">

Option to activate this test step for use.

</td></tr><tr><td>

Timeout

</td><td id="atf-timeout">

Number of seconds allowed before the step fails. If the validation fails, the system repeats the step until it reaches the duration of the timeout. If the validation fails after the timeout duration has passed, the step fails.

</td></tr><tr><td>

Application

</td><td id="atf-application-scope">

Application scope in which the system runs this step.

</td></tr><tr><td>

Test

</td><td id="atf-test">

Read-only name of the test that you're adding the step to.

</td></tr><tr><td>

Step config

</td><td id="atf-step-config">

Read-only name of the step.

</td></tr><tr><td>

Description

</td><td id="atf-description">

Description of the test step. This field value is automatically set based on the field values of the test step. This field appears after the test step is submitted.

</td></tr><tr><td>

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Assert Type

</td><td id="atf-assert-type-submit-record-producer">

Criteria for the test to pass.-   **Successfully submitted Record Producer**

Test passes only if the record producer is submitted successfully.

-   **Cannot submit Record Producer**

Test passes only if the record producer cannot be submitted.


</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|record\_id|The sys\_id of target record of the record producer.|

