---
title: Relationship between industrial standards and published standards
description: Industrial standards and published standards are stored in separate back-end tables. See how they relate. Choose the correct version of a standard depending on whether you need a specific version or the latest published one.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Industrial Standards, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Relationship between industrial standards and published standards

Industrial standards and published standards are stored in separate back-end tables. See how they relate. Choose the correct version of a standard depending on whether you need a specific version or the latest published one.

## Relationship overview

In the back end, two tables represent standards:

-   Industrial Standard \[sn\_icw\_std\_standard\]: Contains individual versions of standards. Use this table when working with a specific version, such as for reporting or historical analysis.
-   Published Industrial Standard \[sn\_icw\_std\_publ\_standard\]: Represents the most recently published version of a standard. Use this table when the goal is to reference the latest version.

## Working with specific and latest versions

When a task or report must reference a particular version of a standard, the Industrial Standard table is used. This method is common in reporting, where accuracy depends on the exact version that was active at the time.

In contrast, when the goal is to work across versions or use the most current configuration \(for example, in automation\), the Published Industrial Standard table is used. This type of query enables the system to dynamically reference the latest version without manual selection.

## Selecting standards across versions

Each record in the Industrial Standard table includes a reference to its corresponding published standard via the published\_standard field. This relationship enables queries to group or filter records by their published version.

For example, to retrieve all versions of a standard that belong to the same published group, query the Industrial Standard table where the published\_standard field matches the ID of the desired published standard. This approach supports cross-version reporting and automation by linking multiple versions to a single published reference.

**Parent Topic:**[Using Industrial Standards](using-industrial-standards.md)

