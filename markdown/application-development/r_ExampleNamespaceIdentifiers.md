---
title: Namespace identifier examples
description: The following examples illustrate generating namespace identifiers for applications, tables, and fields.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 1
breadcrumb: [Namespace identifier, Application scope, Anatomy of an application, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Namespace identifier examples

The following examples illustrate generating namespace identifiers for applications, tables, and fields.

<table id="table_mfl_34b_br"><thead><tr><th>

Action

</th><th>

Element generated

</th><th>

Explanation

</th></tr></thead><tbody><tr><td>

1. Generate a namespace identifier for a private scope application called Book Rooms.

</td><td>

x\_acme\_book\_rooms

</td><td>

This is a combination of the vendor prefix and application ID.

</td></tr><tr><td>

2. Generate a namespace identifier for a global scope application called Marketing Events.

</td><td>

None

</td><td>

The system does not generate namespace prefixes for global applications.

</td></tr><tr><td>

3. Add the conference rooms table to the Book Rooms application.

</td><td>

x\_acme\_book\_rooms\_conference\_rooms

</td><td>

This table is in the Book Rooms scope so begins with the namespace identifier.

</td></tr><tr><td>

4. Add a Marketing Event table to a global application.

</td><td>

u\_marketing\_event

</td><td>

Custom tables in the global scope always use the `u_` namespace identifier.

</td></tr><tr><td>

5. Select Book Rooms in the application picker and add the **Capacity** field on the Conference Rooms table.

</td><td>

capacity

</td><td>

The field is in the same scope as the table so it does not have its own namespace identifier. However, to dot-walk to the field in a script, you would use the full path including the table namespace identifier: `x_acme_book_rooms_conference_rooms.capacity`.

</td></tr><tr><td>

6. Select Book Rooms in the application picker and add the **Theme** field to the Marketing Event table.

</td><td>

x\_acme\_book\_rooms\_theme

</td><td>

The field is in a different scope from the table so it is prefixed with the `x_acme_book_rooms` namespace identifier. To dot-walk to the field in a script, you would use full path including the field namespace identifier: `u_marketing_event.x_acme_book_rooms_theme`. **Note:** This example assumes that the Marketing Event table allows other application scopes to add fields.

</td></tr><tr><td>

7. Select Marketing Events in the application picker and add the **Theme** field to the Marketing Event table.

</td><td>

u\_theme

</td><td>

Custom fields in the global scope use the **u\_** prefix. To dot-walk to the field in a script, you would use `u_marketing_event.u_theme`.

</td></tr></tbody>
</table>