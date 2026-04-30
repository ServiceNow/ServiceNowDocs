---
title: Recent selections
description: Reference fields store a list of each user's recent selections to enable you to quickly select past values when filling in a reference field.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Recent selections

Reference fields store a list of each user's recent selections to enable you to quickly select past values when filling in a reference field.

By default, the system stores up to 15 selections from a reference field for each user in the Recent Selection \[sys\_ui\_recent\_selection\] table. You can see the recent selections list by selecting an empty reference field.

**Note:**

-   The system doesn't store recent selections for Service Catalog reference variables.
-   Recent selections aren't available in the Service Portal or mobile user interfaces.

![An empty reference field to the User table displaying a list of two recent user selections: Beth Anglin and Elmo Gabouer.](../image/RecentSelections.png "Recent selections")

The system uses auto-complete to filter the list of recent selections to match the values that you enter.

![A partially-filled in reference field to the User table displaying a filtered list of users whose names begin with the letter B.](../image/RecentSelectionsFiltered.png "Recent selections filtered")

The system adds a Recent Selection record whenever you insert or update a reference field value. Administrators can control the number of recent selections the system displays with the **glide.xmlhttp.max\_choices** system property. Setting the property to zero disables recent selections.

**Note:**

-   The **glide.xmlhttp.max\_choices** property also controls the number of entries the system displays in lists.
-   For information on clearing recent selections, see the [How to clear out the "Recent Selections" that appears up on the reference fields. \[KB0747334\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0747334) article in the Now Support Knowledge Base.

**Related topics**  


[Available system properties](../../reference-pages/reference/r_AvailableSystemProperties.md#)

