---
title: Code reviews
description: Team Development administrators can require that pushes undergo code review before accepting pushes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/team-development/c\_CodeReview.html
release: zurich
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Pushing changes, Working with changes, Team Development, Planning your application, Building applications]
---

# Code reviews

Team Development administrators can require that pushes undergo code review before accepting pushes.

When code review is enabled, pushing a change to the parent instance triggers the code review workflow. By default, the teamdev\_code\_reviewer role receives notifications to review changes and can approve or reject changes.

\[Omitted image "team-dev-code-review-workflow.png"\] Alt text: Code review workflow.

1.  Starts when changes are pushed to the parent instance.
2.  Verifies that the code review property is active on the parent instance.
3.  Sets the state of the changes requiring approval to Awaiting Code Review.
4.  If configured [Notifies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/c_CodeReviewNotifications.md) the Team Development Code Reviewers group to review pushed changes.
5.  Loads the approved changes or sets the state to Code Changes Rejected.

## Change details

For each change, reviewers can see the following information.

-   Which [remote instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_DefineARemoteInstance.md) the pushed change comes from?
-   Who pushed the change to the parent?
-   What the change is called?
-   When the change was created?
-   Which versions the change includes?

Reviewers must approve or reject a push from the Team Development application.

## Child instance restrictions

While changes are being reviewed on the parent instance, a child instance can’t do the following activities involving the parent instance:

-   Push changes to the parent instance.
-   Pull changes from the parent instance.
-   Reconcile changes with the parent instance.
-   Change the parent instance to another instance.
-   Delete the remote instance record for the parent instance.

-   **[Enable a code review](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_EnableCodeReview.md)**  
You can require a code review of all changes pushed to an instance.
-   **[Cancel a code review request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_CancelACodeReviewRequest.md)**  
Developers can cancel any push they submitted that is in the **Awaiting Code Review** stage.
-   **[Code review notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/c_CodeReviewNotifications.md)**  
You can enable email notifications on the instance requiring a code review.

**Parent Topic:**[Pushing changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/pushing-changes.md)

