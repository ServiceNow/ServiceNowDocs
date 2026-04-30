---
title: View scores of a custom scoring profile on bubble chart
description: Create a system property to view indicator scores of a custom scoring profile on the application rationalization bubble chart.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-05-22"
reading_time_minutes: 1
breadcrumb: [Use bubble chart view, Working with application rationalization, Manage, Enterprise Architecture Workspace, Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# View scores of a custom scoring profile on bubble chart

Create a system property to view indicator scores of a custom scoring profile on the application rationalization bubble chart.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** and in the filter enter `sys_properties.list`.

2.  Verify that the property does not exist by searching for the property name in the System Properties table.

3.  Click **New**.

4.  On the form, fill in the following details.

    -   Name- Name of the property you’re creating. In this case, `sn_apm_ws.app_indicator_scoring_profile`.
    -   Description- Type a brief, descriptive phrase describing the function of the property.
    -   Type- String.
    -   Value- Enter the value as `new_scoring_profile_sys_id`.
5.  Select **Submit**.


## Result

The Application Rationalization bubble chart view displays the bubbles representing the scores generated for the new scoring profile.

**Parent Topic:**[Use bubble chart view](../../concept/eaw-concept/eaw-using-app-rat-bubble-chart-view.md)

