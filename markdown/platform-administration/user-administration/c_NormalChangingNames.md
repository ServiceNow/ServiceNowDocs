---
title: Changing normalized company names
description: You can change a normalized company name several different ways. In all cases, that change affects all normalized fields referring to that company.You can change normalized company names by editing records in the Normalized Company Name table.
locale: en-US
release: xanadu
product: User Administration
classification: user-administration
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Normalization data services, Creating users, companies, and departments, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Changing normalized company names

You can change a normalized company name several different ways. In all cases, that change affects all normalized fields referring to that company.

You have several options for changing a normalized company name:

-   Edit the Normalized Name field in the Normalized Mappings table. This method is preferred.
-   Edit the Normalized Company name table.
-   Edit the Company Name field on any table that refers to the Company \[core\_company\] table.

**Warning:** If you edit a field whose value is a normalized name, you change the normalized name for ALL discovered names that map to it.

**Parent Topic:**[Normalization data services](c_NormalizationOverview.md)

## Change a normalized company name

You can change normalized company names by editing records in the Normalized Company Name table.

### Before you begin

Role required: admin

### About this task

You can add and edit records in the Normalized Company Names table.

### Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Normalization Data Services** &gt; **Normalized Mappings**.

2.  Find the record with the name that you want to replace and edit the Normalized name field.

    The system changes the Normalized Company name for every discovered name that maps to that normalized name.


