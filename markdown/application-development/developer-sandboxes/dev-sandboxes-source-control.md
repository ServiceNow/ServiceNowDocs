---
title: Source control and Developer Sandboxes
description: Use source control with Developer Sandboxes to enable parallel development and prevent merge conflicts.
locale: en-US
release: zurich
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2025-08-08"
reading_time_minutes: 1
breadcrumb: [Explore, Developer Sandboxes, Developing your application, Building applications]
---

# Source control and Developer Sandboxes

Use source control with Developer Sandboxes to enable parallel development and prevent merge conflicts.

## Source control overview

Traditional, single-instance development is an outdated model that requires oversight and maintenance. Sharing a single instance increases the risk of merge conflicts and restricts teams to a single version of code. Enterprise IT architecture standards are increasingly mandating full version control for architectural compliance and IP management.

In support, use Developer Sandboxes in tandem with Git source control to synchronize changes between the base and sandbox environments.

Using source control, developers can work on independent branches and merge them according to your organization's best practices.

![Sample Git-based version control flow chart](../image/dev-sbx-infographic-git.png "Example branching strategy with source control")

## Git credentials

Each sandbox inherits Git credentials from the base instance. However, developers can add or change Git credentials locally within the sandbox. A new branch should be created for each sandbox.

