---
title: Granting access rights for the developers
description: To use Team Development, application developers must have a set of credentials for each instance in the Team Development hierarchy.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Team Development Reference, Team Development, Planning your application, Building applications]
---

# Granting access rights for the developers

To use Team Development, application developers must have a set of credentials for each instance in the Team Development hierarchy.

**Note:** The `teamdev_user` role doesn’t grant access to the Team Development application and isn’t intended for developers to work on local development instances. It’s intended to grant developers non-admin access to remote instances such as the parent instance or a peer development instance.

An instance's placement in the [team development hierarchy](../task/t_SetUpAnInstanceHierarchy.md) determines the credentials that it requires.

<table id="table_vnz_5jb_bq"><thead><tr><th>

Desired Access

</th><th>

Credential Requirements

</th></tr></thead><tbody><tr><td>

Access to the Team Development application

</td><td>

admin role on the instance you’re accessing

</td></tr><tr><td>

Right to [register a remote instance](../task/t_DefineARemoteInstance.md)

</td><td>

One of following:-   admin role on the instance you’re registering
-   teamdev\_user role on the instance you’re registering

</td></tr><tr><td>

Right to push changes to the parent instance from a development instance

</td><td>

One of following:-   admin role on the parent instance
-   teamdev\_user role on the parent instance

</td></tr><tr><td>

Right to compare to a registered remote instance

</td><td>

One of following:-   admin role on the registered development instance
-   teamdev\_user role on the registered development instance

</td></tr><tr><td>

Access to the [Code Review Requests](../task/t_EnableCodeReview.md) module

</td><td>

One of following:-   admin role on the parent instance
-   teamdev\_code\_reviewer role on the parent instance

</td></tr></tbody>
</table>**Parent Topic:**[Team Development Reference](team-development-reference.md)

