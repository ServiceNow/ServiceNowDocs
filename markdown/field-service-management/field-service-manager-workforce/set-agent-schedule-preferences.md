---
title: Allow agents to start traveling before their scheduled work hours
description: Support flexible work types by allowing agents to start traveling before their scheduled work hours. For example, you may want to add travel time outside of an agent's scheduled work hours in case bad weather suddenly increases travel time.
locale: en-US
release: yokohama
product: Field Service Manager Workforce
classification: field-service-manager-workforce
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Managing agent skills, schedules and tasks in Field Service Agent Management, Manage workforce, Using Field Service Management, Field Service Management]
---

# Allow agents to start traveling before their scheduled work hours

Support flexible work types by allowing agents to start traveling before their scheduled work hours. For example, you may want to add travel time outside of an agent's scheduled work hours in case bad weather suddenly increases travel time.

## Before you begin

If you are an administrator, you can run a script and add travel time outside of work hours for all users.

Role required: wm\_dispatcher, wm\_manager, wm\_admin, or admin

## Procedure

1.  Navigate to **All** &gt; **Field Service**.

2.  Do one of the following actions:

    -   If you are a dispatcher, go to **Dispatching** &gt; **My Agents**.
    -   If you are a manager, go to **Manager** &gt; **My Team**.
3.  Select a user profile.

4.  To add or update user records, do one of the following.

<table id="choicetable_pnx_tzm_vgb"><thead><tr><th align="left" id="d79409e117">

Option

</th><th align="left" id="d79409e120">

Description

</th></tr></thead><tbody><tr><td id="d79409e126">

**Add a new record for this user**

</td><td>

1.  Click the **Work Parameters** tab.
2.  Click **New**.
3.  Click the **Travel outside of work hours** drop-down menu.
4.  Click **Yes**
5.  Click **Submit**.


</td></tr><tr><td id="d79409e167">

**Updated an existing record**

</td><td>

1.  Click the **Work Parameters** tab.
2.  Double-click the **Travel outside of work hours** column.
3.  Click the new parameter.
4.  Click **Save \(Enter\)**.


</td></tr></tbody>
</table>5.  To add travel time as work hours for all users, do the following:

    1.  Navigate to **System Definition** &gt; **Scripts - Background**

    2.  In the **Run Script** window, add the script to include travel time as work hours for all users.

<table id="table_jsx_f4c_nsb"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Add travel time as work hours for all users

</td><td>

1.  Add this script:

    ```
createWorkParamsForAllAgents("yes");

function createWorkParamsForAllAgents(travelOutsideWorkHours) {
	var now_GR = new GlideRecord("sys_user_has_role");
	gr.addEncodedQuery("role=26c324ba1b32200096f9fbcd2c0713c2"); // fetching users having wm_agent role
	gr.query();
	gs.info("total work agents found: "+gr.getRowCount());
	var agentWorkParameter = {};
		
		while (gr.next()) {
			var userId = gr.getValue("user");
			if (!agentWorkParameter[userId]) {
				var wp = new GlideRecord("wm_agent_work_configuration");
				wp.initialize();
				wp.setValue("user",userId);
				wp.setValue("travel_outside_of_work_hours", travelOutsideWorkHours); // setting default value for travel_outside_of_work_hours
				wp.insert();
				agentWorkParameter[userId] = true;
			}
		}
	}
    ```

2.  Click **Run Script**.


</td></tr><tr><td>

Update travel time as work hours for all users

</td><td>

1.  Add this script:

    ```
updateWorkParamsForAgents("yes");  // param1: default travel outside work hours value

function updateWorkParamsForAgents(travelOutsideWorkHours) {
	var now_GR = new GlideRecord("wm_agent_work_configuration");
	gr.query();
	gs.info("total agent work parameters found: "+gr.getRowCount());
	var updateCount = 0;
	
	while (gr.next()) {
		var canTravelOutside = gr.getValue("travel_outside_of_work_hours");
		if ( canTravelOutside != travelOutsideWorkHours) {
			gr.setValue("travel_outside_of_work_hours", travelOutsideWorkHours);
			if (gr.update())
				updateCount ++;
		}
	}
	gs.info("total agent work parameters updated: "+updateCount);
}
    ```

2.  Click **Run Script**.


</td></tr></tbody>
</table>
**Parent Topic:**[Managing agent skills, schedules and tasks in Field Service Agent Management](../concept/field-service-agent-management.md)

