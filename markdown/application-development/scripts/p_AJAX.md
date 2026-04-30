---
title: AJAX
description: AJAX \(asynchronous JavaScript and XML\) is a group of interrelated, client-side development techniques used to create asynchronous Web applications.The GlideAjax class allows the execution of server-side code from the client. GlideAjax calls pass parameters to the script includes, and, using naming conventions, allows the use of these parameters.There are two parts to the asynchronous GlideAjax script: client-side and server-side code.Use synchronous when your script cannot continue without the GlideAjax response. This stops the session until the response is received.Provides helper functions for Ajax clients to retrieve a value from an Ajax client.
locale: en-US
release: xanadu
product: Scripts
classification: scripts
topic_type: topic
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Client-side scripting, Scripting, Building pro-code applications, Developing your application, Building applications]
---

# AJAX

AJAX \(asynchronous JavaScript and XML\) is a group of interrelated, client-side development techniques used to create asynchronous Web applications.

AJAX enables web applications to send and retrieve information to and from a server in the background, without impacting the user experience with the displayed web page.

**Parent Topic:**[Client-side scripting](../../client-scripts/concept/client-side-scripting-overview.md)

## GlideAjax

The GlideAjax class allows the execution of server-side code from the client. GlideAjax calls pass parameters to the script includes, and, using naming conventions, allows the use of these parameters.

**Note:** This functionality requires a knowledge of JavaScript.

Using GlideAjax:

-   Initialize GlideAjax with the name of the script include that you want to use.
-   When creating the script include, you must set the name field to be exactly the same as the class name.
-   When creating the script include, you must select the **Client callable** check box.
-   Specify the parameter **sysparm\_name**. GlideAjax uses**sysparm\_name** to find which function to use.
-   Any extra parameters may be passed in, all of which must begin with **sysparm\_**. Avoid using predefined parameter names:
    -   **sysparm\_name**
    -   **sysparm\_function**
    -   **sysparm\_value**
    -   **sysparm\_type**
-   Code is then executed with the getXML\(\) or getXMLWait\(\) functions.

