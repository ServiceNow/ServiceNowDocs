---
title: Set up a worker profile
description: Establish a connection between a functional location and a user by setting up a worker profile in Industrial Connected Workforce.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/industrial-connected-workforce/digital-factory-workspace/set-up-worker-profile.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Prerequisites, Configure, Digital Factory Workspace, Industrial Connected Workforce]
---

# Set up a worker profile

Establish a connection between a functional location and a user by setting up a worker profile in Industrial Connected Workforce.

## Before you begin

Your functional location must be created and available in the list of equipment model entities.

Role required: sn\_icw.admin

**Note:** Users without the admin role can only edit their own worker profiles.

## About this task

The sn\_icw\_worker\_profile table contains the link between a user and a functional location. Setting up this link is a prerequisite to use the system.

## Procedure

1.  In the **All** tab search bar, enter `sn_icw_worker_profile.list`.

2.  Select **New**.

3.  In the **Functional location** field, enter the location that you need.

4.  In the **User** field, enter the user that you want to link to the location.

5.  Select **Submit**.

    \[Omitted image "worker-profile.png"\] Alt text: New record page for worker profile


**Parent Topic:**[Setting up prerequisites for Digital Factory Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/setting-up-prerequisites-digital-factory-workspace.md)

