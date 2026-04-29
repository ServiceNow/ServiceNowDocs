---
title: Update change request states
description: If you upgraded from a release prior to Geneva, you must update old state labels to new state labels after you activate the Change Management state model.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Activate Change Management - State Model, Change Management plugins, Configure, Change Management, IT Service Management]
---

# Update change request states

If you upgraded from a release prior to Geneva, you must update old state labels to new state labels after you activate the Change Management state model.

## Before you begin

Role required: admin

## About this task

State values for current change records are not modified when you activate the Change Management state model. However, your current change records display the new state labels in the state field.

|State value|New state label|Old state label|
|-----------|---------------|---------------|
|-5|New|Pending|
|-4|Assess|\(Not used\)|
|-3|Authorize|\(Not used\)|
|-2|Scheduled|\(Not used\)|
|-1|Implement|\(Not used\)|
|0|Review|\(Not used\)|
|1|\(Not used\)|Open|
|2|\(Not used\)|Work in Progress|
|3|Closed|Closed Complete|
|4|Canceled|Closed Incomplete|
|7|\(Not used\)|Closed Skipped|

For example, records with a state value of -5 have the **Pending** state label before the Change Management state model is activated. After the state model is activated, these records retain the state value of -5 but have the **New** label. To use your organization's required change management process with the state model, you must update state values to the new labels in your existing change records as appropriate, either manually or by script.

You must also update any reports that run queries based on old state labels to reflect the new state labels.

## Procedure

1.  To automatically update the state field values from old state labels to new state labels, customize and then run the following sample script:

    ```
    updateStates();
    
    function updateStates() {
    
      function hasApprovers(changeGr) {
        var approverGr = new GlideRecord("sysapproval_approver");
        approverGr.addQuery('sysapproval', changeGr.getUniqueValue());
        approverGr.query();
        return approverGr.getRowCount() > 0;
      }
    
      function hasRunningWorkflows(changeGr) {
        var workflow = new Workflow();
        var workflowGr = workflow.getRunningFlows(changeGr);
        var hasRunningFlows = workflowGr.getRowCount() > 0;
        return hasRunningFlows;
      }
    
      // Old State Model
      var PENDING = '-5';
      var OPEN = '1';
      var CLOSED_COMPLETE = '3';
      var CLOSED_INCOMPLETE = '4';
      var CLOSED_SKIPPED = '7';
    
      // New State Model
      var NEW = '-5';
      var ASSESS = '-4';
      var AUTHORIZE = '-3';
      var SCHEDULED = '-2';
      var IMPLEMENT = '-1';
      var REVIEW = '0';
      var CLOSED = '3';
      var CANCELLED = '4';
    
      // Find all change requests
      var record = new GlideRecord('change_request');
      record.query();
    
      // Update state from old value to new value
      while (record.next()) {
        switch(record.getValue('state')) {
          case OPEN:
            if (!hasRunningWorkflows(record) && !hasApprovers(record))
              record.state = NEW;
            break;
          case CLOSED_COMPLETE:
            record.state = CLOSED;
            record.close_code = "successful";
            break;
          case CLOSED_SKIPPED:
            record.state = CANCELLED;
            record.close_code = "unsuccessful";
            break;
          case CLOSED_INCOMPLETE:
            record.state = CLOSED;
            record.close_code = "successful_issues";
            break;
        }
        record.autoSysFields(false);
        record.setWorkflow(false);
        record.update();
      }
    
    }
    
    ```

2.  Verify that the state labels have changed in existing change request records.


**Parent Topic:**[Activate Change Management - State Model](t_ActivateStateModel.md)

**Related topics**  


[Installed with Change Management - State Model](../reference/r_InstalledWithStateModel.md#)

