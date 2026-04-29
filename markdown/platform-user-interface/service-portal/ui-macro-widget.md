---
title: Replace a Service Catalog form script with a widget
description: You can use widgets in Service Portal to replace UI Macros. If your Service Catalog form includes a UI Macro that references other fields or variables on the form, you can create a widget to hold reusable code and embed it within the Service Catalog form. Use special syntax to access any variable fields on the form.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Replace a Service Catalog form script with a widget

You can use widgets in Service Portal to replace UI Macros. If your Service Catalog form includes a UI Macro that references other fields or variables on the form, you can create a widget to hold reusable code and embed it within the Service Catalog form. Use special syntax to access any variable fields on the form.

## Before you begin

Role required: admin or sp\_admin

## Procedure

1.  Create a widget that performs the action you would like to use in catalog item forms.

    See step 7 for a simple example widget that accesses another variable on the form.

2.  Open a catalog item that previously used a UI Macro or other reusable component not supported in Service Portal.

3.  In related lists, add a new variable to the catalog item.

4.  Configure the variable form to add the **Widget** field.

5.  In the **Type** field, select **Macro**.

6.  In the **Widget** field, select a widget that performs the desired action.

7.  Use the `$scope.page.g_form()` or `$scope.page.field` syntax in the embedded widget to access the catalog item values.

    This example shows how to modify the value of a single-line text variable with the name **color** associated with the catalog item.

    -   **Widget HTML Template**

        ```
        <div>  
          Data from catalog variable:  
          <h1>{{ c.data.message }}</h1>  
        </div>
        ```

    -   **Widget client script**

        ```
        function($scope) {  
             var c = this;  
          
             //Watch for changes in the color variable  
             $scope.$watch(function () {  
                  return $scope.page.g_form.getValue('color');  
             }, function (value) {  
             //Update local data object with data from variable  
             c.data.message = value ? 'Content of color variable: ' + value : '';  
        });  
        }  
        ```

    You can use the following to access variable or catalog item fields:

    -   `$scope.page.g_form()`: The g\_form instance on the form. You can use all supported g\_form methods described in [Service Portal and client scripts](../concept/unsupported_client_scripts.md). For example, `g_form.setValue('variable_name', 'new value');`.
    -   `$scope.page.field()`: The object that represents the variable.
    When you open the catalog item in the Service Portal, the embedded widget accesses the variable fields associated with the catalog item.

    ![The input to the variable displays in the embedded widget.](../image/macro-var.png)


**Parent Topic:**[Developing custom widgets](../concept/widget-dev-guide.md)

