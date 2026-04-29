---
title: Service Catalog in Service Portal category
description: Validate catalog item transactions and requester flows from Service Portal.Open a record producer in the Service Portal.Open a catalog item in the Service Portal.Open an order guide in the Service Portal.Add a row to a multi-row variable set included in the current catalog item in Service Portal. You can use this step configuration only when the current catalog item contains a multi-row variable set.Save the current row of a multi-row variable set included in the current catalog item in Service Portal. You can use this step configuration only when the current catalog item contains a multi-row variable set. Use this step after the Add row to multi-row variable set \(SP\) step.Set variable values for a catalog item or record producer in the Service Portal. For a catalog item, use this step after using the Open a Catalog Item \(SP\) step, and before using the Order Catalog Item \(SP\) step.Validates variable values of a catalog item or record producer in Service Portal. For a catalog item, use this step after using the Open a Catalog Item \(SP\) step, and before using the Order Catalog Item \(SP\) step.Validates the state of variables in Service Portal. Possible variable states are mandatory, not mandatory, read only, not read only, visible, and not visible.Validate the price and recurring price of a catalog item in Service Portal. Use this step after using the Open a Catalog Item \(SP\) step, and before using the Order Catalog Item \(SP\) step. This step is not applicable for a record producer.Navigate within an order guide.Set the quantity for a catalog item in Service Portal. This step is not applicable for a record producer. Use this step after using the Open a Catalog Item \(SP\) step, and before using the Order Catalog Item \(SP\) step.Validate items included in the order guide.Review the order guide summary in the Service Portal.Review individual items in the order guide and choose whether or not to include the item.Add the current catalog item to the shopping cart in Service Portal. Use this step after using the Open a Catalog Item \(SP\) step.Add an order guide to the shopping cart.Click Order Now for the current catalog item in the Service Portal. Use this step after using the Open a Catalog Item \(SP\) step.Click Order Now to order an order guide. Do not add more than one record producer to the order guide.Submit the current record producer in the Service Portal. Use this step after using the Open a Record producer \(SP\) step. After this step, you cannot use any other steps on the record producer.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 24
breadcrumb: [Automated Test Framework \(ATF\) test step categories, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Service Catalog in Service Portal category

Validate catalog item transactions and requester flows from Service Portal.

## Activation of the Automated Test Framework for Service Catalog in Service Portal

These ATF test steps require activation of the Automated Test Framework Service Catalog Service Portal \(com.glide.automated\_testing\_impl.service\_catalog\_portal\) plugin, which is active by default on new instances. Administrators may need to activate the plugin on instances upgraded from earlier versions.

## Support for parametrized tests

Service Catalog in Service Portal step configurations support parametrized tests. For more information on parametrized tests, refer to [Parameterized tests](../concept/parameterized-tests.md).

## Open a Record Producer \(SP\)

Open a record producer in the Service Portal.

<table id="table_c5b_qvv_tcb"><thead><tr><th>

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

Portal

</td><td id="atf-portal">

Portal for which you want to test this step.

</td></tr><tr><td>

Page

</td><td id="atf-page">

Service Catalog page associated with the test step.

</td></tr><tr><td>

Record Producer

</td><td id="atf-record-producer">

Record producer that you want to open.**Note:** You should have access to the record producer.

</td></tr><tr><td>

Query Parameters

</td><td id="atf-query-parameters">

URL query parameters for the page, such as **sys\_id**.

</td></tr></tbody>
</table>## Open a Catalog Item \(SP\)

Open a catalog item in the Service Portal.

<table id="table_tbt_15v_tcb"><thead><tr><th>

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

Portal

</td><td id="atf-portal">

Portal for which you want to test this step.

</td></tr><tr><td>

Page

</td><td id="atf-page">

Service Catalog page associated with the test step.

</td></tr><tr><td>

Catalog Item

</td><td id="atf-catalog-item">

Catalog item that you want to open.**Note:** You should have access to this catalog item.

</td></tr><tr><td>

Query Parameters

</td><td id="atf-query-parameters">

URL query parameters for the page, such as **sys\_id**.

</td></tr></tbody>
</table>## Open an Order Guide \(SP\)

Open an order guide in the Service Portal.

<table id="table_y5d_f43_qfb"><thead><tr><th>

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

Portal

</td><td id="atf-portal">

Portal for which you want to test this step.

</td></tr><tr><td>

Page

</td><td id="atf-page">

Service Catalog page associated with the test step.

</td></tr><tr><td>

Order Guide

</td><td id="atf-order-guide">

Order guide that you want to open.**Note:** You should have access to this order guide.

</td></tr><tr><td>

Query Parameters

</td><td id="atf-query-parameters">

URL query parameters for the page, such as **sys\_id**.

</td></tr></tbody>
</table>## Add row to multi-row variable set \(SP\)

Add a row to a multi-row variable set included in the current catalog item in Service Portal. You can use this step configuration only when the current catalog item contains a multi-row variable set.

Use this step after the Open a Catalog Item\(SP\) step, Open a Record Producer\(SP\) step, or Open an Order Guide \(SP\) step. If a contextual value has been used for the Open a Catalog Item\(SP\) step, Open a Record Producer\(SP\) step, or Open an Order Guide \(SP\) step, set the catalog item in this step.

<table id="table_ezd_5dw_hgb"><thead><tr><th>

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

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Catalog Item

</td><td>

Catalog item whose multi-row variable set requires an addition of a row. If an item is not already selected, you can either search for the item, or insert a reference to the contextual value of the item from a list of available parameters.

</td></tr><tr><td>

Multi-Row Variable Set

</td><td>

Multi-row variable set for which a row should be added.

</td></tr></tbody>
</table>## Save current row of multi-row variable set \(SP\)

Save the current row of a multi-row variable set included in the current catalog item in Service Portal. You can use this step configuration only when the current catalog item contains a multi-row variable set. Use this step after the Add row to multi-row variable set \(SP\) step.

<table id="table_oqw_sdw_hgb"><thead><tr><th>

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

Notes

</td><td id="atf-notes">

Notes about the test step.

</td></tr><tr><td>

Assert Type

</td><td>

Criteria for the test to pass.-   **Successfully saved row to a multi-row variable set**

Test passes only if the current row of the multi-row variable is saved.

-   **Cannot save a row to multi-row variable set**

Test passes only if the current row of the multi-row variable is not saved.


</td></tr></tbody>
</table>## Set Variable Values \(SP\)

Set variable values for a catalog item or record producer in the Service Portal. For a catalog item, use this step after using the Open a Catalog Item \(SP\) step, and before using the Order Catalog Item \(SP\) step.

For a record producer, use this step after using the Open a Record Producer \(SP\) step, and before using the Submit Record Producer \(SP\) step.

<table id="table_byj_pwv_tcb"><thead><tr><th>

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

Multi-Row Variable Set

</td><td>

Multi-row variable set for which variable values should be set.**Note:** Use the Add row to multi-row variable set \(SP\) step configuration prior to the current step configuration.

</td></tr><tr><td>

Variable Values

</td><td id="atf-variable-values">

List of variables and the values that you want to set for them.**Note:** You can set the value for multiple variables.

</td></tr></tbody>
</table>**Note:** Custom variables and custom variable with labels are not supported for Set Variable Values step configuration.

## Validate Variable Values \(SP\)

Validates variable values of a catalog item or record producer in Service Portal. For a catalog item, use this step after using the Open a Catalog Item \(SP\) step, and before using the Order Catalog Item \(SP\) step.

For a record producer, use this step after using the Open a Record Producer \(SP\) step, and before using the Submit Record Producer \(SP\) step.

<table id="table_sxw_wxv_tcb"><thead><tr><th>

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

Multi-Row Variable Set

</td><td>

Multi-row variable set for which variable values should be validated.**Note:** Use the Add row to multi-row variable set \(SP\) step configuration prior to the current step configuration.

</td></tr><tr><td>

Catalog Conditions

</td><td id="atf-catalog-conditions">

Conditions for variable validation. If the conditions are met, the test passes.**Note:** The label of a variable associated with a variable set reflects the variable set name. The format is *variable\_set\_name » variable\_name*.

</td></tr></tbody>
</table>**Note:** Custom variables and custom variable with labels are not supported for Validate Variable Values step configuration.

## Variable State Validation \(SP\)

Validates the state of variables in Service Portal. Possible variable states are mandatory, not mandatory, read only, not read only, visible, and not visible.

<table id="table_zf4_y1w_tcb"><thead><tr><th>

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

Item

</td><td id="atf-item-validate">

Catalog item or record producer whose variables should be validated.

</td></tr><tr><td>

Multi-Row Variable Set

</td><td>

Multi-row variable set for which variable states should be validated.**Note:** Use the Add row to multi-row variable set \(SP\) step configuration prior to the current step configuration.

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
</table>**Note:** Custom variables and custom variable with labels are not supported for Variable State Validation step configuration.

## Validate Price and Recurring Price \(SP\)

Validate the price and recurring price of a catalog item in Service Portal. Use this step after using the Open a Catalog Item \(SP\) step, and before using the Order Catalog Item \(SP\) step. This step is not applicable for a record producer.

<table id="table_ubl_clw_tcb"><thead><tr><th>

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
</table>## Navigate within Order Guide \(SP\)

Navigate within an order guide.

<table id="table_x2v_sw3_qfb"><thead><tr><th>

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

Guide Step

</td><td id="atf-guide-step">

Order guide step to which you want to navigate:-   **Describe Needs**
-   **Choose Options**
-   **Summary**

</td></tr><tr><td>

Assert Type

</td><td id="atf-assert-type-nav-order-guide">

Criteria for the test to pass.-   **Navigation Successful**

Test passes only if the navigation is successful.

-   **Navigation Failed**

Test passes only if the navigation fails.


</td></tr></tbody>
</table>## Set Catalog Item Quantity \(SP\)

Set the quantity for a catalog item in Service Portal. This step is not applicable for a record producer. Use this step after using the Open a Catalog Item \(SP\) step, and before using the Order Catalog Item \(SP\) step.

<table id="table_kzb_hxv_tcb"><thead><tr><th>

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

Quantity

</td><td id="atf-quantity">

Quantity of the catalog item that you want to order.

</td></tr></tbody>
</table>## Validate Order Guide Items \(SP\)

Validate items included in the order guide.

<table id="table_t1c_rdj_qfb"><thead><tr><th>

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

Catalog Items

</td><td id="atf-validate-catalog-items">

Catalog items that you want to validate.**Note:** You should have access to these catalog items.

</td></tr></tbody>
</table>## Review Order Guide Summary \(SP\)

Review the order guide summary in the Service Portal.

<table id="table_osf_cfj_qfb"><thead><tr><th>

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

Catalog Items

</td><td id="atf-review-catalog-items">

Catalog items that you want to review.**Note:** You should have access to these catalog items.

</td></tr><tr><td>

Price

</td><td id="atf-price">

Price of the catalog item for the step to pass.

</td></tr></tbody>
</table>## Review Item in Order Guide \(SP\)

Review individual items in the order guide and choose whether or not to include the item.

<table id="table_iqm_dhj_qfb"><thead><tr><th>

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

Catalog Item

</td><td id="atf-review-catalog-item">

Catalog item that you want to review.**Note:** You should have access to this catalog item.

</td></tr><tr><td>

Included

</td><td id="atf-included">

Selected if the catalog item should be included in the order guide, otherwise unselected.

</td></tr></tbody>
</table>## Add Item to Shopping Cart \(SP\)

Add the current catalog item to the shopping cart in Service Portal. Use this step after using the Open a Catalog Item \(SP\) step.

<table id="table_pwk_5lw_tcb"><thead><tr><th>

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

## Add Order Guide to Shopping Cart \(SP\)

Add an order guide to the shopping cart.

<table id="table_mtz_pkj_qfb"><thead><tr><th>

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

</td><td id="atf-assert-type-add-order-guide">

Criteria for the test to pass.-   **Cannot add order guide to shopping cart**

Test passes only if the order guide cannot be added to the shopping cart.

-   **Successfully added order guide to shopping cart**

Test passes only if the order guide is successfully added to the shopping cart.


</td></tr><tr><td>

 

</td><td>

 

</td></tr></tbody>
</table>## Order a Catalog Item \(SP\)

Click **Order Now** for the current catalog item in the Service Portal. Use this step after using the Open a Catalog Item \(SP\) step.

After this step, you cannot use any other steps on the catalog item. If the two-step checkout is false, a request is generated for the catalog item. If the two-step checkout is true, you are redirected to the cart preview page.

<table id="table_smw_hmw_tcb"><thead><tr><th>

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
|table|The table to which the submitted request belongs.|
|record\_id|The sys\_id of the submitted request.|

## Submit an Order Guide \(SP\)

Click **Order Now** to order an order guide. Do not add more than one record producer to the order guide.

<table id="table_rhz_ymj_qfb"><thead><tr><th>

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

</td><td id="atf-assert-type-submit-order-guide">

Criteria for the test to pass.-   **Cannot order the Order Guide**

Test passes only if the order guide cannot be ordered.

-   **Successfully ordered the Order Guide**

Test passes only if the order guide is successfully ordered.


</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|table|The table containing the submitted order guide.|
|record\_id|The sys\_id of the submitted order guide.|

## Submit Record Producer \(SP\)

Submit the current record producer in the Service Portal. Use this step after using the Open a Record producer \(SP\) step. After this step, you cannot use any other steps on the record producer.

<table id="table_s3n_rmw_tcb"><thead><tr><th>

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
|table|The table containing target record of the record producer.|

