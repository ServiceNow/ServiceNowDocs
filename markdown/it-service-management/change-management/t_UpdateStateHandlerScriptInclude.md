---
title: Update the state handler script include
description: Update the ChangeRequestStateHandler script include with the new Complete state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/t\_UpdateStateHandlerScriptInclude.html
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tutorial: add a new change management state, Reference, Change Management, IT Service Management]
---

# Update the state handler script include

Update the ChangeRequestStateHandler script include with the new **Complete** state.

## Before you begin

Role required: admin

## About this task

The ChangeRequestStateHandler script include defines the states available for the Change Request state model.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Open the ChangeRequestStateHandler script include and modify the script as follows.

    1.  Add the following line to the top of the script in the **Constants** section:

        ```
        ChangeRequestStateHandler.COMPLETE = "complete";
        ```

    2.  Add the following line as the last line of the function in the *Initialize* function:

        ```
        this.STATE_NAMES["-6"] = ChangeRequestStateHandler.COMPLETE;
        ```

    \[Omitted image "NewStateTutUpdScrptIncl1.png"\] Alt text: Modified script

3.  Click **Update**.


**Parent Topic:**[Tutorial: add a new change management state](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_AddNewStateTutorial.md)

**Previous topic:**[Create an ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_CreateNewACL.md)

**Next topic:**[Update the state model script include](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/change-management/t_UpdateStateModelScriptInclude.md)