For additional information, refer to the [GlideAjax](https://www.servicenow.com/docs/access?context=c_GlideAjaxAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US) API.

## Examples of asynchronous GlideAjax

There are two parts to the asynchronous GlideAjax script: client-side and server-side code.

### Hello World: Returning a value from the server

### Client side

This code runs on the client \(the web browser\). Create a client script as normal. This sends the parameters to server, which then does the processing. So that the client does not wait for the result, a callback function is used to return the result, passed to the getXML\(\) function. \(In this case it is called `HelloWorldParse`.\)

The getXMLWait\(\) function does not need a separate callback function, but this will block the client. If the client-server communication takes a long time \(for example on slow networks\), the application will seem unresponsive and slow. An example of getXMLWait\(\) is in the following section.

```
var ga = new GlideAjax('HelloWorld');
ga.addParam('sysparm_name', 'helloWorld');
ga.addParam('sysparm_user_name', "Bob");
ga.getXML(HelloWorldParse);
 
function HelloWorldParse(response) {
  var answer = response.responseXML.documentElement.getAttribute("answer");
  alert(answer); }
```

### Server side

The server-side code for the above function. Do not create a business rule, but instead navigate to **System Definition &gt; Script Include** and create a new script. Paste in the code below.

**Note:** You must set the name of the script include to `HelloWorld`.

-   The sys\_script\_include code must extend the AbstractAjaxProcessor class and be Glide AJAX enabled.
-   Function names starting with "\_" are considered private and are not callable from the client.
-   Avoid overriding methods of AbstractAjaxProcessor, including `initialize`. While it is possible to invoke methods of your superclass object which you have overridden, it is complicated and best avoided altogether.

```
var HelloWorld = Class.create();
HelloWorld.prototype = Object.extendsObject(AbstractAjaxProcessor, {
   helloWorld:function() { return "Hello " + this.getParameter('sysparm_user_name') + "!"; } ,
   _privateFunction: function() { // this function is not client callable     
    }
 });
```

This results in an alert box that says 'Hello Bob!' when you visit the form.

### Returning multiple values

Since the response is an XML document we are not limited to returning a single `answer` value. Here is a more complex example returning multiple XML nodes and attributes.

### AJAX processor script include

```
/*
 * MyFavoritesAjax script include Description - sample AJAX processor returning multiple value pairs
 */ 
var MyFavoritesAjax = Class.create();
MyFavoritesAjax.prototype = Object.extendsObject(AbstractAjaxProcessor, {
 
	 /*
	 * method available to client scripts call using:
	 * var gajax = new GlideAjax("MyFavoritesAjax");
	 * gajax.addParam("sysparm_name","getFavorites");
	 */
	getFavorites: function() { // build new response xml element for result
         var result = this.newItem("result");
	  result.setAttribute("message","returning all favorites");
 
	  //add some favorite nodes with name and value attributes 
         this._addFavorite("color","blue");
         this._addFavorite("beer","lager");
         this._addFavorite("pet","dog");
       },
	 // all items are returned to the client through the inherited methods of AbstractAjaxProcessor
	 _addFavorite: function(name, value) { 
          var favs = this.newItem("favorite");
	   favs.setAttribute("name",name);
	   favs.setAttribute("value",value); },
 
	type:"MyFavoritesAjax"
 
 });
```

### Client script

```
// new GlideAjax object referencing name of AJAX script include 
var ga = new GlideAjax("MyFavoritesAjax"); 
// add name parameter to define which function we want to call 
// method name in script include will be getFavorites
ga.addParam("sysparm_name","getFavorites");
 
// submit request to server, call ajaxResponse function with server response
 
ga.getXML(ajaxResponse);
 
function ajaxResponse(serverResponse) { 
  // get result element and attributes
  var result = serverResponse.responseXML.getElementsByTagName("result");
  var message = result[0].getAttribute("message");
 
  //check for message attribute and alert user
  if(message) alert(message);
 
  //build output to display on client for testing 
  var output = "";
 
  // get favorite elements 
  var favorites = serverResponse.responseXML.getElementsByTagName("favorite");
  for(var i = 0; i < favorites.length; i ++) { 
    var name = favorites[i].getAttribute("name");
    var value = favorites[i].getAttribute("value");
    output += name + " = " + value + "\n "; }
 
  alert(output); }
```

### XML response

```
<xml sysparm_max= "15" sysparm_name="getFavorites" sysparm_processor="MyFavoritesAjax">
  <result message = "returning all favorites"></result>
  <favorite name = "color" value = "blue"></favorite>
  <favorite name = "beer" value = "lager"></favorite>
  <favorite name = "pet" value = "dog"></favorite>
</xml>
```

## Examples of synchronous GlideAjax

Use synchronous when your script cannot continue without the GlideAjax response. This stops the session until the response is received.

If your use case demands that no further processing can occur until the GlideAjax response has been received, you can use getXMLWait\(\). However, because this will slow down your code and lock the user session until the response is received, it is generally recommended that you use getXML\(\) with a callback function.

**Note:** Do not use AJAXEvaluateSynchronously.

The getXMLWait\(\) method is not available in scoped applications.

This code results in a client-side alert that displays `The Server Says Hello Bob!`.

The client code.

```
var ga = new GlideAjax('HelloWorld') ;
ga.addParam('sysparm_name','helloWorld');
ga.addParam('sysparm_user_name',"Bob");
ga.getXMLWait(); 
alert(ga.getAnswer());
```

The server-side script include code.

```
var HelloWorld = Class.create();
HelloWorld.prototype = Object.extendsObject(AbstractAjaxProcessor, {
helloWorld: function() 
 { return "The Server Says Hello " + this.getParameter('sysparm_user_name') + "!"; } } );
```

## AJAXClientHelper

Provides helper functions for Ajax clients to retrieve a value from an Ajax client.

### Where to use

Use this script include wherever your need to retrieve a value from an Ajax client.

### Method summary

|Method summary|Description|
|--------------|-----------|
|getDisplay\(\)|Gets the display value from the choice list.|

### Method detail

|API method|Description|Input parameters|Output returns|
|----------|-----------|----------------|--------------|
|getDisplay\(\)|Gets the display value from the choice list.|none|The display value.|

### Curl

```
// getDisplay
(function(table, sysId) {
    var ga = new GlideAjax('AjaxClientHelper');
    ga.addParam("sysparm_name", "getDisplay");
    ga.addParam('sysparm_table', 'incident');
    ga.addParam('sysparm_value', "0598b22b877313003c1c8467a7cb0b71");
    ga.getXMLWait();
    return ga.getAnswer();
}("incident", "0598b22b877313003c1c8467a7cb0b71")); // Returns 'INC0010001'
```

