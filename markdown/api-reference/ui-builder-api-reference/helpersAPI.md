---
title: helpers - UI Builder
description: The helpers API provides general functionality that is common across page scripts, eliminating the need to write scripts for simple functionality such as opening and closing a modal.Closes the specified modal on the current page.Opens the specified modal on the current page.Passes the specified parameters down to other components on the same page.Navigates from one screen to another based on the specified route and field information. URL changes and the respective screen loads are observed.Enables pages to report their status updates, such as title, icon, dirty state, message, and error changes.Makes an HTTP request to the ServiceNow instance and returns a promise with the results.Cancels the execution of the function that was scheduled through a prior setInterval\(\) call.Cancels the execution of the function that was scheduled through a prior setTimeout\(\) call.Repeatedly executes the specified function, using the specified delay value as the interval between function calls.Executes the specified function, after the specified delay.Asynchronously retrieves and translates the specified message based on the current user's session language.
locale: en-US
release: australia
product: UI Builder API Reference
classification: ui-builder-api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [UIB API reference, API reference, API implementation and reference]
---

# helpers - UI Builder

The helpers API provides general functionality that is common across page scripts, eliminating the need to write scripts for simple functionality such as opening and closing a modal.

This API is only available to page scripts, it is not available in any other UI Builder scripts including:

-   component property value scripts
-   component visibility scripts
-   event payload scripts
-   UX client script includes

**Parent Topic:**[UIB API reference](../../../../../build/applications/concept/api-uib.md)

## helpers - helpers.modal.close\(String modalId\)

Closes the specified modal on the current page.

|Name|Type|Description|
|----|----|-----------|
|modalId|String|Modal component ID of the modal to close. Component IDs are auto generated when a component is dragged and dropped on the UI Builder stage. You can locate the ID on the property page.|

|Type|Description|
|----|-----------|
|None| |

This example shows closing a modal with a component ID that ends with `alert-modal`.

```
function handler({api, event, imports, helpers}) {
  helpers.modal.close("[component-id$='alert_modal']")
}
```

## helpers - helpers.modal.open\(String modalId, Object options\)

Opens the specified modal on the current page.

You can only display one modal at a time within a page. If a modal is currently open, and you call this method, the existing modal is hidden and the new modal appears.

<table id="table_mmh_5ky_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

modalId

</td><td>

String

</td><td>

Component ID of the modal to open. Component IDs are auto generated when a component is dragged and dropped on the UI Builder stage. You can locate the ID on the property page.

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Optional.```
"options": {
  "content": "String",
  "contentFullWidth": Boolean,
  "headerLabel": "String",
  "size": "String"
}
```

</td></tr><tr><td>

options.content

</td><td>

String

</td><td>

Text content for the modal.

</td></tr><tr><td>

options.contentFullWidth

</td><td>

Boolean

</td><td>

Flag that indicates whether to remove the horizontal padding around the body of the modal in order to fit wider content.Valid values:

-   true: Remove the padding.
-   false: Do not remove the padding.

 Default: false

</td></tr><tr><td>

options.headerLabel

</td><td>

String

</td><td>

Text content for the modal header.

</td></tr><tr><td>

options.size

</td><td>

String

</td><td>

Size of the modal container. Most sizes automatically expand to fill the viewport when the screen size is small.Valid values:

-   sm
-   md
-   lg
-   fullscreen

 Default: sm

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows opening a modal with ca omponent ID that ends with `alert-modal`.

```
function handler({api, event, imports, helpers}) {
  helpers.modal.open("[component-id$='alert_modal']")
}
```

## helpers - helpers.navigate.setRouteParams\(Object params\)

Passes the specified parameters down to other components on the same page.

Use this method in any page component that wants to add a parameter in a URL. You may want to add a parameter to a URL when another component needs to know the current value of that parameter when it changes, so it can react to it. For example, use this method to pass the `selectedIndex` of a tab component so it reflected in the URL to give focus to that tab.

<table id="table_jnx_kf1_p4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

params

</td><td>

