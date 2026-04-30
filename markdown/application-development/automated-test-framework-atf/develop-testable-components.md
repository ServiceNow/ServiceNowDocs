---
title: Override component test actions
description: Change the testing properties of a particular page component using HTML attributes that are specific to Automated Test Framework. Use sn-atf-clickable and sn-atf-settable attributes to specify that an element and its child elements should be treated as a custom clickable or custom settable component.Use the sn-atf-class attribute to specify the JavaScript object to use when testing a custom clickable or settable component. Write a custom JavaScript object to specify the test actions available for a custom component.Use custom UI steps to manipulate the values of the sn-reference-picker and sn-record-picker angular directives. The value on a reference picker returns the sys\_id of the chosen record. The value on a record picker returns the value field chosen for that record picker. Both elements can be set by selecting a record to set as their value.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Custom UI test steps, UI test steps, Building and running automated tests with the Automated Test Framework, Automated Test Framework \(ATF\) test building and execution, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Override component test actions

Change the testing properties of a particular page component using HTML attributes that are specific to Automated Test Framework.

## Before you begin

Role required: admin

## About this task

When Automated Test Framework retrieves a component, it determines which interactions it supports, such as whether it is a settable or clickable component. If the component is settable, Automated Test Framework determines the field type that can be set. If Automated Test Framework incorrectly determines your custom component's actions or field types, or your component contains multiple DOM elements that should be treated as one entity, explicitly set them using HTML attributes that are specific to Automated Test Framework.

**Parent Topic:**[Custom UI test steps](../concept/custom-ui-test-steps.md)

## Using sn-atf-clickable and sn-atf-settable attributes

Use `sn-atf-clickable` and `sn-atf-settable` attributes to specify that an element and its child elements should be treated as a custom clickable or custom settable component.

### Before you begin

Role required: admin

### Procedure

1.  Open the custom UI page you would like to test.

2.  Add the `sn-atf-clickable` or `sn-atf-settable` attribute to the element being tested.

    ```
    <div sn-atf-clickable="true" sn-atf-disabled id="customClickable">
    	<button id="customButton">Click me</button>
    </div>
    ```

    ```
    <div sn-atf-settable="true" id="customSettable" sn-atf-component-value="A default value">
    	<input id="customInput" value="A default value"></input>
    </div>
    ```

    **Note:** You can use either `sn-atf-clickable` or `sn-atf-settable` attribute to specify if an element should be treated as a custom clickable or custom settable component. You can't use both attributes on the same element.

