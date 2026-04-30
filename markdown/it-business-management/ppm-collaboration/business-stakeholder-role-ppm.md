---
title: Business stakeholder role for PPM
description: For PPM users, the Business Stakeholder \(com.snc.business\_stakeholder\) plugin contains the business stakeholder roles for Enterprise Architecture \(formerly APM\), ITFM, and PPM. Users with this role can read records of the tables that are used to retrieve data for reports and dashboards and can approve demands and timecards. You can assign this role to any user who is a business stakeholder.
locale: en-US
release: yokohama
product: PPM Collaboration
classification: ppm-collaboration
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Reference, Project Portfolio Management, Strategic Portfolio Management]
---

# Business stakeholder role for PPM

For PPM users, the Business Stakeholder \(com.snc.business\_stakeholder\) plugin contains the business stakeholder roles for Enterprise Architecture \(formerly APM\), ITFM, and PPM. Users with this role can read records of the tables that are used to retrieve data for reports and dashboards and can approve demands and timecards. You can assign this role to any user who is a business stakeholder.

## Upgrade information

If you have upgraded, the business stakeholder role for PPM is available only when you activate Read only roles for PPM Standard plugin \(com.snc.pmo\_read\_roles\).

If you are a new customer, the Read only roles for PPM Standard plugin \(com.snc.pmo\_read\_roles\) is activated on zBoot. However, the business stakeholder role for PPM is available only when you install the PPM Standard plugin.

## Demand and Timecard approver roles

The Read only roles for PPM Standard plugin \(com.snc.pmo\_read\_roles\) installs the sn\_ppm\_read role. The sn\_ppm\_read role provides read-only access to the Portfolio, Program, and Timecard dashboards along with the Resources report to the assigned users. The sn\_ppm\_read role also contains the timecard\_approver and demand\_approver roles, which allow the assigned users to approve demands and timecards. Commenting is enabled, when a business stakeholder role is added as collaborator in demands.

## PPM tables accessible to users with the business stakeholder role

Users with the business stakeholder role for PPM can access the following tables that store the data to load the widgets in the Portfolio dashboard, Program dashboard, and Time Sheet dashboard, and Resource reports:

|Label|Table name|
|-----|----------|
|Action|project\_action|
|Decision|dmn\_decision|
|Demand|dmn\_demand|
|Demand Task|dmn\_demand\_task|
|Fiscal period|fiscal\_period|
|Idea|im\_idea\_core|
|Issue|issue|
|Program|pm\_program|
|Project|pm\_project|
|Project Task|pm\_project\_task|
|Program Task|pm\_program\_task|
|Project Time Card Exception|project\_timecard\_exception|
|Requirement|dmn\_requirement|
|Resource Aggregate Daily|resource\_aggregate\_daily|
|Resource Aggregate Monthly|resource\_aggregate\_monthly|
|Resource Aggregate Weekly|resource\_aggregate\_weekly|
|Resource Plan|resource\_plan|
|Risk|risk|
|Status Report|project\_status|
|Time Card|time\_card|
|Time Sheet|time\_sheet|
|Time Sheet Exception|time\_sheet\_exception|

**Parent Topic:**[Project Portfolio Management reference](project-portfolio-management-reference.md)

