---
title: Assign multiple teams to support a service offering
description: You can assign multiple teams to support a single service offering when several teams are responsible for that offering.
locale: en-US
release: yokohama
product: Service Portfolio Management
classification: service-portfolio-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Service offerings in Service Portfolio Management, Using Service Portfolio Management, Service Portfolio Management, IT Service Management]
---

# Assign multiple teams to support a service offering

You can assign multiple teams to support a single service offering when several teams are responsible for that offering.

## Before you begin

Role required: service\_editor

## About this task

The service offering team table \[cmdb\_rel\_team\] enables multiple groups to be related to a single service offering. While in the offering record, use the **Team** tab to assign a support group to the offering. Use the Related Links **Teams** tab to add more support groups to the service offering. You can also edit the group type of the teams that you add in the Related Links **Teams** tab.

## Procedure

1.  Navigate to **All** &gt; **Service Portfolio Management** &gt; **Service Offerings**.

2.  Open the service offering that you want to assign support teams.

    ![Offering record example.](../image/spm2-teams-offering.png "Offering record example")

3.  In the first **Team** tab on the offering record, use the Search icon \(![Search icon](../../site-reliability-ops/image/icon-search.png)\) to select the support group for this service offering, and then **Save** the page.

    After you save the page, the support group that you selected displays in the second **Teams** tab, in the Related Links area. The Related Links **Teams** tab has three columns: **User group** \(the support group name that you selected in the first teams tab\), **Group type**, and **Primary**. You can set the primary entry to true or false, indicating that the user group is the primary support group.

4.  **Save** the offering record.

5.  The Related Links **Teams** tab contains all the teams that you added.

    You can select any team in the **User group** column to change the team. You can also select any **Group type** to change it to one of the other options: Support Group, Approver Group, Change Group, or Managed By Group.


**Parent Topic:**[Service offerings in Service Portfolio Management](../concept/SPM2-service-offerings.md)

