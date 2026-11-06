---
title: Utility workflow activities
description: Utility activities provide controls over the path of the workflow, and other useful tools.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
---

# Utility workflow activities

Utility activities provide controls over the path of the workflow, and other useful tools.

-   **[Branch workflow activity]()**  
The **Branch** activity splits the workflow into multiple transition paths from a single activity.
-   **[Join workflow activity]()**  
The **Join** activity unites multiple execution paths into one transition.
-   **[Lock workflow activity]()**  
The **Lock** activity prevents other instances of this workflow from continuing past this activity until the lock is released.
-   **[Log Message workflow activity]()**  
The **Log Message** activity writes a message to the workflow log.
-   **[Log Trace Message workflow activity]()**  
The **Log Trace Message** activity writes a trace message to the workflow log.
-   **[REST Message legacy workflow activity]()**  
The legacy **REST Message** activity enables an administrator to override the REST endpoint or supply the variables configured in the REST Message module.
-   **[Return Value workflow activity]()**  
The **Return Value** activity returns a value to a parent workflow, when run from a subflow.
-   **[Run Script workflow activity]()**  
The **Run Script** activity runs the specified script in the scope of the workflow version.
-   **[Set Values workflow activity]()**  
The **Set Values** activity sets values on the current record when the workflow quiesces or ends.
-   **[SOAP Message legacy workflow activity]()**  
The legacy **SOAP Message** activity uses SOAP messages defined in the System Web Services plugin and can call the messages using a MID Server.
-   **[Turnstile workflow activity]()**  
The **Turnstile** activity limits how many times a workflow can pass through the same point.
-   **[Unlock workflow activity]()**  
The **Unlock** activity releases a lock that was previously placed by the **Lock** activity.

**Parent Topic:**[Workflow activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/workflow-activities/c_WorkflowActivities.md)

