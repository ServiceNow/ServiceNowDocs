---
title: Components installed with Contextual Search
description: Several types of components are installed with the activation of the Contextual Search plugin \(com.snc.contextual\_search\), including tables and user roles.
locale: en-US
release: yokohama
product: Contextual Search
classification: contextual-search
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Contextual search plugin, Contextual search plugin, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Components installed with Contextual Search

Several types of components are installed with the activation of the Contextual Search plugin \(com.snc.contextual\_search\), including tables and user roles.

**Note:** The Application Files table lists the components that are installed with this application. For instructions on how to access this table, see [Find components installed with an application](../../plugins/task/find-components.md).

## Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Available Search Resource \[cxs\_search\_resource\]

</td><td>

List of available search resources used in configuration of searches.

</td></tr><tr><td>

Email Configuration \[cxs\_table\_email\_config\]

</td><td>

List of email notifications configured to have contextual search results attached.

</td></tr><tr><td>

Record Producer Configuration \[cxs\_rp\_config\]

</td><td>

List of record producers configured to have contextual search.

</td></tr><tr><td>

Relevant Document \[cxs\_relevant\_doc\]

</td><td>

Groups the Relevant Document Detail individual recorded actions by search session.**Note:** A new search session group is created every time you create or open a record or reload the page.

For more information on the table, refer [Feedback information on contextual search](r_QueryFeedbackInformation.md).

</td></tr><tr><td>

Relevant Document Detail \[cxs\_rel\_doc\_detail\]

</td><td>

List of individual recorded actions. For example, **Preview**, **This helped**, **Attach**, or **Order**. For more information on the table, refer [Feedback information on contextual search](r_QueryFeedbackInformation.md).

</td></tr><tr><td>

Search Context \[cxs\_context\_config\]

</td><td>

Search contexts for contextual search.

</td></tr><tr><td>

Search Field \[cxs\_table\_field\_config\]

</td><td>

All form fields that have contextual search configured to it.

</td></tr><tr><td>

Search Resource \[cxs\_search\_res\_config\]

</td><td>

Search resource configurations for the related searcher.

</td></tr><tr><td>

Search Resource Context Configuration \[cxs\_res\_context\_config\]

</td><td>

Conditions for this search context that restrict the results returned to a user.

</td></tr><tr><td>

Search Resource Context Property \[cxs\_res\_context\_config\_prop\]

</td><td>

Property values for search resource context configuration.

</td></tr><tr><td>

Search Resource Property \[cxs\_search\_res\_config\_prop\]

</td><td>

Property values for search resource searcher configuration.

</td></tr><tr><td>

Searcher Configuration \[cxs\_searcher\_config\]

</td><td>

Details of available search configurations.

</td></tr><tr><td>

Table Configuration \[cxs\_table\_config\]

</td><td>

Lists the tables configured for table configurations.

</td></tr><tr><td>

Wizard Configuration \[cxs\_wizard\_config\]

</td><td>

Lists the tables configured for wizard configurations.

</td></tr><tr><td>

Base UI Configuration \[cxs\_ui\_config\_base\]

</td><td>

Common elements for the record producer, table, and wizard configurations.

</td></tr></tbody>
</table>**Parent Topic:**[Contextual search plugin](../task/contextual-search-plugin.md)

