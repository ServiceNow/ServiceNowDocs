---
title: Data classification for Install Base Management
description: Enable customers to automatically classify sensitive data for their workflows. After data is classified, users can view the type of classification associated to different fields, whether internal, restricted, confidential, or public.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Reference, Customer Service Management]
---

# Data classification for Install Base Management

Enable customers to automatically classify sensitive data for their workflows. After data is classified, users can view the type of classification associated to different fields, whether internal, restricted, confidential, or public.

|Table|Field|Plugin from which the field is coming|Classification|
|-----|-----|-------------------------------------|--------------|
|Sold product table \(sn\_install\_base\_sold\_product\)|offering\_type|Product Catalog Management core \(sn\_prd\_pm\)|Internal|
|Sold product table \(sn\_install\_base\_sold\_product\)|relationship\_type|Product Catalog Management core \(sn\_prd\_pm\)|Internal|
|Sold product table \(sn\_install\_base\_sold\_product\)|unit\_of\_measurement|Product Catalog Management core \(sn\_prd\_pm\)|Confidential|
|Sold product table \(sn\_install\_base\_sold\_product\)|product\_specification|Product Catalog Management core \(sn\_prd\_pm\)|Internal|
|Sold product table \(sn\_install\_base\_sold\_product\)|periodicity|Product Catalog Management core \(sn\_prd\_pm\)|Confidential|
|Sold product table \(sn\_install\_base\_sold\_product\)|pricing method|Product Catalog Management core \(sn\_prd\_pm\)|Confidential|
|Sold product table \(sn\_install\_base\_sold\_product\)|prd\_offering|Product Catalog Management core \(sn\_prd\_pm\)|Internal|
|Sold product table \(sn\_install\_base\_sold\_product\)|service\_offering|Customer Service with Service Portfolio Management \(snc.csm\_spm\)|Internal|
|Sold product table \(sn\_install\_base\_sold\_product\)|household|Customer Household Data Model \(com.snc.household\)|Confidential|
|Sold product table \(sn\_install\_base\_sold\_product\)|service\_organization|Service Organization \(com.snc.service\_organization\)|Confidential|
|Sold product table \(sn\_install\_base\_sold\_product\)|provider\_service\_organization|Service Organization \(com.snc.service\_organization\)|Confidential|
|Install base table \(sn\_install\_base\_item\)|household|Customer Household Data Model \(com.snc.household\)|Confidential|
|Install base table \(sn\_install\_base\_item\)|service\_context|Proactive Customer Service Operations with Event Management \(snc.proactive\_cs\_itom\)|Internal|
|Install base table \(sn\_install\_base\_item\)|health\_status\_last\_updated|Proactive Customer Service Operations with Event Management \(snc.proactive\_cs\_itom\)|Internal|
|Install base table \(sn\_install\_base\_item\)|service\_context|Proactive Customer Service Operations with Event Management \(snc.proactive\_cs\_itom\)|Internal|
|Install base table \(sn\_install\_base\_item\)|health\_status|Proactive Customer Service Operations with Event Management \(snc.proactive\_cs\_itom\)|Confidential|
|Install base table \(sn\_install\_base\_item\)|service\_organization|Service Organization \(com.snc.service\_organization\)|Confidential|

