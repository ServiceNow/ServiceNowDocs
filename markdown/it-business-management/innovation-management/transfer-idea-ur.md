---
title: Transfer an Idea to another department
description: Transfer an idea to another department with or without resolution if the idea is rejected or cannot be implemented.
locale: en-US
release: xanadu
product: Innovation Management
classification: innovation-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Integrate, Innovation Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Transfer an Idea to another department

Transfer an idea to another department with or without resolution if the idea is rejected or cannot be implemented.

## Before you begin

Ensure that the following requirements are met:

-   The idea is created from a universal request.
-   The idea is associated with a category.
-   Personalize the Create an Idea form to add the **Assigned to** field.
-   The idea is assigned to an agent.
-   Additional plugins required for transfer are active. For example, if the idea is being transferred as an HR case \(HRC\), activate the Human Resources Scoped App: Core \(com.sn\_hr\_core\), and Employee Center \(com.snc.employee\_center\) plugins.

Role required: Agent to whom the idea is assigned or is a part of the assigned work group.

## About this task

If the idea is rejected or cannot be implemented, transfer the idea to another department as an HRC, incident, or a custom task.

When an idea is transferred to another department, the idea is closed and a new record is created. For example, a universal request related to HR process improvement can be converted to an idea and then transferred to the HR department as an HRC when the idea is deemed not feasible.

## Procedure

1.  Navigate to **All** &gt; **Ideas** &gt; **Idea Portal**.

2.  Select the title of an idea to view its details.

3.  Select the more options icon \(![More options icon](../image/more-options-icon.png)\), and then click the **Open in platform** option to open the idea in the form view.

4.  Select **Transfer**.

5.  In the **Transfer Ticket** dialog box, provide the following details.

    -   **Department**: Select the department from the list.
    -   **Transfer reason**: Select the reason from the list.
    -   **Transfer notes**: A brief description for transferring the idea that you want to pass to the UR Routing agent.
    -   **Copy additional comments and attachments**: Clear the check box if you do not want to transfer the idea with additional comments and attachments.
6.  Select **Transfer**.

    The idea is transferred to the selected department and the state of the idea is changed to **Unlikely to implement**.

7.  Provide information about why the idea was rejected or closed in the **Close notes** field.

8.  Select **Update**.


## Result

The idea is transferred to the selected department. The **Primary Ticket** field of the parent universal request is updated with the INC, HRC, or custom task number created as a result of the transfer.

**Parent Topic:**[Integrating Innovation Management with Universal Request](../concept/universal-req-idea-mgmt.md)

