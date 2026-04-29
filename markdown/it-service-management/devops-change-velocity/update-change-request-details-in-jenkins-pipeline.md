---
title: Update change request details in Jenkins pipeline
description: Update the change request details associated with a Jenkins pipeline by running the snDevOpsUpdateChangeInfo script in the pipeline.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Additional information - Jenkins, Jenkins, Integrate, DevOps Change Velocity, IT Service Management]
---

# Update change request details in Jenkins pipeline

Update the change request details associated with a Jenkins pipeline by running the snDevOpsUpdateChangeInfo script in the pipeline.

## Before you begin

Role required: Jenkins admin

## About this task

When you update the **state** parameter in a change request, only the following transitions are supported:

-   cancel: Change request state must be **implement** to move the state to **cancel**. **reason** is a mandatory input to update the state to canceled.
-   closed: Change request state must be **implement** or **post implement** to move the state to **close**. **close\_code** and **close\_notes** are mandatory input to update the state to closed.

Specify the change request state as an integer value:

-   4 - Cancel \(Value set in the sn\_devops.change\_request.cancel\_state property\)
-   3 - Closed \(Value set in the sn\_devops.change\_request.closed\_state property\)

When you update a choice field, you must specify a valid choice value that is available in the corresponding choice list. For example, the choice list values for the **Close code** field are successful, successful\_issues, and unsuccessful. ![Choice values for the Close code field](../image/choice-field-update-change.png)

## Procedure

1.  In your Jenkins dashboard, open the pipeline for which you want to update the change request details.

2.  Navigate to **Configure &gt; Pipeline**. ![Pipeline script section in Jenkins](../image/jenkins-script-pipeline.png)

3.  In the Pipeline script section, update the `snDevOpsUpdateChangeInfo` script with the following input parameters:

    -   Change request number whose details need to be updated.
    -   Change request details to be updated as Key:Value pairs.
    ```
    { "short_description": "Test description", "priority": "1", "start_date": "2021-02-05 08:00:00", 
    "end_date": "2022-04-05 08:00:00", "justification": "test justification", "description": "test description", 
    "cab_required": <true/false>, "comments": "This update for work notes is from jenkins file", "work_notes": "test work notes", 
    "assignment_group": "<SYS_ID>", "state":"<STATE_CODE>", "close_code":"<successful/successful_issues/unsuccessful>", "reason":"<As per Choice List>" 
    ```

4.  Save the script.

5.  Navigate to **DevOps &gt; Orchestrate &gt; Pipeline Change Requests**.

6.  Select the change record associated with the pipeline.

7.  Approve the change request by selecting  **Approved**  in the  **State**  field.

8.  In Jenkins, open the pipeline for which you are updating the change request details.

9.  Select **Build Now**.

    The change request details specified in step 3 will be updated for the pipeline.


