---
title: Team Development
description: Team Development supports parallel development on multiple, non-production ServiceNow instances.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/team-development/c\_TeamDevelopment.html
release: xanadu
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Planning your application, Building applications]
---

# Team Development

Team Development supports parallel development on multiple, non-production ServiceNow instances.

Team Development provides the following features:

-   Branching operations, including pushing and pulling record versions between instances.
-   The ability to compare a development instance to other development instances.
-   A central dashboard for all Team Development activities.

-   **[Team Development overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/c_UsingTeamDevelopment.md)**  
Team Development allows developers to work on separate development instances while sharing code and resolving collisions throughout the development process.
-   **[Team Development setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/c_SettingUpTeamDevelopment.md)**  
To enable parallel development on multiple non-production instances, administrators can set up the Team Development instance hierarchy and grant access rights for developers.
-   **[Code reviews](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/c_CodeReview.md)**  
Team Development administrators can require that pushes undergo code review before accepting pushes.
-   **[Code review notifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/c_CodeReviewNotifications.md)**  
You must enable email notifications on the instance requiring code review for that instance to send code review notifications.
-   **[Code review workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/c_CodeReviewWorkflow.md)**  
The Team Development Code Review workflow manages how changes are pushed to the parent.
-   **[Exclusion policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/c_ExclusionPolicies.md)**  
You can exclude certain files from change tracking by creating an exclusion policy.
-   **[Instance hierarchies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/c_InstanceHierarchies.md)**  
Team Development allows you to set up a distributed version control system between multiple ServiceNow instances where each instance acts as a source repository, or branch.
-   **[Pulls and pushes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/c_PullsAndPushes.md)**  
Developers synchronize their instances to the parent instance by pulling and pushing versions of customized records and resolving collisions between versions on the parent instance and the development instance.
-   **[Team Development process](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/t_TeamDevelopmentProcess.md)**  
The basic Team Development process sets up the instance hierarchy, grants developer access rights, manages the movement of development changes from development instances to test instances, and promotes applications to the production instance.
-   **[Team Development roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/c_TeamDevelopmentRoles.md)**  
To use Team Development, developers must have admin access to their development instance.
-   **[Versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/c_Versions.md)**  
Version records track changes to a customized record over time so that administrators can compare or revert to specific versions later.
-   **[Versions and local changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/team-development/c_VersionsAndLocalChanges.md)**  
Version records track changes to a customizable record over time so that you can compare or revert to a specific version later.

**Parent Topic:**[Planning your application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/building-applications/planning-applications.md)

