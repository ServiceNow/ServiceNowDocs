---
title: m\_form - Client
description: Provides methods to get and set input values on input form screens, as well as display messages.Displays an error message at the top of the input form screen.Displays an informational message at the top of the input form screen.Returns the value of a specified input on an input form screen.Adds a shimmering effect to specified inputs indicating that the value is being set by a script.Sets the value of a specified input on an input form screen.
locale: en-US
release: xanadu
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# m\_form- Client

Provides methods to get and set input values on input form screens, as well as display messages.

This API supports the following input types:

-   Boolean
-   Choice
-   Date/time
-   Number
-   Reference
-   String

This API can be used with the [MobileScriptIncludeCaller - Client](../../MobileScriptIncludeCaller/concept/MobileScriptInclCallerClientAPI.md#) API to auto-fill inputs on input form screens. For more information about input form screens, see [Input form screen](https://www.servicenow.com/docs/access?context=parameter-input-screen&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

Use this API in the **Client script** field of a Mobile UI Rule Action. For instructions on configuring a Mobile UI Rule Action with the correct settings for this API, see [Configure auto-fill inputs on input form screens](https://www.servicenow.com/docs/access?context=config-autofil-inputs-nptfrmscrn&version=xanadu&pubname=xanadu-mobile&ft:locale=en-US).

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## m\_form - addErrorMessage\(String message\)

Displays an error message at the top of the input form screen.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to display.|

|Type|Description|
|----|-----------|
|None| |

In this example, an informational or error message is displayed on the form depending on the value entered for the priority.

```
// Client script in a Mobile UI Rule Action
function onChange(inputName, newValue) { 
   var priority = newValue; 
   if (priority > 0 && priority < 3) { 
      getMessage("This incident should be handled ASAP", function(response){ 
         m_form.addInfoMessage(response); 
      }); 
   } else { 
      getMessage("The selected priority is invalid", function(response){ 
         m_form.addErrorMessage(response); 
      }); 
   }	 
}
```

## m\_form - addInfoMessage\(String message\)

Displays an informational message at the top of the input form screen.

|Name|Type|Description|
|----|----|-----------|
|message|String|The message to display.|

|Type|Description|
|----|-----------|
|None| |

In this example, an informational or error message is displayed on the form depending on the value entered for the priority.

```
// Client script in a Mobile UI Rule Action
function onChange(inputName, newValue) { 
   var priority = newValue; 
   if (priority > 0 && priority < 3) { 
      getMessage("This incident should be handled ASAP", function(response){ 
         m_form.addInfoMessage(response); 
      }); 
   } else { 
      getMessage("The selected priority is invalid", function(response){ 
         m_form.addErrorMessage(response); 
      }); 
   }	 
}
```

## m\_form - getValue\(String inputName\)

Returns the value of a specified input on an input form screen.

|Name|Type|Description|
|----|----|-----------|
|inputName|String|Name of the input to return the value of.|

<table id="table_mpp_tr2_mbc" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

String

</td><td>

The value of the specified input.**Note:** If the input is a choice list with multi-select, the return type is an array of strings containing the selected values.

</td></tr></tbody>
</table>This client script passes the employee\_id input value to the script include, which uses the ID to look up the employee's title. The title is provided to the callback function, which it uses to auto-fill the business\_title input on the input form screen.

```
// Client script in a Mobile UI Rule Action
function onChange(inputName, newValue) { 
   var employeeId = m_form.getValue("employee_id"); 
   var caller = new MobileScriptIncludeCaller("UserUtilsTest", "getBusinessTitle"); 
   caller.addParam("employeeId", employeeId); 
   caller.call(function(response) { 
      m_form.setValue("business_title", response); 
   }); 
}
```

Script include.

```
// Mobile callable script include
var UserUtilsTest = Class.create(); 
UserUtilsTest.prototype = Object.extendsObject(global.AbstractMobileCallableInclude, { 
   getBusinessTitle: function() { 
      var employeeId = this.getParameter("employeeId"); 
      var gr = new GlideRecord("sys_user"); 
      gr.get(employeeId); 
      return gr.getValue("title"); 
   }, 
   type: 'UserUtilsTest' 
});
```

## m\_form - setAffectedInputs\(Array inputNames\)

Adds a shimmering effect to specified inputs indicating that the value is being set by a script.

The shimmering effect ends once the value for the input is set.

|Name|Type|Description|
|----|----|-----------|
|inputNames|Array|Array of strings containing the names of inputs to apply the shimmer effect to.|

|Type|Description|
|----|-----------|
|None| |

This client script adds a shimmer effect to the caller input to indicate that it's auto-filled.

```
// Client script in a Mobile UI Rule Action
function onChange(inputName, newValue) { 
   var affectedInputs = []; 
   affectedInputs.push("Caller"); 
   m_form.setAffectedInputs(affectedInputs); 
   m_form.setValue("Caller", ["800b174138d089c868d09de320f9833b", "46d44a23a9fe19810012d100cca80666"]); 
   var result = m_form.getValue("Caller"); 
   console.log(`Ref test: ${result[0]}`); 
}
```

## m\_form - setValue\(String inputName, Object value, String displayValue\)

Sets the value of a specified input on an input form screen.

<table id="table_tp1_wr2_mbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

inputName

</td><td>

String

</td><td>

Name of the input to set the value of.

</td></tr><tr><td>

value

</td><td>

Object

</td><td>

Value to set the input to.The data type of the value varies based on the input being set.

</td></tr><tr><td>

displayValue

</td><td>

String

</td><td>

Optional. Use this parameter when setting the value of Reference type inputs.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example sets an integer value for the order input.

```
m_form.setValue("order", 5);
```

This example sets a string value for the description input.

```
m_form.setValue("description", "This is the description content");
```

This example uses an object containing the value and display value to set a reference type input.

```
m_form.setValue("Caller", [{"value":"800b174138d089c868d09de320f9833b", "displayValue":"Abel Tuter"}]);
```

