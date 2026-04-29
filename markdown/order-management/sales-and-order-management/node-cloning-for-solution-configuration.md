---
title: Node cloning for solution configuration
description: Node cloning lets you duplicate an existing solution configuration node in a set, producing an independent copy that you can modify without affecting the source.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-18"
reading_time_minutes: 1
breadcrumb: [Solution configuration setup, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Node cloning for solution configuration

Node cloning lets you duplicate an existing solution configuration node in a set, producing an independent copy that you can modify without affecting the source.

In solution configuration, a set groups related configuration nodes. When you need a new node that resembles an existing one, cloning that node is faster and less error-prone than building a new one from scratch. The cloned node starts as an exact copy of the source, then diverges as you edit it.

Cloning is available from the solution configuration navigation sidebar. You can clone any node in the set that is in a valid state. Nodes in an invalid state cannot be cloned.

When you clone a node, the following are copied to the new node:

-   All field values, including set-based fields, boolean fields, number fields, picklists, product fields, and text fields.
-   Child configurations associated with the source node, preserving their structure and field values.
-   Nested child configurations, so that the full hierarchy of the source node is reproduced in the clone.

The cloned node is independent of the source. Changes you make to the clone do not affect the source node, and changes to the source do not affect the clone.

## Relationship to existing set repeater controls

Cloning is an additional option in the solution configuration navigation sidebar. It does not replace the existing set repeater controls. The following controls continue to be available alongside Clone and Delete:

-   Add row above
-   Add row below
-   Copy row
-   Delete row

**Note:** Adding a blank node remains available as it was before this capability was introduced. Use Clone when you want a pre-filled copy of an existing node. Use Add when you want to start from an empty node.

## Node hierarchy and recursive cloning

A cloned node can itself be the parent of child and grandchild configurations. When you clone a parent node, the full hierarchy beneath it is reproduced in the new node. This means you do not need to rebuild nested configurations manually after cloning. The depth of the hierarchy that can be cloned depends on the configuration design. Solution configuration supports cloning up to four levels deep.

