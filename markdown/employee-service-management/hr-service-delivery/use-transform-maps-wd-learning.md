---
title: Use transform maps
description: Transform maps specify data relationships between source table and target table.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using HR Service Delivery Integration with Workday Learning, HR Service Delivery Integration with Workday Learning, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Use transform maps

Transform maps specify data relationships between source table and target table.

For details on the transform maps, navigate to **System Import Sets** &gt; **Administration** &gt; **Transform Maps**.

|Name|Description|
|----|-----------|
|Workday Learning User Mapping|Maps users profiles from the user Profile Staging \[sn\_lrn\_workday\_user\_mapping\_staging\] table to the User Profile \[sn\_lc\_user\_mapping\] table.|
|Workday Learning Courses|Maps workday learning courses from Staging \[sn\_lrn\_workday\_course\_staging\] table to the Learning External Content \[sn\_lc\_external\_content\] table.|
|Workday Learning Offering Lessons|Maps the Workday Learning Offering Lessons from the Staging \[sn\_lrn\_workday\_offering\_lessons\_staging\]|
|Workday Learning User Course Activity|Maps user course activity from the Staging \[sn\_lrn\_workday\_user\_course\_activity\_staging\] table to the Learning User Course Activity \[sn\_lc\_user\_course\_activity\] table.|
|Workday Learning Todos|Maps to-dos from the Workday Learning Todos Staging \[sn\_lrn\_workday\_todos\_staging\] table to the Workday Learning Todos \[sn\_lrn\_workday\_todos\] table.|
|Workday Learning User Course Self Enrollment|Maps user self enrollment information from the Staging \[sn\_lrn\_workday\_user\_course\_self\_enrollment\_staging\] to the Learning User Course Activity \[sn\_lc\_user\_course\_activity\] table.|
|Workday Learning Course Offering|Maps learning course offerings from the Staging \[sn\_lrn\_workday\_course\_offering\_staging\] to the Collection \[sn\_lc\_collection\] table.|
|Workday Learning Collection Courses|Maps the Workday Learning Collection from the Staging \[sn\_lrn\_workday\_collection\_staging\] to the Collection \[sn\_lc\_collection\] table.|
|Workday Learning Program Courses|Maps learning program courses from the Staging \[sn\_lrn\_workday\_program\_courses\] to the Collection Course Item \[sn\_lc\_m2m\_collection\_course\_item\] table.|

**Parent Topic:**[Using HR Service Delivery Integration with Workday Learning](using-workday-learning-intg.md)

**Related topics**  


[View user activity for Workday Learning](../task/sync-user-actitvity-wdl-intg.md)

[View track approval for Workday Learning](../task/track-approval-adl-intg.md)

[Import set tables in HR Service Delivery Integration with Workday Learning](import-set-tables.md)

