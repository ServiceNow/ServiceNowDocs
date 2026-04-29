---
title: GlideSession - Scoped
description: The scoped GlideSession API provides methods to find information about the current session.Retrieves a session client value previously set with putClientData\(\).Returns the client IP address.Returns the application currently selected in the application picker.Returns the sys\_id of the current domain for the logged-in user session.Returns the session's language code.Returns the session token.Returns the name of the session's time zone.Returns the URL on the stack. Returns null if the stack is empty.Returns true if the user is impersonating another user.Returns true if the session is interactive.Returns true if the user is logged in.Sets a session client value that can be retrieved with getClientData\(\). This method is used in a server side script that runs when a form is created.
locale: en-US
release: australia
product: Server API Reference
classification: server-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Server API reference, API reference, API implementation and reference]
---

# GlideSession- Scoped

The scoped GlideSession API provides methods to find information about the current session.

There are no constructors for creating an instance of a scoped GlideSession object. Instead, use the getSession\(\) method of the scoped GlideSystem API.

**Parent Topic:**[Server API reference](../../../../../build/applications/concept/api-server.md)

## Scoped GlideSession - getClientData\(String paramName\)

Retrieves a session client value previously set with putClientData\(\).

Use this method to retrieve data values that were set using the putClientData\(\) method.

|Name|Type|Description|
|----|----|-----------|
|paramName|String|Name of the client data to retrieve.|

|Type|Description|
|----|-----------|
|String|Client data.|

```
var session = gs.getSession();
session.putClientData('test1', 'Harry');
var clientData = session.getClientData('test1');
gs.info(clientData);
```

Output:

```
Harry
```

## Scoped GlideSession - getClientIP\(\)

Returns the client IP address.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|IP address.|

```
var session = gs.getSession();
var addr = session.getClientIP();
gs.info(addr);
```

Output:

```
50.59.164.97
```

## Scoped GlideSession - getCurrentApplicationId\(\)

Returns the application currently selected in the application picker.

This method requires admin privileges.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Currently selected application.|

```
var session = gs.getSession();
var appID = session.getCurrentApplicationId();
gs.info(appID);
```

Output:

```
ce05b9f32b840200c5244f74b4da1501
```

## Scoped GlideSession - getCurrentDomainID\(\)

Returns the sys\_id of the current domain for the logged-in user session.

The identifier that is returned depends on the domain type and the instantiation of that domain.

-   If the user is configured in the global domain, and does not use the domain picker to switch domains, the method returns null.
-   If the user uses the domain picker to switch to the global domain, the method returns the string "global".
-   For all other domains, the method returns the sys\_id of that domain.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Sys\_id of the session domain of the current logged-in user. This is the same information that appears in the domain picker.|

This example shows the current sys\_email record's domain being set to the user's session domain, if the user domain is global or null.

```
// Set domain based on parent record's domain
setDomain();

// If the domain is global, set to user's domain
if (current.sys_domain == 'global' || current.sys_domain.nil())
   current.sys_domain = gs.getSession().getCurrentDomainID();

function setDomain() {
   if (current.target_table.nil())
      return;

   var d = new GlideRecord(current.target_table);
   if (!d.isValid())
      return;

   if (!d.get('sys_id', current.instance))
      return;

   if (typeof(d.sys_domain) == 'object')
      current.sys_domain = d.sys_domain;

```

## Scoped GlideSession - getLanguage\(\)

Returns the session's language code.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Session's language code.|

```
var session = gs.getSession();
var language = session.getLanguage();
gs.info(language);
```

Output:

```
en
```

## Scoped GlideSession - getSessionToken\(\)

Returns the session token.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Session token.|

```
var session = gs.getSession();
var token = session.getSessionToken();
gs.info(token);
```

Output:

```
4284b5372b840200c5244f74b4da15f2c3476cf7fcb6572afa4ef9d5e6d307a5fd9e1da7
```

## Scoped GlideSession - getTimeZoneName\(\)

Returns the name of the session's time zone.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|Name of the session's time zone.|

```
var session = gs.getSession();
var zoneName = session.getTimeZoneName();
gs.info(zoneName);
```

Output:

```
US/Pacific
```

## Scoped GlideSession - getUrlOnStack\(\)

Returns the URL on the stack. Returns null if the stack is empty.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|String|URL on the stack. Returns null if the stack is empty.|

```
var session = gs.getSession();
var URL = session.getUrlOnStack();
gs.info(URL);
```

Output: line breaks added for clarity.

```
sys_app.do?sys_id=ce05b9f32b840200c5244f74b4da1501&sysparm_goto_url=sys_app.do
%3Fsys_id%3Dce05b9f32b840200c5244f74b4da1501
```

## Scoped GlideSession - isImpersonating\(\)

Returns true if the user is impersonating another user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_shv_tj5_xw" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates the user is impersonating another user.Possible values:

-   true: User is impersonating.
-   false: User isn't impersonating.

</td></tr></tbody>
</table>```
var isImpersonator = gs.getSession().isImpersonating();
gs.info(isImpersonator);
```

## Scoped GlideSession - isInteractive\(\)

Returns true if the session is interactive.

An interactive session is one that involves an end-user interacting with a user interface that then retrieves information from a server. An example of this type of session is when a user logs in using the log-in screen or uses a form to query a data store. A non-interactive session is one that only involves programmatic interaction with a server such as a SOAP request to retrieve data.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_gjc_dpk_ls" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the session is interactive.Possible values:

-   true: Session is interactive.
-   false: Session isn't interactive.

</td></tr></tbody>
</table>```
var interActive = gs.getSession().isInteractive();
gs.info(interActive);
```

## Scoped GlideSession - isLoggedIn\(\)

Returns true if the user is logged in.

|Name|Type|Description|
|----|----|-----------|
|None| | |

<table id="table_qhb_qpk_ls" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Boolean

</td><td>

Flag that indicates whether the user is logged inPossible values:

-   true: User is logged in.
-   false: User isn't logged in.

</td></tr></tbody>
</table>```
var session = gs.getSession();
var loggedIn = session.isLoggedIn();
gs.info(loggedIn);
```

Output:

```
true
```

## Scoped GlideSession - putClientData\(String paramName, String paramValue\)

Sets a session client value that can be retrieved with getClientData\(\). This method is used in a server side script that runs when a form is created.

|Name|Type|Description|
|----|----|-----------|
|paramName|String|Name of the client data to set.|
|paramValue|String|Value of the client data.|

|Type|Description|
|----|-----------|
|void| |

```
var session = gs.getSession();
session.putClientData('test1', 'Harry');
var clientData = session.getClientData('test1');
gs.info(clientData);
```

Output:

```
Harry
```

