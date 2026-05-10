---
title: Configure the create action check box for safety inspection survey in the Mobile Agent app
description: Determine the survey field types that should display the Create action option when inspection agents complete the survey in the Mobile Agent app.
locale: en-US
release: australia
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage the safety inspection and audit surveys through mobile app, Manage safety inspections and audits through the mobile apps, Mobile experience for Health and Safety, Health and Safety, Employee Service Management]
---

# Configure the create action check box for safety inspection survey in the Mobile Agent app

Determine the survey field types that should display the **Create action** option when inspection agents complete the survey in the Mobile Agent app.

## Before you begin

Verify that the application scope is selected as Health and Safety Incident Management. For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_ApplicationPicker.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety administration** &gt; **Properties**.

2.  In the property **Survey fields enabled for action creation** add the values, such as, `checkbox,boolean,choice,long,percentage,scale,numericscale` to determine whether a specific survey field should display the **Create action** check box.

    `checkbox,boolean,choice,long,percentage,scale,numericscale,imagescale,string, multiplecheckboxranking,reference` is set as the default value for this property.

3.  Select **Save**.


## Result

The **Create action** check box is added to the type of the survey field mentioned in the property.

**Parent Topic:**[Manage the safety inspection and audit surveys through mobile app](../concept/hs-configure-manage-safety-inspections-audits-mobile.md)

