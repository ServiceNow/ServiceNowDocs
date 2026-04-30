---
title: GlideAjax - Client
description: The GlideAjax class enables a client script to call server-side code in a script include.Constructor for GlideAjax.Specifies a parameter name and value to be passed to the server-side function associated with this GlideAjax object.Retrieves the results from a server-side method called from the client via getXMLWait\(\).Calls the processor asynchronously and gets the answer element of the response in XML format.Sends the server a request to execute the method and parameters associated with this GlideAjax object.Sends the server a request to execute the method and parameters associated with this GlideAjax object.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# GlideAjax- Client

The GlideAjax class enables a client script to call server-side code in a script include.

To use GlideAjax in a client script, follow these general steps.

1.  Create a GlideAjax instance by calling the GlideAjax constructor. As the argument to the constructor, specify the name of the script include class that contains the method you want to call.
2.  Call the addParam method with the **sysparm\_name** parameter and the name of the script-include method you want to call.
3.  Optional. Call the addParam method one or more times to provide the script-include code with other parameters it needs.
4.  Execute the server-side code by calling getXML\(\).

    **Note:** getXML\(\) is the preferred method for executing the code, because it is asynchronous and does not hold up the execution of other client code. Another method, getXMLWait\(\), is also available but is not recommended. Using getXMLWait\(\) ensures the order of execution, but can cause the application to seem unresponsive, significantly degrading the user experience of any application that uses it. getXMLWait\(\) is not available to scoped applications.


```
var ga = new GlideAjax('HelloWorld'); // HelloWorld is the script include class 
ga.addParam('sysparm_name','helloWorld'); // helloWorld is the script include method 
ga.addParam('sysparm_user_name',"Bob"); // Set parameter sysparm_user_name to 'Bob' 
ga.getXML(HelloWorldParse);  /* Call HelloWorld.helloWorld() with the parameter sysparm_user_name set to 'Bob' 
      and use the callback function HelloWorldParse() to return the result when ready */

// the callback function for returning the result from the server-side code
function HelloWorldParse(response) {  
   var answer = response.responseXML.documentElement.getAttribute("answer"); 
    alert(answer);
}
```

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## GlideAjax - GlideAjax\(String class\_name\)

Constructor for GlideAjax.

|Name|Type|Description|
|----|----|-----------|
|class\_name|String|The name of the server-side class that contains the method you want to execute.|

In this example, a client script sets the user to Fred Luddy and then calls a script include to get their manager.

```
// client script – contains onLoad function and a callback function

function onLoad() {
   var ga = new GlideAjax('GetUserInfo'); // GetUserInfo is the script include name 
   ga.addParam('sysparm_name','managerName'); // managerName is the function in the script include that we're calling 
   ga.addParam('sysparm_user_name','fred.luddy'); // set user to Fred Luddy 

   /* Call GetUserInfo.managerName() with user set to Fred Luddy and use the callback function ManagerParse() to return the result when ready */
   ga.getXMLAnswer(ManagerParse);  		
}

// callback function for returning the result from the script include
function ManagerParse(response) {  
   alert(response);
}


// GetUserInfo script include 

var GetUserInfo = Class.create();
GetUserInfo.prototype = Object.extendsObject(global.AbstractAjaxProcessor, {

    managerName: function() {
        var userName = this.getParameter("sysparm_user_name");
        var grUser = new GlideRecord('sys_user');
        grUser.get("user_name", userName);

        // Build the payload. You can return additional data if needed. 
        var result = {    
           "manager": grUser.getDisplayValue('manager')
        }; 
        return JSON.stringify(result);
    },
    type: 'GetUserInfo'
});

```

## GlideAjax - addParam\(String parm\_name, String parm\_value\)

Specifies a parameter name and value to be passed to the server-side function associated with this GlideAjax object.

You can execute addParam multiple times with different parameters and values.

**Note:** The first call to addParam should be with the parameter **sysparm\_name** and the name of the server-side method you want to call. The server-side code does not execute until the client script calls getXML\(\) or getXMLAnswer\(\).

|Name|Type|Description|
|----|----|-----------|
|parm\_name|String|The name of the parameter to pass. \(The name must begin with the `sysparm_` .\)|
|parm\_value|String|The value to assign to **parm\_name**.|

|Type|Description|
|----|-----------|
|void| |

In this example, a client script sets the user to Fred Luddy and then calls a script include to get their manager.

