---
title: Limit the number of task sys\_ids returned for reverse matching rules
description: Reverse matching rules return a list of case sys\_ids. Limit the number of cases returned by configuring the number in the reverse.matchingrule.entity.limit system property.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Reverse matching, Routing and assigning customer service cases, Administer Customer Service Management, Customer Service Management]
---

# Limit the number of task sys\_ids returned for reverse matching rules

Reverse matching rules return a list of case sys\_ids. Limit the number of cases returned by configuring the number in the reverse.matchingrule.entity.limit system property.

## Before you begin

Role required: admin

## Procedure

1.  In the navigation filter, type `sys_properties.list`.

2.  Search for the reverse.matchingrule.entity.limit system property.

3.  In the number field, change the number of cases returned.

    The default number is 30.


## Result

If the number of cases returned is more than the value listed in the system property, the reverse matching rule does not run for Scripted and Selection Criteria matching rules.

**Parent Topic:**[Reverse matching](t_ReverseMatching.md)

