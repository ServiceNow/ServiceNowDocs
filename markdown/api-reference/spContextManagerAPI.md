---
title: spContextManager - Client
description: Makes data from a Service Portal widget available to other applications and services in a Service Portal page. For example, pass widget data to Agent Chat when it opens in a Service Portal page.Initializes a key and adds widget data as the value. For example, add data to the 'agent-chat' key to make it available to Agent Chat.Returns each key and associated data object defined by any widget on the page.Returns the widget data associated with a key.Sends data to an existing key. For example, if another widget on the page uses the 'agent-chat' key to pass data to the Agent Chat configuration, you must update the context of the key rather than using the addContext\(\) method.
locale: en-US
release: australia
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Client API reference, API reference, API implementation and reference]
---

# spContextManager- Client

Makes data from a Service Portal widget available to other applications and services in a Service Portal page. For example, pass widget data to Agent Chat when it opens in a Service Portal page.

The spContextManager API is an AngularJS service that you can use in Service Portal widget client scripts.

Keys passed to this API are unique per page. For example, if the `'agent-chat'` key is already initialized by another widget on the page through the addContext\(\) method, you must use the updateContextForKey\(\) method to update the key's data. Available keys include: agent-chat: Sends widget data to Agent Chat.

For more information about passing data to Agent Chat, see Configure Agent Chat in Service Portal.

**Parent Topic:**[Client API reference](../../../../../build/applications/concept/api-client.md)

## spContextManager - addContext\(String key, Object context\)

Initializes a key and adds widget data as the value. For example, add data to the 'agent-chat' key to make it available to Agent Chat.

Use this method the first time data is added to a specific key on a Service Portal page. If the key is already used by another widget on the page, use the updateContextForKey\(\) method instead.

<table id="table_dsz_dcz_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key

</td><td>

String

</td><td>

Name of the key to send the data. Available keys include**agent-chat**: Sends widget data to Agent Chat when it opens in a Service Portal page.

</td></tr><tr><td>

context

</td><td>

Object

</td><td>

Widget data in JSON format to send to the application or service specified in the key parameter. For example, `{'approval_count': 5}`.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

Pass `approval_count` to Agent Chat. When a user initiates an Agent Chat conversation from the Service Portal homepage, the system appends `&sysparm_approval_count=5` to the Agent Chat `iframe` URL.

```
function ($scope, spContextManager) {
    spContextManager.addContext('agent-chat', {
        'approval_count': 5       
    });
};
```

## spContextManager - getContext\(\)

Returns each key and associated data object defined by any widget on the page.

Using this method may affect performance. Use this method to understand which keys are initialized on the page and to get their current values. If you know which key you need to access, use the getContextForKey\(\) method instead.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Object|Each key and associated data object defined on the page.|

```
function ($scope, spContextManager) {
  spContextManager.getContext();
} 
```

## spContextManager - getContextForKey\(String key, Boolean returnPromise\)

Returns the widget data associated with a key.

<table id="table_w2r_jcz_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key

</td><td>

String

</td><td>

Name of the key to get context from. Available keys include: agent-chat: Sends widget data to Agent Chat.

</td></tr><tr><td>

returnPromise

</td><td>

Boolean

</td><td>

Flag that determines whether to return the data associated with a key as a promise or an object. Values include: -   True: return the data as a promise. Use this option if another widget on the page uses the addContext\(\) method to initialize the same key. Returning a promise prevents returning an undefined object when the key is not yet initialized.
-   False: returns an object containing the data associated with the key.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|Promise|If returnPromise is true, returns a promise that is fulfilled when another widget on the page initializes the key.|
|Object|If returnPromise is false, returns an object containing the data associated with the key. For example, `{approval_count: 5}`.|

Pass `approval_count` to Agent Chat. When a user initiates an Agent Chat conversation from the Service Portal homepage, the system appends `&sysparm_approval_count=5` to the Agent Chat `iframe` URL.

```
function ($scope, spContextManager) {
  spContextManager.getContextForKey('agent-chat', true).then(function(context) {
    context = context || {};
    context.approval_count = 5; 
    spContextManager.updateContextForKey('agent-chat', context);
  });
} 
```

## spContextManager - updateContextForKey\(String key, Object context\)

Sends data to an existing key. For example, if another widget on the page uses the 'agent-chat' key to pass data to the Agent Chat configuration, you must update the context of the key rather than using the addContext\(\) method.

<table id="table_mhr_lcz_qhb" class="parameters"><thead><tr><th>

Name

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

key

</td><td>

String

</td><td>

Name of the key to send the data. Available keys include**agent-chat**: Sends widget data to Agent Chat when it opens in a Service Portal page.

</td></tr><tr><td>

context

</td><td>

Object

</td><td>

Widget data in JSON format to send to the application or service specified in the key parameter. For example, `{'approval_count': 5}`.

</td></tr></tbody>
</table>|Type|Description|
|----|-----------|
|void| |

Pass `approval_count` to Agent Chat. When a user initiates an Agent Chat conversation from the Service Portal homepage, the system appends `&sysparm_approval_count=5` to the Agent Chat `iframe` URL.

```
function ($scope, spContextManager) {
  spContextManager.getContextForKey('agent-chat', true).then(function(context) {
    context = context || {};
    context.approval_count = 5; 
    spContextManager.updateContextForKey('agent-chat', context);
  });
} 
```

