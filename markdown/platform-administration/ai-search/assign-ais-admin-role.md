---
title: Assign roles to AI Search administrators and users
description: Grant users the ais\_admin, ais\_external\_content, ais\_high\_security\_admin, and search\_application\_admin roles so they can configure and manage settings and content for AI Search and search applications.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-28"
reading_time_minutes: 2
breadcrumb: [Configure, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Assign roles to AI Search administrators and users

Grant users the ais\_admin, ais\_external\_content, ais\_high\_security\_admin, and search\_application\_admin roles so they can configure and manage settings and content for AI Search and search applications.

## Before you begin

Role required: admin

## About this task

Users with the following roles can access and configure settings and content for the AI Search application.

<table id="table_n3c_3l3_wnb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Search administrator \[ais\_admin\]

</td><td>

Manages configuration settings for the AI Search application, including the following:

-   Creates, reads, updates, and deletes indexed sources
-   Creates, reads, updates, and deletes search sources
-   Creates and deletes mappings between search sources and search profiles
-   Creates, reads, updates, and deletes search profiles
-   Creates, reads, updates, and deletes synonym and stop word dictionaries
-   Creates and deletes mappings between dictionaries and search profiles
-   Reads and updates typo handling auto-correction dictionaries linked to search profiles
-   Creates, reads, updates, and deletes Genius Result configurations
-   Creates and deletes mappings between Genius Result configurations and search profiles
-   Creates, reads, updates, and deletes result improvement rules
-   Creates and deletes mappings between result improvement rules and search profiles

</td></tr><tr><td>

AI Search high security administrator \[ais\_high\_security\_admin\]

</td><td>

Accesses High Security settings for AI Search, including the following:

-   Bypasses all search filters from search sources and content security in the Search Preview UI, viewing all search query results available in the AI Search index
-   Reads external content user mapping import history records

 This is an elevated privilege role. Elevated privilege roles aren't assigned to users or groups, and must be used by elevation. For more information on elevated privilege roles, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US). To learn about elevation, see [Elevate to a privileged role](https://www.servicenow.com/docs/access?context=t_ElevateToAPrivilegedRole&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

 The Instance Security Center **Users with High Privilege Roles** user metric displays the count of users assigned this role. For more details, see [User metrics](https://www.servicenow.com/docs/access?context=instance-sec-center-user-metrics&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Search application administrator \[search\_application\_admin\]

</td><td>

Creates, reads, updates, and deletes search application configurations for Zing and AI Search.

 This role includes the ais\_admin and personalize\_dictionary roles.

</td></tr><tr><td>

AI Search external content API user \[ais\_external\_content\]

</td><td>

Accesses endpoints for AI Search external content APIs, including the following:

-   Feeds external documents for AI Search to index as search results, or deletes records for external documents from the index, using the [External Content Ingestion API](https://www.servicenow.com/docs/access?context=external-content-ingestion-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).
-   Imports user mappings for external content security using the [AI Search External User Mapping API](https://www.servicenow.com/docs/access?context=ext-user-mapping-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

 Assign this role to non-interactive users and integration users who require access to external content API endpoints. For more information on non-interactive users, see [Non-interactive sessions](../../users-and-groups/concept/c_NonInteractiveSessions.md#). For details on integration users, see [Mark service accounts as internal integration users](https://www.servicenow.com/docs/access?context=t_MarkSvcAcctsAsInternalIntegUsers&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

 Users with the admin role don't need this role to access external content API endpoints.

</td></tr></tbody>
</table>Assign these roles to users and groups to enable them as search administrators or external content API users for AI Search.

## Procedure

-   [Assign a role to a user](../../users-and-groups/task/t_AssignARoleToAUser.md)

-   [Assign a role to a group](../../roles/task/t_AssignRoleToGroup.md)


**Parent Topic:**[Configuring AI Search](../concept/configuring-ais.md)

