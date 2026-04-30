---
title: Data lookup and record matching support
description: The data lookup and record matching feature enables administrators to define rules that automatically set one or more field values when certain conditions are met.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering fields, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Data lookup and record matching support

The data lookup and record matching feature enables administrators to define rules that automatically set one or more field values when certain conditions are met.

Data lookup rules allow administrators to specify the conditions and fields where they want data lookups to occur. For example, on Incident forms, there are priority lookup rules for the sample data that automatically set the incident **Priority** based on the incident **Impact** and **Urgency** values.

**Note:** Activating the Data Lookup and Record Matching Support plugin replaces the **calculatePriority** business rule with a priority data lookup definition, but does not transfer any custom logic. If you manually activate the plugin, you must recreate any custom business logic that uses the priority lookup rules.

The following codes will be removed by manually activating the **com.glide.data\_lookup** plugin:

-   sys\_script\_18105ab0c61122750127a49c9055d29f
-   sys\_script\_client\_2bbac34da9fe1561000d89c04779a30c
-   sys\_script\_client\_2bc0bf4fa9fe15610019c5c8a8461647
-   sys\_script\_client\_ac0081210f030000b12e6903cfe012ac
-   ys\_script\_d1b7d4af4655e7c2001be4c18b99215a
-   sys\_script\_include\_9e1904840a0a0b7d00d5ee8d0e2d89ef

