---
title: Code review workflow
description: The Team Development Code Review workflow manages how changes are pushed to the parent.
locale: en-US
release: australia
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Code reviews, Administer, Team Development, Planning your application, Building applications]
---

# Code review workflow

The Team Development Code Review workflow manages how changes are pushed to the parent.

By default this workflow:

-   Starts when changes are pushed to the parent instance.
-   Verifies that the code review property is active on the parent instance.
-   Sets the stage of changes requiring approval to Awaiting Code Review.
-   [Notifies](c_CodeReviewNotifications.md) the Team Development Code Reviewers group to review pushed changes, if configured.
-   Loads approved changes or sets the stage to Code Changes Rejected.

![Workflow describing the code review process in Team Development](../image/TeamDevelopmentCodeReviewWorkflow.png "Team Development code review workflow")

**Warning:** Use caution when modifying this workflow, as the code review feature may not function properly.

