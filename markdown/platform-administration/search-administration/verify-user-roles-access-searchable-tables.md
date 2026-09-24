---
title: Verify that user roles have access to your searchable tables
description: Evaluate your Zing text index configurations to see whether any user roles lack access to indexed columns in your searchable tables. The checker tool provides guidance on correcting access issues for each affected table's index.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/search-administration/verify-user-roles-access-searchable-tables.html
release: brazil
product: Search Administration
classification: search-administration
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Verify that user roles have access to your searchable tables

Evaluate your Zing text index configurations to see whether any user roles lack access to indexed columns in your searchable tables. The checker tool provides guidance on correcting access issues for each affected table's index.

## Before you begin

Role required: ts\_admin

## About this task

Starting with the Brazil release, Zing text search and indexing honors column-level query\_range read ACLs on table columns that are indexed for search. This change was made as part of improvements to security for search. In previous releases, Zing only honored table-level read ACLs.

This change affects searchable tables with text indexes that use the v3 legacy format and older formats. A user role may grant access to such a table without granting query\_range access to all of that table's indexed columns. In this case, Zing returns no results when users with the role search the table.

The Text Search Query Range ACL Checker tool helps you see which user roles are affected by this behavior change. It shows whether Zing currently honors query\_range ACLs for each of your searchable tables. You can evaluate the configuration for each table. Evaluation shows whether any user roles that grant access to the table lack query\_range access to all of its indexed columns. If this is the case, the tool provides guidance on modifying your configuration to resolve the search access issue. You can also accept the configuration as is, with the understanding that doing so will impact search for users with affected roles.

You only need to perform this procedure for text indexes that use the legacy v3 format or earlier formats. Zing's v4 text index format enforces query\_range read ACLs at the level of individual columns. Using the v4 format, when an indexed column is inaccessible by the search user, search ignores that column but still returns results from accessible indexed columns.

**Note:** To check the format for a searchable table's text index, navigate to **All** &gt; **System Definition** &gt; **Text Indexes**, find the record for your searchable table, and find the value of its **Format** field.

## Procedure

1.  In your web browser, navigate to the Text Search Query Range ACL Checker page at `https://<instance-name>.service-now.com/ts_query_range_acl_checker.do`, replacing `<instance-name>` with the name of your ServiceNow AI Platform® instance.

2.  In the **Text Search V3 Tables Restricted Search Status** section, use the **Index Name** filter and **Query Range ACL enforced** drop-down menu to locate the text search index for a searchable table.

    A value of **Enabled** in the **Query Range ACL enforced** column means the table's text index currently honors column-level query\_range ACLs. This configuration provides better security, but blocks searches by users with roles that lack query\_range access to all of the table's indexed columns.

    A value of **Disabled** means the table's text index doesn't currently honor column-level query\_range ACLs. This configuration offers less security, but doesn't block searches by users with roles that lack query\_range access to all of the table's indexed columns.

3.  Select **Evaluate**.

    An **Evaluation Result for &lt;table-name&gt;** section appears for your chosen table.

4.  In the **Evaluation Result for &lt;table-name&gt;** section, review the list of user roles which lack access to one or more columns in the chosen table's text index.

    The entry for a user role includes a list of columns on the chosen table that are inaccessible by users with the role. It also lists the ACLs that block access to those columns. Each ACL entry is a link to the relevant record in the Access Control \[sys\_security\_acl\] table.

5.  In the **Options to address blocking ACLs** section, choose one of the listed options and follow the tool's guidelines to resolve the access blockage for the listed user roles.

    -   Mark the inaccessible columns as unrestricted.

        **Note:** This option reduces security for search. Unrestricted columns can be searched by any user regardless of their role.

    -   Modify the ACLs that prevent access.

        Add the listed user roles to the existing ACLs, granting them access to the specified columns on the chosen table.

        **Note:** If you prefer, you can instead create additional ACLs that grant the listed roles access to the specified columns on the chosen table.

    -   Upgrade the table's text index format to v4.

        Using the v4 text index format, search ignores any blocked columns but still returns results from accessible columns, rather than returning no results if any column is blocked.

        **Note:** Upgrading a searchable table's text index to v4 may increase the space required for the index. The v4 index may rank results differently than the index with the previous format.

6.  To accept the current text index configuration, select **Enable Restricted Search in &lt;table-name&gt;**, where `<table-name>` is the name of your chosen table.

    **Note:** If you haven't resolved the access blockages reported for the table, users with the listed roles will be unable to search the table once you enable restricted search.


**Parent Topic:**[Zing text indexing and search engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/search-administration/c_ZingTextSearch.md)

**Related topics**  


[Features of Zing text indexing and search engine]()

[Available search options]()

[Global search finds records from multiple tables]()

[Zing generates search results in four phases]()

[Zing filters search results with access controls]()

[Zing computes document scores using three components]()

[Zing indexes words]()

[Zing can include attachments in search results]()

[Zing removes stop words from queries]()

[Zing matches derived words with stemming]()

[Zing can expand search results with synonyms]()

[Zing displays search suggestions as users enter search terms]()

[Installed with Zing]()

