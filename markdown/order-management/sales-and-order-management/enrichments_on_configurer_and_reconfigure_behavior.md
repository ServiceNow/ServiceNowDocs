---
title: Scripting: Checking for first and subsequent configurations
description: You can test whether a configuration is being initialized or being reconfigured, and set code to execute based on the result.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 4
breadcrumb: [Setting up enrichments and rules scripting, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Scripting: Checking for first and subsequent configurations

You can test whether a configuration is being initialized or being reconfigured, and set code to execute based on the result.

Sometimes it is necessary to execute code only when the configuration is being initialized, or only when it is being reconfigured. For example, you might want to set a field to its default values at the beginning of a configuration, but keep the userʼs selection during any future edit.

The methods below can be combined without interfering with one another and can lead to flexible and unique code behaviors for your configurable products.

## userEdited: running only when a field was not edited

Two field properties can be accessed in the On Configure/Reconfigure enrichment: **value** and **userEdited**. While the **value** property holds the data contained in the field and is usually what will be accessed when scripting, **userEdited** contains a Boolean value that stores whether the field has been changed by the end user.

This can be used in if statements to write a default value only when the field has not been changed by the user. For example:

```
if (cfgRequest.[fieldVariableName].userEdited == false) {
      //code to run
}
```

All fields will have the **userEdited** property set to false when the configuration is initialized, but when reconfiguring, some will be set to true based on the changes made by the user. If youʼd like a behavior to occur only when a field has or hasnʼt been edited, write the code to execute after one of these checks.

## The lineId partner field

Alternatively, if youʼd like to make only one check in the On Configure/Reconfigure enrichment script, and have Salesforce integration, the **lineId** partner field will only be populated with the Salesforce ID of the parent configurable productʼs quote line when reconfiguring. It will not be populated when a configuration is initialized.

This is because when a ServiceNow CPQ configuration is initialized, this ID does not yet exist, because the configuration has yet to be saved. Only after a ServiceNow CPQ configuration has been created and the quote line editor saved are any quote lines created in Salesforce. So, when we see that the **lineId** partner field is present, we can be sure that the current session is due to a reconfiguration, not a new configuration.

Script writers can take advantage of this distinction by putting any code that must be run only on initialization or reconfiguration under a check for this value.

Here is how the field can be referenced in the On Configure/Reconfigure enrichment:

```
cfgRequest.partner.quote.lineId.value;
```

If the behavior should only happen when the configuration is initialized, you could add the following check:

```
if (cfgRequest.partner.quote.lineId.value == null) {
      //code to run
      return cfgRequest;
}
```

Adding the `return cfgRequest;` line in the check guarantees that any code after the check for the line ID will not be executed.

Similarly, if the behavior should happen only when the configuration is reconfigured, add the inverse check:

```
if (cfgRequest.partner.quote.lineId.value != null) {      
      //code to run
      return cfgRequest;
}
```

For more information on partner fields, see [ServiceNow CPQ fields, system fields, and partner fields](system_fields_vs_partner_fields.md).

## isInitial: creating a text field

Another way to guarantee that a distinction is present \(regardless of whether Salesforce is used as an entry point into the configurator\) is to create a field that checks whether the current configuration is due to an initialization or a reconfiguration.

Create a text field with the variable name `isInitial`. Associate the field with your blueprint. Then, in the On Configure/Reconfigure enrichment, add the following lines:

```
if (cfgRequest.isInitial.value === "Yes" || cfgRequest.isInitial.value === "No") {
      cfgRequest.isInitial.set("value","No");
}
else
{
c fgRequest.isInitial.set("value","Yes");
}
```

On initialization, the `isInitial` field will be blank. Therefore, the script will set the value of `isInitial` to Yes in the `else` clause.

On the first reconfiguration, `isInitial` will be Yes. Therefore, the script will set the value of `isInitial` to No in the `if` clause.

On every subsequent reconfiguration, `isInitial` will be No, and will remain No.

This method has the added benefit of not having to save the entire QLE in SFDC in order to make the distinction between an initialization or reconfiguration. The method immediately detects when the user enters the configurator a second time.

This method also includes the ability to reference the new field as a condition in rules, such as making a rule fire specifically on initialization or reconfiguration. It does not require the behavior to exist only in the On Configure/Reconfigure script. However, to keep the configuring experience similar from the end user's perspective, you should be wary of making too many behavioral differences between initialization and reconfiguration.

