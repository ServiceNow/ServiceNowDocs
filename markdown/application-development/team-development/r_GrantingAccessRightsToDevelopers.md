---
title: Access rights for developers
description: To use Team Development, application developers must have a set of credentials for each instance in the Team Development hierarchy.
locale: en-US
release: xanadu
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Team Development setup, Team Development, Planning your application, Building applications]
---

# Access rights for developers

To use Team Development, application developers must have a set of credentials for each instance in the Team Development hierarchy.

An instance's placement in the [team development hierarchy](../task/t_SetUpAnInstanceHierarchy.md) determines the credentials it requires.

<table id="table_vnz_5jb_bq"><thead><tr><th>

Desired Access

</th><th>

Credential Requirements

</th></tr></thead><tbody><tr><td>

Access to the Team Development application

</td><td>

A user with the admin role on the instance you are accessing

</td></tr><tr><td>

Right to [register a remote instance](../task/t_DefineARemoteInstance.md)

</td><td>

One of following:-   A user with the admin role on the instance you are registering
-   A user with the teamdev\_user role on the instance you are registering

</td></tr><tr><td>

Right to push changes to the parent instance from a development instance

</td><td>

One of following:-   A user with the admin role on the parent instance
-   A user with the teamdev\_user role on the parent instance

</td></tr><tr><td>

Right to compare to a registered remote instance

</td><td>

One of following:-   A user with the admin role on the registered development instance
-   A user with the teamdev\_user role on the registered development instance

</td></tr><tr><td>

Access to the [Code Review Requests](../task/t_EnableCodeReview.md) module

</td><td>

One of following:-   A user with the admin role on the parent instance
-   A user with the teamdev\_code\_reviewer role on the parent instance

</td></tr></tbody>
</table>**Note:** The teamdev\_user role does not grant access to the Team Development application and is not intended for developers to work on local development instances. It is intended to grant developers non-admin access to remote instances such as the parent instance or a peer development instance.

**Parent Topic:**[Team Development setup](../concept/c_SettingUpTeamDevelopment.md)

**Related topics**  


[Create an exclusion policy](../task/t_CreateAnExclusionPolicy.md)

[Define a remote instance](../task/t_DefineARemoteInstance.md)

[Enable a code review](../task/t_EnableCodeReview.md)

[Select the parent instance](../task/t_SelectTheParentInstance.md)

[Set up an instance hierarchy](../task/t_SetUpAnInstanceHierarchy.md)

