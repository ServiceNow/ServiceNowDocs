---
title: ScopedSessionDomain - Client
description: The ScopedSessionDomain script include that contains client-side methods that provide functionality related to the current session domain.Returns the sys\_id of the current domain for the logged-in user session.
locale: en-US
release: yokohama
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# ScopedSessionDomain- Client

The ScopedSessionDomain script include that contains client-side methods that provide functionality related to the current session domain.

This API is only available if the Domain Support - Domain Extensions Installer plugin \(com.glide.domain.msp\_extensions\) plugin has been activated in the instance. In addition, the caller must have the admin role to access this API.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## ScopedSessionDomain - getCurrentDomainID\(\)

Returns the sys\_id of the current domain for the logged-in user session.

The identifier that is returned depends on the domain type and the instantiation of that domain.

-   If the user is configured in the global domain, and does not use the domain picker to switch domains, the method returns null.
-   If the user uses the domain picker to switch to the global domain, the method returns the string "global".
-   For all other domains, the method returns the sys\_id of that domain.

To access this method from a client-side script, you must use [GlideAjax\(\)](../../GlideAjax/concept/c_GlideAjaxAPI.md#) to invoke it. To invoke this method from a server-side script, use something similar to the following to instantiate the object and access the method.

```
var ssg = new global.ScopedSessionDomain(); 
domainID = ssg.getCurrentDomainID();
```

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the session domain of the current logged-in user. This is the same information that appears in the domain picker.|

This example shows how to call the getCurrentDomainID\(\) method from a client-side script.

```
// This example is calling the script include in a client script. 
// This particular record is within the "Service Portal - Standard Ticket" scope. 
// To reproduce this example: 
//  1. Change application scope to "Service Portal - Standard Ticket" 
//  2. Navigate to Client Script table and open a new form and name it anything 
//  3. Set table=ticket_configuration (this table is within the same scope) 
//  4. Set UI type=Desktop and Type=onLoad 
//  5. Populate the script field with the script above 
//  6. Navigate to the ticket_configuration table and open any form. 
//
// This will trigger the client script, invoke the API, and pop up a browser alert containing the sys_id of the user's current domain

function onLoad() {	
  var ga = new GlideAjax("global.ScopedSessionDomain"); // Set the script include
  ga.addParam("sysparm_name", "getCurrentDomainID"); // Set the getCurrentDomainID method
  ga.getXML(getResponse);
	
  function getResponse(response) {
     var answer = response.responseXML.documentElement.getAttribute('answer');
     alert(answer); // Pops up the sys_id of the domain record
  }
}
```

