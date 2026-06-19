---
title: Versions and local changes
description: Version records track changes to a customizable record over time so that you can compare or revert to a specific version later.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/team-development/c\_VersionsAndLocalChanges.html
release: zurich
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Working with version records, Team Development, Planning your application, Building applications]
---

# Versions and local changes

Version records track changes to a customizable record over time so that you can compare or revert to a specific version later.

A version record is created every time a developer changes a customizable record, so a single record can have multiple version records associated with it. A local change record is created or updated to reference the current version every time a developer modifies a customizable record. A single record can have only one local change record associated with it.

Local change records track customized records that have changes on the development instance that aren’t on the parent instance. This process enables you to collect changes in preparation for a push.

\[Omitted image "team-development-versions.png"\] Alt text: team development instance hierarchy and workflow

Developers can back out a local change to restore a previous version of a customizable record. The back out action sets the local customizable record to the last revision identified by a reconciliation action.

-   **[Version record navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/c_NavigatingVersionRecords.md)**  
There are a variety of methods for viewing a list of versions for an object.
-   **[Versions transferring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/c_TransferringVersions.md)**  
Administrators transfer version records between instances by moving customizations with update sets or the Team Development application.

**Parent Topic:**[Working with version records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/team-development/c_Versions.md)

