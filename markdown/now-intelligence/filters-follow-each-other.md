---
title: Conditions for two filters to follow each other
description: It is possible to set up two filters to follow each other mutually. However, several technical limitations apply.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Select or cascading filters, Filters, Platform Analytics experience, Platform Analytics]
---

# Conditions for two filters to follow each other

It is possible to set up two filters to follow each other mutually. However, several technical limitations apply.

Two Single/Multiple select filters can follow each other through a direct connection, as described in [Configure a Single/Multiple select or cascading filter](../task/create-select-filter-workspace.md). The conditions described in that topic apply to both filters. For example, both filters must filter data on the other's filter source.

Two Single/Multiple select filters can also filter each other through a many-to-many connection, as described in [Set a filter to follow another filter in a many-to-many relationship](../task/set-filter-to-follow-filter.md). Only admins can set up such a connection.

Besides the general conditions for a filter to follow another, the following conditions also apply:

-   **Mixed connection types are invalid**

    Both filters must follow each other through either a direct connection or a many-to-many connection. One filter cannot follow the other directly and be followed through a many-to-many connection.

-   **Many-to-many connections must use the same connection table**

    If two filters follow each other through many-to-many connections, both connections must use the same connecting table.


