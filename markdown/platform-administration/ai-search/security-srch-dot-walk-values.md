---
title: Security for searchable referenced table field values in AI Search
description: When a user searches referenced table field values that you have indexed for search with the searchable\_dot\_walk\_fields field setting, only field values that the user can view appear in the search results. The system uses a field value's role-based access control list rules \(ACLs\) to determine whether the search user can view that field value.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-search/security-srch-dot-walk-values.html
release: zurich
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-07-28"
reading_time_minutes: 1
breadcrumb: [Field settings, Indexed sources, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Security for searchable referenced table field values in AI Search

When a user searches referenced table field values that you have indexed for search with the **searchable\_dot\_walk\_fields** field setting, only field values that the user can view appear in the search results. The system uses a field value's role-based access control list rules \(ACLs\) to determine whether the search user can view that field value.

Searchable referenced table field values that have condition-based or script-based ACLs or user criteria don't appear in search results.

For searchable field values indexed through multiple dot-walk reference levels, the system only considers role-based ACLs on the final field value. As an example, if you index `company.contact.name` referenced table field values for search, user access to **name** field values isn't affected by role-based ACLs on **contact** field values.

To bypass all ACLs and allow users to search for all searchable referenced table field values, you can set the **glide.ais.query.allow\_indexlookup\_for\_dotwalk** system property to true. This bypasses ACL evaluation for field values indexed via the **dot\_walk\_fields** and **searchable\_dot\_walk\_fields** field settings.

For more details on ACL types and configuration, see [Access control list rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/access-control/access-control-rules.md).

**Parent Topic:**[Field settings for AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-search/field-settings-ais.md)