3.  Use either the `sn-atf-clickable` or `sn-atf-settable` attribute.

    -   `sn-atf-clickable`: If you added the `sn-atf-clickable` attribute, ATF clicks the component by sending an `sn-atf-click` event to the DOM element with the `sn-atf-clickable` attribute. You should add an event listener \(for example, using `addEventListener`\) to this DOM element, and implement your custom click logic for the component. You can interact with a custom clickable component using [Click Component](../reference/test-steps-custom-ui-category.md#) test step.

<table id="table_r5q_gry_cgb"><thead><tr><th>

Attribute name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn-atf-disabled

</td><td>

The presence of this optional attribute \(regardless of its value\) tells ATF that this component is disabled**Note:** If this attribute is missing, ATF considers that this component is enabled by default.

</td></tr><tr><td>

sn-atf-component-value

</td><td>

A string or JSON object that tells ATF the current value of this component

</td></tr></tbody>
</table>    -   `sn-atf-settable`: If you added the `sn-atf-settable` attribute, ATF sets the component value by sending an `sn-atf-setvalue` event to the DOM element with the `sn-atf-settable` attribute. You should add an event listener \(for example, using `addEventListener`\) to this DOM element, and implement your custom set value logic for the component. The value that needs to be set can be accessed with `event.detail.newvalue`. The `event` argument is passed to your event handler. You can interact with a custom settable component using [Set Component Values](../reference/test-steps-custom-ui-category.md#) test step.

<table id="table_kml_csy_cgb"><thead><tr><th>

Attribute name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn-atf-disabled

</td><td>

The presence of this optional attribute \(regardless of its value\) tells ATF that this component is disabled.**Note:** If this attribute is missing, ATF considers that this component is enabled by default.

</td></tr><tr><td>

sn-atf-component-value

</td><td>

A string or JSON object that tells ATF the current value of this component.

</td></tr><tr><td>

sn-atf-data-type

</td><td>

Optional type of field to present to user when building a step. It defaults to string. For example, `glide_date_time`, reference, boolean, etc.

</td></tr><tr><td>

sn-atf-data-type-params

</td><td>

JSON object with more data type details.

</td></tr></tbody>
</table>
### Example

```
//A custom clickable component

<div sn-atf-clickable="true" sn-atf-disabled id="customClickable">
	<button id="customButton">Click me</button>
</div>
<script>
	var customClickableDiv = document.getElementById("customClickable");
	customClickableDiv.addEventListener('sn-atf-click', function() {
		document.getElementById('customButton').click();
	});
</script>
```

```
//A custom settable component

<div sn-atf-settable="true" id="customSettable" sn-atf-component-value="A default value">
	<input id="customInput" value="A default value"></input>
</div>
<script>
	var customSettableDiv = document.getElementById("customSettable");
	customSettableDiv.addEventListener('sn-atf-setvalue', function(event) {
		var newValue = event.detail.newValue;
		document.getElementById("customInput").value = newValue;
	});
</script>
```

## Using sn-atf-class attribute

Use the `sn-atf-class` attribute to specify the JavaScript object to use when testing a custom clickable or settable component. Write a custom JavaScript object to specify the test actions available for a custom component.

### Before you begin

Role required: admin

### About this task

Test designers can manually specify the test actions available for a custom component by writing a custom JavaScript object and assigning the component a `sn-atf-class` attribute. Set the value of the attribute to the name of the JavaScript object containing the component test actions. Testable custom components must be either clickable or settable, and this classification determines the functions and properties your JavaScript object requires. See [Custom UI test steps](../concept/custom-ui-test-steps.md) for testable page component requirements.

### Procedure

1.  Open the custom UI page you would like to test.

2.  Add the `sn-atf-class` attribute to the element being tested and set the value to the name of the JavaScript object embedded in the page that handles getValue\(\), setValue\(\), click\(\), or isDisabled\(\) functions.

    ```
    <div sn-atf-class="MyClickableComponent">
        <label for="a_clickable_checkbox">MyClickableComponent</label>
        <input type="checkbox" id="a_clickable_checkbox" checked="true"/>
    </div>
    ```

3.  Create the JavaScript object specified in the `sn-atf-class` attribute and add the functions and attribute needed to identify your custom page component as either a clickable or settable page component.

<table id="table_r5q_gry_cgb"><thead><tr><th>

Function name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

initialize\(\)

</td><td>

Gets the initial values of the component. Enter:```
$super(element, area)
```

</td></tr><tr><td>

click\(\)

</td><td>

Selects the component. Returns a JSON object with these properties: `success`: true if the component can be clicked.

 **Note:** Triggers the UI test step intelligent wait mechanism.

</td></tr><tr><td>

getValue\(\)

</td><td>

Gets the value of the element. Returns a JSON object with these properties: -   `success`: true if the value is retrieved.
-   `result`: the value of the component.


</td></tr><tr><td>

isDisabled\(\)

</td><td>

Whether the component is disabled. Returns a JSON object with these properties:-   `success`: true if the component is disabled.
-   `result`: true if the component is disabled.


</td></tr></tbody>
</table><table id="table_kml_csy_cgb"><thead><tr><th>

Function name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

initialize\(\)

</td><td>

Gets the initial values of the component. Enter:```
$super(element, area)
```

</td></tr><tr><td>

setValue\(newValue\)

</td><td>

Sets the value of the component. See the second example below. Returns a JSON object with these properties:`success`: true if the value is set.

 **Note:** Triggers the UI test step intelligent wait mechanism.

</td></tr><tr><td>

getValue\(\)

</td><td>

Gets the value of the element. Returns a JSON object with these properties: -   `success`: true if the value is retrieved.
-   `result`: the value of the component.


</td></tr><tr><td>

isDisabled\(\)

</td><td>

Whether the component is disabled. Returns a JSON object with these properties:-   `success`: true if the component is disabled.
-   `result`: true if the component is disabled.


</td></tr></tbody>
</table>    |Attribute name|Description|
    |--------------|-----------|
    |isSettable: true|Identifies the component as a settable page component.|

4.  When creating your custom component in Jelly, add `<g2:atf_only>` tags around the JavaScript object specified in the `sn-atf-class` attribute.

    These tags ensure the system only runs the JavaScript object during automated testing.


### Example

```
//A custom clickable component

<form>
     <div sn-atf-class="MyClickableComponent">
         <label for="a_clickable_checkbox">MyClickableComponent</label>
         <input type="checkbox" id="a_clickable_checkbox" checked="true"/>
     </div>
</form>
<script>
var MyClickableComponent = {

    // The constructor must have this signature, but you can perform additional setup after the $super(element, area) call
    initialize: function($super, element, area) {
        $super(element, area);
    },

    click: function() {
        document.getElementById('a_clickable_checkbox').click();
        return {success: true};
    },

    // The function returns an object with a result attribute of type String
    getValue: function() {
        var isChecked = document.getElementById('a_clickable_checkbox').checked ? "true" : "false";
        return {success: true, result: isChecked};
    },

    // The function returns an object with a result attribute of type Boolean
    isDisabled: function() {
        if (document.getElementById('a_clickable_checkbox').disabled)
            return {success: true, result: true};

        return {success: true, result: false};
    },

};
</script>
```

```
//A custom settable component

<form>
    <div sn-atf-class="MySettableComponent">
        <label for="a_settable_checkbox">MySettableComponent</label>
        <input type="checkbox" id="a_settable_checkbox" checked="true"/>
    </div>
</form>
<script>
var MySettableComponent = {

    // This attribute is required for settable components
    isSettable: true,

    // The constructor must have this signature, but you can perform additional setup after the $super(element, area) call
    initialize: function($super, element, area) {
        $super(element, area);
    },

    // The value parameter is a string
    setValue: function(value) {
        document.getElementById('a_settable_checkbox').checked = (value == "true");
        return {success: true};
    },

    // The function returns an object with a result attribute of type String
    getValue: function() {
        var isChecked = document.getElementById('a_settable_checkbox').checked ? "true" : "false";
        return {success: true, result: isChecked};
    },

    // The function returns an object with a result attribute of type Boolean
    isDisabled: function() {
        if (document.getElementById('a_settable_checkbox').disabled)
            return {success: true, result: true};

        return {success: true, result: false};
    },

};
</script>
```

## Reference and record picker

Use custom UI steps to manipulate the values of the `sn-reference-picker` and `sn-record-picker` angular directives. The value on a reference picker returns the `sys_id` of the chosen record. The value on a record picker returns the value field chosen for that record picker. Both elements can be set by selecting a record to set as their value.

