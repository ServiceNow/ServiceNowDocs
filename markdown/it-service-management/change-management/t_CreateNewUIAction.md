---
title: Create a UI action
description: Create a UI action to display a button on a change request for the Complete state.
locale: en-US
release: australia
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tutorial: add a new change management state, Reference, Change Management, IT Service Management]
---

# Create a UI action

Create a UI action to display a button on a change request for the **Complete** state.

## Before you begin

Role required: admin

## About this task

The UI action must contain a condition that uses the state model script include to decide when the **Complete** button is displayed on the Change Request form. In this case, the **Complete** button is displayed only when the change has reached the **Implement** state.

## Procedure

1.  Open the **Change Request** form.

2.  Open the form context menu and select **Configure** &gt; **UI Actions**.

3.  Locate and open the existing **Implement** UI action.

4.  Open the form context menu and click **Insert and Stay** to create a duplicate record.

5.  Modify the following fields with new values.

<table id="table_mpc_zd1_4v"><thead><tr><th>

Field

</th><th>

Values

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Complete.

</td></tr><tr><td>

Action name

</td><td>

state\_model\_move\_to\_complete.

</td></tr><tr><td>

Hint

</td><td>

Progresses change to Complete state.

</td></tr><tr><td>

Onclick

</td><td>

`moveToComplete();`.

</td></tr><tr><td>

Condition

</td><td>

gs.hasRole\('itil'\) &amp;&amp; new ChangeRequestStateHandler\(current\).isNext\("**complete**"\)

</td></tr><tr><td>

Script

</td><td>

Update function, state name, and state value.```
function moveToComplete(){
                  var ga = new GlideAjax("ChangeRequestStateHandlerAjax");         
                  ga.addParam("sysparm_name", "getStateValue");         
                  ga.addParam("sysparm_state_name", "complete"); 
                  ga.getXMLAnswer(function(stateValue) {              
                      g_form.setValue("state", stateValue);              
                      gsftSubmit(null, g_form.getFormElement(), "state_model_move_to_complete");         
                  });
          } 
          if (typeof window == 'undefined')   
             setRedirect(); 

          function setRedirect() {   
              current.update();   
              action.setRedirectURL(current);
          }
```

.

</td></tr></tbody>
</table>6.  Click **Update**.


**Parent Topic:**[Tutorial: add a new change management state](t_AddNewStateTutorial.md)

**Previous topic:**[Update the state model script include](t_UpdateStateModelScriptInclude.md)

**Next topic:**[Create a process flow record](t_CreateNewProcessFlowRecord.md)

