---
title: Code review workflow
description: The Team Development Code Review workflow manages how changes are pushed to the parent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/application-development/team-development/c\_CodeReviewWorkflow.html
release: yokohama
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Team Development, Team Development, Planning your application, Building applications]
---

# Code review workflow

The Team Development Code Review workflow manages how changes are pushed to the parent.

By default this workflow:

-   Starts when changes are pushed to the parent instance.
-   Verifies that the code review property is active on the parent instance.
-   Sets the stage of changes requiring approval to Awaiting Code Review.
-   [Notifies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/application-development/team-development/c_CodeReviewNotifications.md) the Team Development Code Reviewers group to review pushed changes, if configured.
-   Loads approved changes or sets the stage to Code Changes Rejected.

\[Omitted image "TeamDevelopmentCodeReviewWorkflow.png"\] Alt text: Workflow describing the code review process in Team Development

**Warning:** Use caution when modifying this workflow, as the code review feature may not function properly.

