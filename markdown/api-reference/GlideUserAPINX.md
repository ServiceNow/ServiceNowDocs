---
title: GlideUser \(Next Experience\) - Client
description: The GlideUser API provides a method to access information about current user roles in the Next Experience UI Framework.Returns all roles assigned to the current user.
locale: en-US
release: zurich
product: API Reference
classification: api-reference
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client Next Experience API reference, API reference, API implementation and reference]
---

# GlideUser \(Next Experience\)- Client

The GlideUser API provides a method to access information about current user roles in the Next Experience UI Framework.

GlideUser methods are accessed through a global object \(`g_user`\) that is only available in client scripts.

**Parent Topic:**[Client Next Experience API reference](../../../../../build/applications/concept/api-client-next.md)

## GlideUser \(Next Experience\) - getRoles\(\)

Returns all roles assigned to the current user.

|Name|Type|Description|
|----|----|-----------|
|None| | |

|Type|Description|
|----|-----------|
|Array|Array of roles assigned to the current user. Includes explicitly granted roles, inherited roles, and roles acquired by group membership.|

This example checks if the current user has the admin role.

```
if (g_user.getRoles().indexOf('admin') !== -1) {
    console.log('User is admin');
}
```

Output:

```
User is admin
```

This example logs all roles assigned to the current user.

```
function onChange(control, oldValue, newValue, isLoading, isTemplate) {
   if (isLoading || newValue === '') {
      return;
   }
   console.log(g_user.getRoles());
}
```

Output:

```
['actsub_user', 'sn_publications_recipients_list_user', 'sn_publications.author', 'interaction_agent', 'interaction_admin', 'image_admin', 'sn_publications_recipients_user', 'workflow_publisher', 'knowledge']
```

