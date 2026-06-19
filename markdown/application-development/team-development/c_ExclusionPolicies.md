---
title: Exclusion policies
description: You can exclude certain files from change tracking by creating an exclusion policy.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/team-development/c\_ExclusionPolicies.html
release: zurich
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Configure, Team Development, Planning your application, Building applications]
---

# Exclusion policies

You can exclude certain files from change tracking by creating an exclusion policy.

When a change matches an exclusion policy, the change doesn’t generate records in the local changes list. The change still generates local version records and update set records as normal.

**Note:** The exclusion policy applies to changes identified during a reconciliation operation. If you create an exclusion policy after a reconciliation, Team Development still tracks the changes until the next reconciliation.

-   **[Create an exclusion policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/t_CreateAnExclusionPolicy.md)**  
Application developers can create an exclusion policy to avoid pushes or pulls to specific instances in the team development hierarchy.

**Parent Topic:**[Configuring Team Development](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/configuring-team-development.md)

