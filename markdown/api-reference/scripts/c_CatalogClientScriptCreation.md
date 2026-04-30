---
title: Catalog client scripts
description: Client-side scripts can add dynamic effects and validation to forms. Scripts can apply to service catalog items or variable sets, allowing administrators to use the same functionality that is available on other forms.When you create catalog client scripts, be aware of the following considerations.Catalog client scripts are very similar to standard client scripts, with a few important differences.Follow this procedure to create a catalog client script.Examples of client scripts to perform common actions.
locale: en-US
release: zurich
product: Scripts
classification: scripts
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Client-side scripting, Scripting, API implementation, API implementation and reference]
---

# Catalog client scripts

Client-side scripts can add dynamic effects and validation to forms. Scripts can apply to service catalog items or variable sets, allowing administrators to use the same functionality that is available on other forms.

You can use client side scripts to:

-   Get or set variable values.
-   Hide or display variables.
-   Make variables mandatory or not.
-   Validate form submission.
-   Add something to the cart.
-   Order something immediately.

**Parent Topic:**[Client-side scripting](client-side-scripting-overview.md)

## Catalog client script considerations

When you create catalog client scripts, be aware of the following considerations.

-   Catalog client scripts run when a user orders an item from the service catalog. Catalog client scripts can also run when variables or variable sets for a catalog item are displayed when a user requests that item.
-   For a variable to be accessible using a catalog client script, it must have a variable name. Variables without names do not appear in the list of available variables.
-   When using standard client scripts on a Requested Item or Catalog Task form, make a note of fields with the same name as variables. If a table field and a variable of the same name are both present on a form, the table field is matched when it is accessed using a script. If this happens, specifically address the variable by naming it `variables.variable name`. For example: `g_form.setValue('variables.replacement', 'false');`
-   If you are using record producers to pass variables from the service catalog to other types of records, these variables are made visible in those records with a variable editor, such as the Change Variable Editor UI formatter on Change request forms. You can manipulate these variables using standard client script methods, such as `setDisplay`, `setMandatory`,`setValue`, and `getValue`.
-   Catalog client scripts can be used for catalog items included in a wizard.
-   You can use the `g_form.refreshSlushbucket(fieldName)` API to update a list collector variable.

## Catalog client script differences

Catalog client scripts are very similar to standard client scripts, with a few important differences.

-   Instead of selecting a table such as Incident for the script, select a catalog item or variable set. As your system may have a large number of catalog items, you should select a catalog item or variable set using a reference field instead of the choice list that the standard Client Script form uses.
-   When using an *onChange\(\)* catalog client script, it is linked to a particular variable instead of a field. The system automatically populates the variable name selection list with any named variables from the catalog item or variable set selected.

## Create a catalog client script

Follow this procedure to create a catalog client script.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Administration** &gt; **Catalog Client Scripts**.

    A list of current custom catalog client scripts appears.

2.  Click **New**.

3.  Fill in the fields, as appropriate \(see table\).

<table id="table_bw1_3g1_dq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a unique name for the catalog client script.

</td></tr><tr><td>

Applies to

</td><td>

Select the item type this client script applies to:-   **A Catalog Item**: enables the Catalog item field.
-   **A Variable Set**: enables the Variable set field.


</td></tr><tr><td>

Active

</td><td>

Select the check box to enable the client script. Clear the check box to disable the script.

</td></tr><tr><td>

UI Type

</td><td>

Whether to apply this to desktop, mobile, or both.

</td></tr><tr><td>

Script

</td><td>

Enter the client script that should run on the service catalog item.

</td></tr><tr><td>

Type

</td><td>

Select when the script should run, such as **onLoad** or **onSubmit**.

</td></tr><tr><td>

Catalog item or Variable set

</td><td>

Select a catalog item or variable set from the list. The field name and options available depend on the selection in the **Applies to** field.

</td></tr><tr><td>

Applies on a Catalog Item view

</td><td>

Select the check box to apply the catalog client script to catalog items displayed within the order screen on the service catalog. Available in the requester view.

</td></tr><tr><td>

Applies on Requested Items

</td><td>

Select the check box to apply the catalog client script on a Requested Item form, after the item is requested. Available in the fulfiller view. See [VEditor](https://www.servicenow.com/docs/access?context=service-catalog-variable-editor&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) .

</td></tr><tr><td>

Applies on Catalog Tasks

</td><td>

Select the check box to apply the catalog client script when a Catalog Task form for the item is being displayed. Available in the fulfiller view. See [VEditor](https://www.servicenow.com/docs/access?context=service-catalog-variable-editor&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) .

</td></tr><tr><td>

Applies on the Target Record

</td><td>

Select the check box to support the catalog UI policy on a record created for task-extended tables via record producers. See [Default variable editor](https://www.servicenow.com/docs/access?context=service-catalog-variable-editor&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) .

</td></tr></tbody>
</table>4.  Click **Submit**.


## Catalog client script examples

Examples of client scripts to perform common actions.

### Get the value of a variable

Use the following syntax to obtain the value of a catalog variable. Note that the variable must have a name. Replace `variable_name` with the name of the variable.

```
g_form.getValue('variable_name');
```

### Restrict the number of characters a user can type in a variable

This is an example of a script that runs when the variable is displayed, rather than when the item is ordered.

```
function onLoad(){
  var sd = g_form.getControl('short_description');
  sd.maxLength=80;
}
```