```
// client script – contains onLoad function and a callback function

function onLoad() {
   var ga = new GlideAjax('GetUserInfo'); // GetUserInfo is the script include name 
   ga.addParam('sysparm_name','managerName'); // managerName is the function in the script include that we're calling 
   ga.addParam('sysparm_user_name','fred.luddy'); // set user to Fred Luddy 

   /* Call GetUserInfo.managerName() with user set to Fred Luddy and use the callback function ManagerParse() to return the result when ready */
   ga.getXMLAnswer(ManagerParse);  		
}

// callback function for returning the result from the script include
function ManagerParse(response) {  
   alert(response);
}


// GetUserInfo script include 

var GetUserInfo = Class.create();
GetUserInfo.prototype = Object.extendsObject(global.AbstractAjaxProcessor, {

    managerName: function() {
        var userName = this.getParameter("sysparm_user_name");
        var grUser = new GlideRecord('sys_user');
        grUser.get("user_name", userName);

        // Build the payload. You can return additional data if needed. 
        var result = {    
           "manager": grUser.getDisplayValue('manager')
        }; 
        return JSON.stringify(result);
    },
    type: 'GetUserInfo'
});

```

## GlideAjax - getAnswer\(\)

Retrieves the results from a server-side method called from the client via getXMLWait\(\).

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|void|The result returned by the server-side method previously called with getXMLWait\(\).|

## GlideAjax - getXMLAnswer\(Function callback, Object additionalParam, Object responseParam\)

Calls the processor asynchronously and gets the answer element of the response in XML format.

|Name|Type|Description|
|----|----|-----------|
|callback|Function|Callback function. The function receives the answer element of the response in XML format as an argument.|
|additionalParam|Object|Optional. Name-value pair of additional parameters.|
|responseParam|Object|Optional. Second argument for the callback function.|

|Type|Description|
|----|-----------|
|void| |

This example retrieves the number of attachments for a given sysid using GlideAjax and updates the UI with the count. It also passes an additional parameter \(for example, a timestamp\) to the callback function, which can be used for debugging or tracking when the request was made.

```
function updateAttachmentCount(sysid) {
  var ga = new GlideAjax('AttachmentAjax');
  ga.addParam('sysparm_type', 'attachmentCount');
  ga.addParam('sysparm_value', sysid);

  // Adding an additional parameter object
  var additionalParam = { timestamp: new Date().toISOString() };

  ga.getXMLAnswer(numberOfAttachments, additionalParam, sysid); 
}

function numberOfAttachments(answer, additionalParam, sysid) {
  var number = parseInt(answer);

  console.log('Additional Param:', additionalParam); // Debugging
  console.log('Timestamp:', additionalParam?.timestamp); // Example usage

  var buttons = $$('.attachmentNumber_' + sysid);
  if (buttons[0] == undefined)
    $('header_attachment_list_label').down().innerHTML = number;
  else {
    for (var i = 0; i < buttons.length; i++) {
      buttons[i].innerHTML = number;
    }
  }
}
```

## GlideAjax - getXML\(Function callback\)

Sends the server a request to execute the method and parameters associated with this GlideAjax object.

The server processes the request asynchronously and -- when ready -- returns the results via the function specified as the **callback\_function**.

|Name|Type|Description|
|----|----|-----------|
|callback|Function|The name of the callback function to process the results returned by the server.|

|Type|Description|
|----|-----------|
|void| |

```
var comments = gel("dialog_comments").value;
var ga = new GlideAjax('validateComments'); //Call script include to escape text
ga.addParam('sysparm_name', 'validateComments');
ga.addParam('sysparm_comments', comments);
ga.getXML(callback);
 
return false;
 
function callback(response) {
  var comments = response.responseXML.documentElement.getAttribute("answer");
  comments = trim(comments);
  if (comments == "") {
     //If comments are empty, alert the user and stop submission
     alert("Please enter your comments before submitting.");
  } else {
    //If there are comments, close the dialog window and submit them
    GlideDialogWindow.get().destroy(); //Close the dialog window
    g_form.setValue("comments", comments); //Set the "Comments" field with comments in the dialog
  }
```

## GlideAjax - getXMLWait\(\)

Sends the server a request to execute the method and parameters associated with this GlideAjax object.

The server processes the request synchronously and will not process further requests from the client until finished. To retrieve the results, the client must call getAnswer\(\). Using getXMLWait\(\) ensures the order of execution, but can cause the application to seem unresponsive, significantly degrading the user experience of any application that uses it. We recommend usinggetXML\(\) instead.

**Note:** getXMLWait\(\) is not available to scoped applications.

|Name|Type|Description|
|----|----|-----------|
|none| | |

|Type|Description|
|----|-----------|
|void| |

```
var ga = new GlideAjax('HelloWorld');
      ga.addParam('sysparm_name','helloWorld');
      ga.addParam('sysparm_user_name',"Bob");
      ga.getXMLWait();
      alert(ga.getAnswer());
```