Object

</td><td>

Key-value pairs of optional parameters to pass to other components. This must be a plain, flat object with only primitive values. Array or object references are ignored and not added to the URL. All specified keys  must be part of  the optional parameters  in the route configuration or they are also ignored. For additional information on optional parameters, see Create a page in UI Builder.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This code example shows how to append the URL `params/selected-tab-index/2`. Note that the parameter in the actual URL is changed from camel case to snake case, so `selectedTabIndex` becomes `selected-tab-index`.

```
function handler({api, event, helpers, imports}) {  
  helpers.navigate.setRouteParams({'params': {'selectedTabIndex':  2}});  
} 
```

## helpers - helpers.navigate.to\(String route, Object fields, Object params, Boolean redirect, Boolean passiveNavigation, String targetRoute\)

Navigates from one screen to another based on the specified route and field information. URL changes and the respective screen loads are observed.

<table id="table_htg_jzy_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

route

</td><td>

String

</td><td>

Name of the route. Must be a valid entry from UX App Routes \(sys\_ux\_app\_route.list\). This value is reflected in the URL, and the URL is created based on the**route**, **fields**, and **optionalParams** column values: `/<route>/<field1Value>/{<field2Value>/params/<optionalParamKey1>/<optionalParamValue1>/<optionalParamKey2>/<optionalParamValue2>` For example: `/record/incident/12345/params/selectedTabIndex/4`

</td></tr><tr><td>

fields

</td><td>

Object

</td><td>

Optional. Key-value pairs of required parameters. For example: `'fields' : {'table': 'incident', 'sysId': '12345'}`.

</td></tr><tr><td>

params

</td><td>

Object

</td><td>

Optional. Key-value pairs of optional parameters. For example: `'params' : {'selectedTabIndex': 4}`.

</td></tr><tr><td>

redirect

</td><td>

Boolean

</td><td>

Flag that indicates whether to remove the latest history entry from the browser history. For example, if you navigate to sites A, B and then C. If **redirect** is set to `true` while navigating to C, the history entry for B is removed. The browser history only shows only A and C.Valid values:

-   true: Removes the latest history entry, and redirects to the latest URL.
-   false: Does not remove any history entries.

 Default: false

</td></tr><tr><td>

passiveNavigation

</td><td>

Boolean

</td><td>

Flag that indicates whether to perform background navigation. Background navigation is when a page is opened but it is not active or shown. For example, opening an inactive tab for the page, but it is not visible but loaded in the background.Valid values:

-   true: Perform background navigation.
-   false: Do not perform background navigation.

 Default: false

</td></tr><tr><td>

targetRoute

</td><td>

String or Object

</td><td>

Sub navigation to a drill-down, deep-link, or sub-tab. If set to `current`, the current route does a sub-navigation under the current URL. For example, if `/record/incident/123` is the current URL, and the following call is made:

 `helper.navigate.to('record', {'table': 'problem', 'sysId': '567'}, {}, false, false, 'current');`

 The following URL is generated: `/record/incident/123/sub/record/problem/567`

 **Note:** **targetRoute** can be either a string such as `'current'` or an object, such as `navigation NAV_ITEM_SELECTED payload`.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

This example shows how to navigate to a page passing just the **route** parameter.

```
function handler({api, event, imports, helpers}) {
  helpers.navigate.to('test');
}
```

This example shows how to navigate to a page passing the **route** and **fields** parameters.

```
function handler({api, event, imports, helpers}) {
  helpers.navigate.to('test', {'key': 'value'});
}
```

This example shows how to navigate to a page passing the **route**, **fields**, and **params** parameters.

```
function handler({api, event, helpers, imports}) {
  helpers.navigate.to('test', {'key': 'value'}, {'first': 'FirstName', 'last': 'Last Name'});
}
```

## helpers - helpers.screen.updateStatus\(Object statusObj\)

Enables pages to report their status updates, such as title, icon, dirty state, message, and error changes.

Status updates are reported to WorkspaceChrome or AppShell, whichever the outer layer is, and acting as the host.

