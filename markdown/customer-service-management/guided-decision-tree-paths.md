---
title: Decision tree paths
description: A path is created and associated with a node and represents the potential outcome of that node.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Decision trees in Guided decision, Guided Decisions configuration, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Decision tree paths

A path is created and associated with a node and represents the potential outcome of that node.

When you create a path, you provide a name, a priority, and the path conditions.

|Field|Description|
|-----|-----------|
|Path name|The path name appears in the decision tree.|
|Path priority|The priority determines which path and its conditions get checked first when there are multiple paths. A node can have more than one path but only one path from a node can be executed at a time. For example, a path with a priority of 100 has a lower priority value than a path with a priority of 200, so only path with priority 100 is executed.|
|Path conditions|Path conditions represent the potential answers or outcomes from a node. You create path conditions using a condition builder, which has access to its direct parent node’s inputs. It uses these inputs to create informative path conditions that represent potential answers or outcomes for the node. Path conditions must be met in order to go to the path's destination node.|

-   Decision Tree Builder: [Determine the next node displayed in a decision tree](../task/configure-path-in-gdb.md)
-   Core UI: [Determine the next node in a decision tree](../task/create-decision-paths.md)

