---
title: Cascade an order guide variable
description: Cascading enables values entered for variables in the initial order form to be passed to the equivalent variables in the ordered catalog items.You can use a variable set with an order guide.You can hide the duplicated variables on the Choose Options screens to keep your screen clean.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create an order guide variable, Order guides, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Cascade an order guide variable

Cascading enables values entered for variables in the initial order form to be passed to the equivalent variables in the ordered catalog items.

Cascading allows values entered for variables in the initial order form to be passed to the equivalent variables in the ordered catalog items. For example, a variable on the initial order form prompts the customer to enter a delivery location value. If you enable cascading, the value for this variable then populates delivery location fields on each of the ordered items.

To enable cascading, select the **Cascade variables** check box when creating the order guide. Then, create variables on the catalog items that match the names of the corresponding variables in the order guide. When a customer places an order, the variables on the ordered items inherit the values of the identically named variables in the order guide.

**Parent Topic:**[Create an order guide variable](c_CreateVariables.md)

## Use a variable set

You can use a variable set with an order guide.

### Before you begin

Role required: admin

### About this task

Cascading variables require that the same variable be on both the order guide and the ordered items. It can be useful to define each variable once in a variable set, then assign the variable set to both the order guide and the individual catalog item. This approach avoids duplication and ensures that the variable is the same in both locations.

To use a variable set with an order guide:

### Procedure

1.  Create the variable set.

2.  In the Variable Set form, create each variable.

3.  Add the variable set to the order guide and to each catalog item involved.

    **Note:** The individual variables in a variable set do not appear in the Order guide or Catalog Item forms. To view the variables in a variable set, open the variable set record.


## Hide cascaded variables

You can hide the duplicated variables on the **Choose Options** screens to keep your screen clean.

When cascading variables, you can hide the duplicated variables on the Choose Options screens, making these screens simpler.

To hide duplicate variables on all screens after the initial Describe Needs screen in the Service Catalog Platform UI, run an **onLoad catalog client** script.

```
function onLoad(){
  var item = g_form.getControl("current_item");
  var guide = g_form.getControl("sysparm_guide");

  if (item == null && guide == null )
		return;

  if(item != null && guide != null && item.value == guide.value)
    return;
  g_form.setDisplay('YOUR_VARIABLE_NAME',false);
}
```

To hide duplicate variables on all screens after the initial Describe Needs screen in Service Portal, use the isOrderGuide\(\) method.

```
if(g_service_catalog.isOrderGuide()) 
  g_form.setDisplay(‘variable_name’, false);
```

