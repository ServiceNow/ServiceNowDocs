---
title: Configure the create action check box for safety inspection survey in the Mobile Agent app
description: Determine the survey field types that should display the Create action option when inspection agents complete the survey in the Mobile Agent app.
locale: en-US
release: xanadu
product: Health and Safety
classification: health-and-safety
topic_type: task
last_updated: "2025-04-29"
reading_time_minutes: 1
breadcrumb: [Mobile experience for Health and Safety, Health and Safety, Employee Service Management]
---

# Configure the create action check box for safety inspection survey in the Mobile Agent app

Determine the survey field types that should display the **Create action** option when inspection agents complete the survey in the Mobile Agent app.

## Before you begin

Verify that the application scope is selected as Health and Safety Incident Management. For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Health and Safety** &gt; **Health and Safety administration** &gt; **Properties**.

2.  In the property **Survey fields enabled for action creation** add the values, such as, `checkbox,boolean,choice,long,percentage,scale,numericscale` to determine whether a specific survey field should display the **Create action** check box.

    `checkbox,boolean,choice,long,percentage,scale,numericscale,imagescale,string, multiplecheckboxranking,reference` is set as the default value for this property.

3.  Select **Save**.


## Result

The **Create action** check box is added to the type of the survey field mentioned in the property.

**Parent Topic:**[Mobile experience for Health and Safety](../concept/hs-health-safety-mobile.md)

