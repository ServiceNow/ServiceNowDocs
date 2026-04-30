---
title: Domain Separated Tables
description: You can see at a glance which tables are domain-separated in your instance with the Domain Separated Tables feature.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Domain separation setup and administration, Domain separation for service providers, Access Management]
---

# Domain Separated Tables

You can see at a glance which tables are domain-separated in your instance with the Domain Separated Tables feature.

## Overview

Use the Domain Separated Tables feature to see which tables are domain-separated. Start typing "domain" in the **All** filter to access **Domain Separated Tables** in the left navigation pane.

You can filter this view to display or remove column names to look for certain properties or attributes that are included in your tables. There are two table types that display on the list:

-   Tables that have an explicit **sys\_domain** column present, where the **Column** name displays **sys\_domain** value in the list.
-   Tables that are using the **domain\_master** attribute to derive domain separation from a referenced record, where the **Attributes** column includes the **domain\_master=ref-field-value** value.

When you use the Show Matching or Filter Out selections on the Column name menu, you can view these two types of tables.

