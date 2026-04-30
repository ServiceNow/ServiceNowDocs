---
title: MobileScriptIncludeCaller - Client
description: Provides methods to call script includes from Mobile UI Rule Actions.Creates an instance of the MobileScriptIncludeCaller class with the script include and function to call.Adds a parameter to pass when calling the script include.Calls the script include specified by the constructor.
locale: en-US
release: zurich
product: Cllent Mobile API Reference
classification: cllent-mobile-api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Client mobile API reference, API reference, API implementation and reference]
---

# MobileScriptIncludeCaller- Client

Provides methods to call script includes from Mobile UI Rule Actions.

This API can be used with the [m\_form - Client](../../m_form/concept/m_formClientAPI.md#) API to auto-fill inputs on input form screens. For more information about input form screens, see [Input form screen](https://www.servicenow.com/docs/access?context=parameter-input-screen&version=zurich&pubname=zurich-mobile&ft:locale=en-US).

Use this API in the **Client script** field of a Mobile UI Rule Action. For instructions on configuring a Mobile UI Rule Action with the correct settings for this API, see [Configure auto-fill inputs on input form screens](https://www.servicenow.com/docs/access?context=config-autofil-inputs-nptfrmscrn&version=zurich&pubname=zurich-mobile&ft:locale=en-US).

The script include must have the **Mobile callable** field selected to be called by this API.

**Parent Topic:**[Client mobile API reference](../../../../../build/applications/concept/api-client-mobile.md)

## MobileScriptIncludeCaller - MobileScriptIncludeCaller\(String scriptName, String functionName\)

Creates an instance of the MobileScriptIncludeCaller class with the script include and function to call.

<table id="table_umw_wlk_mbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

scriptName

</td><td>

String

</td><td>

Name of the mobile-callable script include to call.If the script include supports cross-scope access and it's in a different scope than the client script, the name of the script include must be prefixed with the scope.

</td></tr><tr><td>

functionName

</td><td>

String

</td><td>

The public function to call in the script include.

</td></tr></tbody>
</table>This example shows how to create an instance of the MobileScriptIncludeCaller class that can be used to call the `getBusinessTitle()` function in the UserUtilsTest script include.

```
var caller = new MobileScriptIncludeCaller("UserUtilsTest", "getBusinessTitle");
```

## MobileScriptIncludeCaller - addParam\(String key, Object value\)

Adds a parameter to pass when calling the script include.

This method enables you to pass values from the input form to the script include.

|Name|Type|Description|
|----|----|-----------|
|key|String|Key to use for the parameter.|
|value|Object|Value of the parameter.|

|Type|Description|
|----|-----------|
|None| |

This example shows how to add the value of the employee\_id input from the input form to the MobileScriptIncludeCaller object.

```
var employeeId = m_form.getValue("employee_id"); 
var caller = new MobileScriptIncludeCaller("UserUtilsTest", "getBusinessTitle"); 
caller.addParam("employeeId", employeeId);
```

## MobileScriptIncludeCaller - call\(Function successCallback, Function errorCallback\)

Calls the script include specified by the constructor.

The server call executes asynchronously and the script include's response is passed to the callback function. If the response from the server fails, for example if the script include isn’t found, the response argument passed to the callback is empty or null.

The script include must have the **Mobile callable** field selected to be called by this method.

<table id="table_es1_b5l_mbc" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

successCallback

</td><td>

Function

</td><td>

Optional. The name of the callback function to process the results returned by the server.If a callback function isn’t provided, this method returns a promise, which can be consumed using the [Promise API](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise).

</td></tr><tr><td>

errorCallback

</td><td>

Function

</td><td>

Optional. The name of the callback function to call if an error occurs.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This client script passes the employee\_id input value to the script include, which uses the ID to look up the employee's title. The title is provided to the callback function, which it uses to auto-fill the business\_title input on the input form screen.

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