<table id="table_hwx_j31_p4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

statusObj

</td><td>

Object

</td><td>

Payload to send to the current page to report that the content has been updated.Valid values:

-   **dirtyModalId**: \(String\) ID of the modal that has changed.
-   **hasError**: \(Boolean\) Flag that indicates that there are errors on the page.
-   **hasUpdate**: \(Boolean\) Flag that indicates that there were updates to the page.
-   **icon**: \(String\) Name of the updated or new icon.
-   **isDirty**: \(Boolean\) Flag that indicates whether the page is dirty \(values have changed\).
-   **message**: \(String\) Updated/new message.
-   **screenKey**: \(String\) ID of the screen on which the change occurred. Every screen has a **screenKey** as a property on the screen macroponent inside sn-canvas-screen.
-   **status**: \(String\) Status operation for this action. This value must be one of the following: inserted, deleted, saved, or closed.
-   **title**: \(String\) Updated/new display title.
-   **tooltipPreview**: \(JSON\) Updated or new tool tip. For example, `tooltipPreview : { primaryTitle, secondaryContent: {} }`

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|None| |

```
screen.updateStatus({'dirtyModalId': 'customModalId', 'isDirty': true});
```

## helpers - helpers.snHttp\(String url, Object options\)

Makes an HTTP request to the ServiceNow instance and returns a promise with the results.

**Note:** There is a known issue where objects named **options** are omitted from the HTTP response.

```
{
  options: {},
  otherFields: {}
}

becomes

{
  otherFields: {}
}
```

<table id="table_o4d_4rr_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

url

</td><td>

String

</td><td>

HTTP endpoint relative to the instance URL. For example, `/api/now/table/incident` or `/api/now/table/incident/a83820b58f723300e7e16c7827bdeed`.

</td></tr><tr><td>

options

</td><td>

Object

</td><td>

Describes the contents of the HTTP request.```
"options": {
  "batch": Boolean,
  "body": {Object},
  "headers": {Object},
  "method": "String"
}
```

</td></tr><tr><td>

options.batch

</td><td>

Boolean

</td><td>

Optional. Flag that indicates whether this HTTP request should be batched with other HTTP requests made to the instance.Valid values:

-   true: Make request as part of a batch request.
-   false: Make dedicated request.

 Default: true

</td></tr><tr><td>

options.body

</td><td>

Object

</td><td>

Optional. Data to send as the request body. Only applicable for request methods `PUT`, `POST`, and `PATCH`. Elements in the object depend on the type of HTTP method. For details, refer to the code examples below.Default: `{}`

</td></tr><tr><td>

options.headers

</td><td>

Object

</td><td>

Optional. Additional HTTP request headers. For example:

 ```
headers: {
  "Content-Type": "application/json",
  "Accept": "application/xml"
}
```

</td></tr><tr><td>

options.method

</td><td>

String

</td><td>

Optional. HTTP method.Valid values:

-   DELETE
-   GET
-   PATCH
-   POST
-   PUT

 Default: GET

</td></tr></tbody>
</table><table id="table_p4d_4rr_n4b" class="returns"><thead><tr><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Object that describes any error returned by the REST API.Data type: Object

 ```
"error": {
  "data": "String",
  "message": "String",
  "options": {Object},
  "status": Number,
  "statusText": "String"
}
```

</td></tr><tr><td>

error.data

</td><td>

Response returned from the HTTP API.Data type: Defined by REST API

</td></tr><tr><td>

error.message

</td><td>

Message describing the error encountered when trying to process the HTTP request.**Note:** This parameter is not always returned.

 Data type: String

</td></tr><tr><td>

error.options

</td><td>

Describes the original HTTP request.Data type: Object

 ```
"options": {
  "headers": {Object},
  "responseHeader": {Object}
}
```

</td></tr><tr><td>

error.options.headers

</td><td>

Object containing a list of all of the request headers sent in the request.Data type: Object

</td></tr><tr><td>

error.options.responseHeaders

</td><td>

