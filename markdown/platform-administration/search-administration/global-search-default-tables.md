---
title: Default display fields for global search tables
description: Multiple tables are enabled for global search in the base system. Each global search table has its own set of fields included in the table's default text\_search list view. The system uses fields from this view to format global search results from these tables.
locale: en-US
release: australia
product: Search Administration
classification: search-administration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Text search views control format of global search results for tables, Global search finds records from multiple tables, Zing text indexing and search engine, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Default display fields for global search tables

Multiple tables are enabled for global search in the base system. Each global search table has its own set of fields included in the table's default text\_search list view. The system uses fields from this view to format global search results from these tables.

|Table|Display fields|
|-----|--------------|
|Catalog Item \[sc\_cat\_item\]|Short description, Description, Category, Price|
|Catalog Task \[sc\_task\]|Short description, Description, Number, Priority, State, Assignment group, Request item|
|Change \[change\_request\]|Short description, Description, Number, Type, Assignment group, State, Risk, Priority|
|Change Task \[change\_task\]|Short description, Description, Number, Type, State, Assignment group|
|Company \[core\_company\]|Name, Street, City, Zip / Postal code, Phone|
|Group \[sys\_user\_group\]|Name, Description, Type|
|Incident \[incident\]|Short description, Description, Number, Opened, Caller, Priority, State, Category, Assignment group|
|Knowledge \[kb\_knowledge\]|Short description, Article body, Category, Number, Updated|
|Problem \[problem\]|Problem statement, Description, Number, State, Resolution code, Assignment group, Configuration item, Related Incidents|
|Request \[sc\_request\]|Short description, Number, Requested for, State, Opened by|
|Requested Item \[sc\_req\_item\]|Number, Item, Stage, State, Requested for, Opened by, Opened|
|User \[sys\_user\]|Name, Email, Company, Department, Title|

**Parent Topic:**[Text search views control format of global search results for tables](../concept/text-search-view-formats-results.md)

