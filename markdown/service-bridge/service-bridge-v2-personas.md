---
title: User roles for providers
description: Learn about the roles, skills, and tasks for the different users in the Service Exchange for Providers application.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Install and configure for provider, Service Exchange for Providers, Service Exchange]
---

# User roles for providers

Learn about the roles, skills, and tasks for the different users in the Service Exchange for Providers application.

A user role is a pre-configured role in the application that is made up of multiple granular roles. The user roles are designed to correspond to the common job titles for managers, analysts, and service owners in an IT organization. If you want your users and groups to have more access than a role permits, you can add more granular roles to your users and groups. If you want to limit the access for specific users and groups at the task level, you can remove the granular roles. You can also build custom roles and access controls \(ACLs\) to suit your needs.

<table id="table_skr_1km_cmb"><thead><tr><th>

Persona

</th><th>

Skills

</th><th>

Tasks

</th><th>

Roles

</th></tr></thead><tbody><tr><td>

Developer

</td><td>

-   Is a certified ServiceNow administrator
-   Is a certified ServiceNow application developer

</td><td>

-   Creates provider connection records.
-   Creates and maintains remote task definitions and transforms.
-   Creates and maintains Workflow Studio flows to determine the request fulfillment processes.
-   Creates and maintains remote record producers.

</td><td>

-   admin
-   sn\_sb.admin

 **Note:** If the user does not have the admin role, the catalog admin role is required to modify and publish Remote Record Producers.

</td></tr><tr><td>

Administrator

</td><td>

Is a certified ServiceNow system administrator

</td><td>

-   Completes the Service Exchange registration requests.
-   Assists the consumer's system administrator as needed.
-   Publishes remote catalogs to the consumer's instance.
-   Publishes remote task definitions to the consumer's instance.
-   Troubleshoots Service Exchange transport payloads.

</td><td>

-   admin
-   sn\_sb.admin
-   sn\_transport.admin

</td></tr><tr><td>

Provider Fulfiller

</td><td>

Has agent skills

</td><td>

-   Resolves consumer questions and issues.
-   Engages in network operations when needed.

</td><td>

-   \*itil
-   sn\_sb.requestor
-   \*sn\_customerservice\_agent
-   \*incident\_read​
-   \*problem\_read​
-   \*change\_read

</td></tr><tr><td>

Consumer Requestor

</td><td>

End user

</td><td>

Makes requests from the Remote Catalog

</td><td>

sn\_sb.requestor

</td></tr></tbody>
</table>