Object containing a list of all of the response headers sent in the request.Data type: Object

</td></tr><tr><td>

error.status

</td><td>

Returned HTTP error status code, such as 400, 405, or 500.Data type: Number

</td></tr><tr><td>

error.statusText

</td><td>

Returned HTTP status message, such as `Bad Request`. Data type: String

</td></tr><tr><td>

response

</td><td>

Returned when HTTP request is successful. The response to the HTTP request.Data type: Any

</td></tr></tbody>
</table>The following example show how to call snHttp\(\) which returns a promise.

```
function handler({api, event, helpers, imports}) {
  helpers.snHttp('/api/now/table/u_movie', {method: 'GET'})
    .then(({response}) => {
      // do something with the table data
    })
    .catch(({error}) => {
      const message = `Error: ${error.data.error.message}`;
      console.error(message);
      api.emit('NOW_UXF_PAGE#ADD_NOTIFICATIONS', {
        id: 'alert5',
        status: 'high',
        icon: 'info-circle-outline',
        content: message,
        action: { type: 'dismiss' }
    });
  });
}
```

The following example show how to call snHttp\(\) using *async* and *await*.

```
async function handler({helpers}) {
  try {
    const result = await helpers.snHttp('/api/now/table/u_movie', {method: 'GET'});
  } catch ({error}) {
      const message = `Error: ${error.data.error.message}`;
      console.error(message);
      api.emit('NOW_UXF_PAGE#ADD_NOTIFICATIONS', {
        id: 'alert5',
        status: 'high',
        icon: 'info-circle-outline',
        content: message,
        action: { type: 'dismiss' }
      });
  }
}
```

The following example show how to set up a POST request.

```
function handler({api, helpers, event, imports}) {
  helpers
    .snHttp("/api/now/table/incident", {
      method: "POST",
      body: {
        description: "Sample description",
        close_notes: "Sample close notes",
        order: "-1"
      }
    })
    .then(({ response }) => {
      // handle POST request response
    })
    .catch(({ error }) => {
      // handle POST request errors
    });
}
```

The following example show how to set up a PUT request.

```
function handler({api, helpers, event, imports}) {
  helpers
    .snHttp("/api/now/table/incident/a83820b58f723300e7e16c7827bdeed2", {
      method: "PUT",
      body: {
        activity_due: "1970-04-02 18:26:17"
      },
      headers: {
        "Content-Type": "application/json",
        "Accept": "application/xml"
      }
    })
    .then(({ response }) => {
      // handle PUT request response
    })
    .catch(({ error }) => {
      // handle PUT request errors
    });
}
```

## helpers - helpers.timing.clearInterval\(Number timeoutId\)

Cancels the execution of the function that was scheduled through a prior setInterval\(\) call.

|Name|Type|Description|
|----|----|-----------|
|timeoutId|Number|Unique identifier of the scheduled function to clear. This value is returned by the corresponding setInterval\(\) call.|

|Type|Description|
|----|-----------|
|None| |

This example shows using clearInterval\(\) to cancel a timing operation that was previously set using thesetInterval\(\) method. This function could be invoked by a user clicking a **Disable Auto-refresh** button on a page.

```
function handler({api, helpers}) {
  api.setState('intervalId', ({currentValue}) => {
    if (currentValue > -1) {
      helpers.timing.clearInterval(currentValue);
    }
    return -1;
  });
}
```

## helpers - helpers.timing.clearTimeout\(Number timeoutId\)

Cancels the execution of the function that was scheduled through a prior setTimeout\(\) call.

|Name|Type|Description|
|----|----|-----------|
|timeoutId|Number|Unique identifier of the scheduled function to clear. This value is returned by the corresponding setTimeout\(\) call.|

|Type|Description|
|----|-----------|
|None| |

This code example shows how to terminate a timer with the specified *timeoutId*.

```
function handler({api, helpers}) {
  api.setState('timeoutId', ({currentValue}) => {
    if (currentValue > -1) {
      helpers.timing.clearTimeout(currentValue);
    }
    return -1;
  });
}
```

