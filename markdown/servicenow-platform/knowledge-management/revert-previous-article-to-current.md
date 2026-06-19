---
title: Revert an outdated article to the current state
description: Use an outdated version of an article to create a new version.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/knowledge-management/revert-previous-article-to-current.html
release: zurich
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use article versioning, Using Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Revert an outdated article to the current state

Use an outdated version of an article to create a new version.

## Before you begin

Roles required: knowledge\_admin or knowledge\_manager \(for the knowledge base containing the article\)

**Note:** If you're using ownerships groups, members of the ownership group for an article \(who also have the knowledge role\) can revert articles to a previous version. For more information, see [Ownership groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/knowledge-management/enable-ownership-group.md).

## About this task

This action is available for earlier published versions that have a state of **Outdated** and only when there is no checked out version. If a version has been checked out, the **Make this current** button does not appear on the Knowledge form header.

## Procedure

1.  Navigate to **Knowledge** &gt; **Articles** &gt; **All**.

2.  Open an article in the **Outdated** state.

3.  Select **Make this current** in the Knowledge form header.

    \[Omitted image "MakeCurrent.png"\] Alt text: Knowledge article record in outdated state with make this current button highlighted.

    The system displays the Knowledge form. The version number increments to the latest version number plus 0.01 and the state changes to **Draft**. For example, if the latest published version of an article is 3.0 and you select the outdated 1.0 version to become the current version, the version number increments to 3.01.


**Parent Topic:**[Use article versioning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/knowledge-management/use-article-versioning_0.md)

