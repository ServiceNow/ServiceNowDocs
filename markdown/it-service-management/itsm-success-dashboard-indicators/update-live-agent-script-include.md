---
title: Update the live agent script include
description: Live agent configuration is used in the self-solved deflections \(Deflection using KB articles, Deflection using QnA AIS, Deflection using QnA LLM, and Deflection using ITSM VA\). While we configure these deflections, we need to update the live agent script include. Update the SSADeflectionHelper script to override the checkInteraction function.
locale: en-US
release: zurich
product: ITSM Success Dashboard Indicators
classification: itsm-success-dashboard-indicators
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ITSM Success Dashboard Admin console, Configure, ITSM Success Dashboard indicators, IT Service Management]
---

# Update the live agent script include

Live agent configuration is used in the self-solved deflections \(Deflection using KB articles, Deflection using QnA AIS, Deflection using QnA LLM, and Deflection using ITSM VA\). While we configure these deflections, we need to update the live agent script include. Update the SSADeflectionHelper script to override the *checkInteraction* function.

## Before you begin

Role required: admin

## About this task

An agent interaction is where the interaction is not through a virtual agent interaction. The interaction could be through Walk up experience, phone, video or with a live agent. The base system instrumentation checks whether the employee created an incident or interacted with an agent after reading an article or interacting with a Virtual Agent.

The SSADeflectionHelper script overrides the check interaction function and helps in setting up the live agent interaction.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

2.  Open the SSADeflectionHelper script include and modify the script as follows.

    1.  Override the function *checkInteraction* from SSADeflectionHelperSNC

        ```
        checkInteraction: function(openedFor, windowStart, windowEnd) {
                var interactionRecord = new GlideRecord('interaction');
                // Pulling Virtual Agent User sysId from com.glide.cs.va.sys_user property
                var vaUser = gs.getProperty('com.glide.cs.va.sys_user');
                var windowConditions = 'opened_for=' + openedFor + '^sys_created_on>=' + windowStart + '^sys_created_on<=' + windowEnd;
                var interactionConditions = 'virtual_agent!=true^ORstateINon_hold,closed_abandoned^ORsys_created_by=system^ORopened_for.web_service_access_only!=false^opened_for.web_service_access_onlyISNOTEMPTY^ORopened_for.internal_integration_user!=false^opened_for.internal_integration_userISNOTEMPTY^assigned_to!=' + vaUser + '^ORassigned_to=NULL';
                var encodedQuery = windowConditions + '^' + interactionConditions;
                interactionRecord.addEncodedQuery(encodedQuery);
                interactionRecord.setLimit(1);
                interactionRecord.query();
                if (interactionRecord.next()) {
                    return true;
                }
                return false;
            },
        ```

    2.  Update the following line to update the live agent interaction conditions:

        ```
        var interactionConditions = 'virtual_agent!=true^ORstateINon_hold,closed_abandoned^ORsys_created_by=system^ORopened_for.web_service_access_only!=false^opened_for.web_service_access_onlyISNOTEMPTY^ORopened_for.internal_integration_user!=false^opened_for.internal_integration_userISNOTEMPTY^assigned_to!=' + vaUser + '^ORassigned_to=NULL';
        ```

    ![Live agent script include](../image/liveagent-script-include.png)


**Parent Topic:**[ITSM Success Dashboard Admin console](../concept/admin-console-sd.md)

