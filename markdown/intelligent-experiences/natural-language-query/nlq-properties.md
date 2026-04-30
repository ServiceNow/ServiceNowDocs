---
title: NLQ properties
description: The Natural Language Query \(NLQ\) properties control how and where NLQ operates.
locale: en-US
release: xanadu
product: Natural Language Query
classification: natural-language-query
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Natural Language Query References, Natural Language Query, Enable AI experiences]
---

# NLQ properties

The Natural Language Query \(NLQ\) properties control how and where NLQ operates.

Admins can edit properties of NLQ by navigating to **All** &gt; **System Properties** &gt; **All Properties**. Filter for the NLQ properties.

**Note:** Editing these system properties requires the admin role. The nlq\_admin role does not have permission to edit records in this table.

![System properties filtered for NLQ properties.](../images/nlq-propertiesT1.png)

<table id="table_xvc_v1z_spb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.listv2.nlq.lists.append\_query

</td><td>

-   True: NLQ inputs add onto existing queries via an "and" operator
-   False: New NLQ input replaces any existing queries

 Example: You run two queries.

-   Query 1: Incidents with critical priority
-   Query 2: assigned to John Smith

If the property is set to true, the results show incidents with critical priority that are assigned to John Smith. If the property is set to false, the results show only items assigned to John Smith.

</td></tr><tr><td>

com.snc.listv2.nlq.lists.enabled

</td><td>

-   True: Enables NLQ search option for List v2
-   False: Removes NLQ search option for List v2

</td></tr><tr><td>

com.snc.nlq.gai\_enabled

</td><td>

-   True: The Now LLM Service fallback is available
-   False: The Now LLM Service fallback is not available

 Initially, queries are interpreted using a rules-based method. If that method fails, queries are passed to the Now LLM Service as a fallback. Queries that fail both of these methods are marked as unsuccessful in the NLQ log.

</td></tr><tr><td>

com.snc.par.nlq.report\_designer.enabled

</td><td>

-   True: Enables NLQ in Report Designer
-   False: Removes NLQ in Report Designer

</td></tr><tr><td>

glide.cmdb.query.nlq.activated

</td><td>

-   True: NLQ search feature is active in CMDB Query Builder
-   False: NLQ search feature is inactive in CMDB Query Builder

</td></tr><tr><td>

glide.service\_portal.ais\_nlq\_enabled

</td><td>

-   True: Enables NLQ in global search
-   False: NLQ is not available in global search

</td></tr></tbody>
</table>**Parent Topic:**[Natural Language Query References](nlq-references.md)

**Related topics**  


[Natural Language Query roles](natural-language-query-roles.md#)