## helpers - helpers.timing.setInterval\(Function fn, Number delay\)

Repeatedly executes the specified function, using the specified delay value as the interval between function calls.

Unlike the native JavaScript setInterval\(\) method, this method does not support passing a code string to evaluate as the first argument. Any additional arguments are passed to the function itself.

<table id="table_t4h_sdy_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fn

</td><td>

Function

</td><td>

Function to repeatedly execute.

</td></tr><tr><td>

delay

</td><td>

Number

</td><td>

Length of the time-interval between each function execution. Unit: Milliseconds

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Number|Unique identifier of the function execution operation. Use this value in the [helpers - helpers.timing.clearInterval\(Number timeoutId\)](helpersAPI.md#) method if you need to cancel this operation.|

This code example shows how to refresh the timestamp on a page every second. This function could be invoked by a user clicking an **Enable Auto-refresh** button on a page.

```
function handler({api, helpers}) {
  // Every one second, refresh the value of current timestamp client state parameter
  const intervalId = helpers.timing.setInterval(() => {
    api.setState('currentTimestamp', new Date().toString())
  }, 1000);

  // The interval ID is kept in state to use when calling the helpers.timing.clearInterval() method at a later point
  api.setState('intervalId', intervalId);
}
```

## helpers - helpers.timing.setTimeout\(Function fn, Number delay\)

Executes the specified function, after the specified delay.

Unlike the native JavaScript setTimeout\(\) method, this method does not support passing a code string to evaluate as the first argument. Any additional arguments are passed to the function itself.

<table id="table_xrg_53y_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

fn

</td><td>

Function

</td><td>

Function to execute.

</td></tr><tr><td>

delay

</td><td>

Number

</td><td>

Length of the time to wait before calling the specified function. Unit: Milliseconds

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Number|Unique identifier of the function execution operation. Use this value in the [helpers - helpers.timing.clearTimeout\(Number timeoutId\)](helpersAPI.md#) method if you need to cancel this operation.|

This code example shows how to set a 20 minute timer. You could associate this function with a button **Remind me in 20 minutes**.

```
function handler({api, helpers}) {
  const timeoutId = helpers.timing.setTimeout(() => {
    api.emit('NOW_UXF_PAGE#ADD_NOTIFICATIONS', {
      id: 'alert5',
      status: 'high',
      icon: 'info-circle-outline',
      content: 'Try to look away at something that is 20 feet away from you for a total of 20 minutes.',
      action: { type: 'dismiss' }
    });
  }, 20 * 60 * 1000);

  // The timeout ID is kept in state to use when calling the helpers.timing.clearTimeout() method at a later point
  api.setState('timeoutId', timeoutId);
}
```

## helpers - helpers.translate\(String message, String tokens\)

Asynchronously retrieves and translates the specified message based on the current user's session language.

You can use this method with the [api - setState\(String stateParam, Any value\)](../../api/concept/apiAPI.md#) to bind the translated value to other fields on the page.

**Note:** You can call this method using a promise or `async` and `await`. The code examples below show both implementations.

<table id="table_xjy_kxw_n4b" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

message

</td><td>

String

</td><td>

Message to translate.

</td></tr><tr><td>

tokens

</td><td>

String

</td><td>

Optional. Comma-separated list of parameters to use for replacing string variables.For example:

 ```
helpers.translate('Text {0} {1}', 'to', 'translate'); 
```

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|String|Translated text string.|

The following example shows how to pass in table field references to embed in the corresponding variables in a string, using a promise.

```
function handler ({api, helpers}) {
  helpers.translate('Welcome {0} {1}!', user.firstName, user.lastName)
    .then((translatedText) => {
      api.setState('greeting', translatedText);
    });
}
```

The following example shows how to use `async` and `await` in your function instead of a promise.

```
async function handler ({api, helpers}) {
  const translatedText = await helpers.translate('Welcome to {0}', 'ServiceNow');
    api.setState('greeting', translatedText);
}
```

