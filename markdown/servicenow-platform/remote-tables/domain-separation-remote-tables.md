---
title: Domain separation and remote tables
description: Domain separation is unsupported in remote tables. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
locale: en-US
release: australia
product: Remote Tables
classification: remote-tables
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Remote tables, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and remote tables

Domain separation is unsupported in remote tables. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: No support

-   The domain field may exist on data tables but there is no business logic to manage the data.
-   This level is not considered domain-separated.

For more information on support levels, see [Application support for domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-separated-apps.md).

## Domain Separation Overview

Domain separation provides complete data isolation for domain-specific users.

## How domain separation works with remote tables

When you create standard internal tables, you can add a sys\_domain field, which results in domain separation of the data that is stored in the table. This functionality is not supported when you natively create remote tables, which results in lack of domain separation for rows that are added to a remote table.

However, script definitions that you create and associate with a remote table can be domain \(data\) separated. When you create the script, you can include DomainSupport APIs that provide domain separation support. If the script definition is domain separated, only users that belong to the designated domain can view the data in the remote table.

**Parent Topic:**[Remote tables](remote-tables.md)

**Related topics**  


[Create script definitions for a remote table](../task/create-remote-table-script.md)

[Domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/domain-sep-landing-page.md)

