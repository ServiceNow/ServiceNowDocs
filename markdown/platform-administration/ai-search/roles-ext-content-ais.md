---
title: External Content for AI Search roles
description: External Content for AI Search includes the following roles.Access endpoints for AI Search external content APIs.Access High Security settings for AI Search.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# External Content for AI Search roles

External Content for AI Search includes the following roles.

To learn more about managing subscriptions, see [Managing per-user subscriptions in Subscription Management](../../subscription-management/concept/managing-user-subscriptions-v2.md) and contact your account representative.

**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

## AI Search external content API user \[ais\_external\_content\]

Access endpoints for AI Search external content APIs.

-   Feeds external documents for AI Search to index as search results, or deletes records for external documents from the index, using the [External Content Ingestion API](https://www.servicenow.com/docs/access?context=external-content-ingestion-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).
-   Imports user mappings for external content security using the [AI Search External User Mapping API](https://www.servicenow.com/docs/access?context=ext-user-mapping-api&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Assign this role to non-interactive users and integration users who require access to external content API endpoints. For more information on non-interactive users, see [Non-interactive sessions](../../users-and-groups/concept/c_NonInteractiveSessions.md#). For details on integration users, see [Mark service accounts as internal integration users](https://www.servicenow.com/docs/access?context=t_MarkSvcAcctsAsInternalIntegUsers&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

Users with the admin role don't need this role to access external content API endpoints.

## AI Search high security administrator \[ais\_high\_security\_admin\]

Access High Security settings for AI Search.

-   Bypasses all search filters from search sources and content security in the Search Preview UI, viewing all search query results available in the AI Search index
-   Reads external content user mapping import history records

### Contains Roles

List of roles contained within the role.

None.

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

This is an elevated privilege role. Elevated privilege roles aren't assigned to users or groups, and must be used by elevation. For more information on elevated privilege roles, see [Elevated privilege roles](https://www.servicenow.com/docs/access?context=c_ElevatedPrivilege&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US). To learn about elevation, see [Elevate to a privileged role](https://www.servicenow.com/docs/access?context=t_ElevateToAPrivilegedRole&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

The Instance Security Center **Users with High Privilege Roles** user metric displays the count of users assigned this role. For more details, see [User metrics](https://www.servicenow.com/docs/access?context=instance-sec-center-user-metrics&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

