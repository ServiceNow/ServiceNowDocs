---
title: Multi-vaccine appointment bookings configuration
description: Administer multi-vaccine appointment bookings based on auto-selection and manual selection of the vaccine method. You can select your preferred vaccine method based on the eligibility criteria, order of method selection, and inventory availability.
locale: en-US
release: zurich
product: Vaccine Administration Management
classification: vaccine-administration-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Vaccine Administration Management, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Multi-vaccine appointment bookings configuration

Administer multi-vaccine appointment bookings based on auto-selection and manual selection of the vaccine method. You can select your preferred vaccine method based on the eligibility criteria, order of method selection, and inventory availability.

You can manage multi-vaccine appointment bookings after making configuration changes to the Vaccine Administration Management system properties. Multi-vaccine functionality can be broadly categorized into auto-selection of the vaccine method and manual selection of the vaccine method.

**Note:** If your first appointment has been completed, you can’t change the method. However, you have the flexibility to change the method while rescheduling your first dose. While rescheduling your appointment, if you change the method, it automatically applies to the second dose as well.

Among other criteria, the multi-vaccine method also supports age-based eligibility and assignment by specifying the age groups in the eligibility criteria for the method. The list of methods is visible only if you’re eligible for more than one vaccine method.

For example, say that only age groups over 60 are eligible to receive the Pfizer vaccine. If you aren’t in this age group, you won’t be assigned the Pfizer vaccine despite availability. Instead, the system evaluates other methods that meet the eligibility criteria defined for the program and the method.

## Auto-selection of method

**Note:** Auto-selection of the vaccination method only applies if the **sn\_vaccine\_sm.enable\_inventory\_management** system property value is **true**.

When you try to book an appointment, the system auto-assigns the method of vaccine based on the order of method selection and inventory availability. In other words, if the inventory management system property \(**sn\_vaccine\_sm.enable\_inventory\_management**\) is **true**, the vaccination request auto-assigns the method with the lowest order that has inventory availability.

For example, if a vaccination center has the Moderna vaccine in the inventory, the request is created using Moderna instead of Pfizer, even when Pfizer is the method with the lowest order.

## Manual selection of method

You can manually select the preferred vaccination method while booking an appointment. Manual selection of the method works with or without vaccine inventory management.

If the slot selection system property \(**sn\_vaccine\_sm.enable\_appointment\_slot\_choice**\) is **false**, the vaccine method selected is kept as the preference. If there’s no availability for the second dose, the system books the slot at the closest vaccination center having the same method. For example, if you select a vaccination site and the site has only one week of the Pfizer vaccine available, the second dose is selected in the nearest center having the same method.

**Note:** For the functionality to run properly, make sure that both the inventory management system property \(**sn\_vaccine\_sm.enable\_inventory\_management**\) and the enable multi-vaccine system property \(**sn\_vaccine\_sm.enable\_multi\_vaccine**\) values are **true**.

**Parent Topic:**[Configuring Vaccine Administration Management](vaccine-mgmt-config.md)

