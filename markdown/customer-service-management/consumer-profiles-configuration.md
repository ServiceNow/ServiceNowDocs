---
title: Creating multiple consumer profiles for a user
description: The concept of consumer profiles refers to the idea that an individual can have multiple profiles associated with them. For example, a consumer might have a patient profile in Healthcare and Life Sciences and simultaneously have a constituent profile in Public Sector Digital Services.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure consumers, Customer data, Set up your environment, Configure, Customer Service Management]
---

# Creating multiple consumer profiles for a user

The concept of consumer profiles refers to the idea that an individual can have multiple profiles associated with them. For example, a consumer might have a patient profile in Healthcare and Life Sciences and simultaneously have a constituent profile in Public Sector Digital Services.

Starting with the Utah release, Customer Service Management \(CSM\) introduced the consumer profile \(sn\_csm\_consumer\_profile\) table with a reference to the consumer \(csm\_consumer\) table to define and support consumer profiles. When creating multiple profiles for a user within Customer Service Management \(CSM\), each profile can have its own set of fields and relational data like sold products, cases, interactions, and installed bases. By creating and defining consumer profiles, you can identify and differentiate profile-specific data.

Industries must use the consumer\_profile column on case \(sn\_customerservice\_case\), sold product \(sn\_install\_base\_sold\_product\), install base item \(sn\_install\_base\_item\), interaction \(interaction\), or child tables for any transactional data. Industries can extend the consumer profile \(sn\_csm\_consumer\_profile\) table for any industry-specific use case.

