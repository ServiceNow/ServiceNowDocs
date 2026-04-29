---
title: Create a talent type
description: Create an implementation in the talent profile scripted extension point to add a new talent type.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Talent Profile, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Create a talent type

Create an implementation in the talent profile scripted extension point to add a new talent type.

## Before you begin

Role required: sn\_ta\_hiring\_core.admin/ sn\_ta\_tp.talent\_profile\_admin

## About this task

The Talent profile extension point has four default implementations that pull in data of different talent types to the talent profiles. You can use the default settings available or create implementations, depending on your organizational requirements.

## Procedure

1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

2.  Search for sn\_ta\_tp.TalentProfileExtPoint extension point and select to open it.

    **Note:** The extension point must be opened within the Talent profile application scope.

    You have four default implementations.

    |Extension point|Extension class|Description|
    |---------------|---------------|-----------|
    |sn\_ta\_tp.TalentProfileExtPoint|TalentProfileExtPointDefault|Extension point for default or unspecified talent profiles.|
    |sn\_ta\_tp.TalentProfileExtPoint|TalentProfileExtPointAlumni|Extension point for the talent type, alumni.|
    |sn\_ta\_tp.TalentProfileExtPoint|TalentProfileExtPointEmployee|Extension point for the talent type, employee.|
    |sn\_ta\_tp.TalentProfileExtPoint|TalentProfileExtPointCandidate|Extension point for the talent type, external candidate.|

3.  Select the **Create implementation** related link to create an implementation.

4.  On the Create implementation form, fill in the fields.

    For a description of the field values, see [Create implementation form](../reference/implementation-ref-ta-tp.md).


## Result

You've created an implementation for the sn\_ta\_tp.TalentProfileExtPoint extension point. Use it to have a customized talent type.

**Parent Topic:**[Configuring Talent profile](../concept/config-tp.md)

