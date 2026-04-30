---
title: Review move conflicts
description: View the reason behind a move request conflict.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Manage, Workplace Move Management, Workplace Service Delivery, Employee Service Management]
---

# Review move conflicts

View the reason behind a move request conflict.

If the state of a move request is set to Closed incomplete, it means that the move request could not be completed due to various reasons. As a move manager, you can review if there are any conflicts with the move request in the Conflicts review related list.

Following are the different types of conflicts:

-   **Selected destination location is not active**: Conflict due to inactive to location selected to move.
-   **Selected destination location is already occupied**: Conflict due to unavailability of the location selected to move.
-   **The cost centre/department of user and the selected destination location does not match**: Conflict due to mismatch in the user's cost centre/department and the location selected to move. The conflict is considered based on the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] system property
-   **The selected destination location is a flexible location**: Conflict due to the location that is selected to move is a flexible location.
-   **Created a workplace move request for a space that is a workplace profile of another user**

You can also customize the list of validations that you want run on a move request. You can add validations or change existing validations in the **WSDMoveRequestValidations** script include.

**Parent Topic:**[Managing Workplace Move Management requests](../concept/workplace-mov-mgmt-setup.md)

**Related topics**  


[Create a move request on behalf of an employee](../task/request-desk-change-for-employee-1.md)

[Raise a move request for a space change](../task/request-desk-change.md)

[Update a move request workplace service](../task/update-move-request-workplace-service.md)

[Update a move-related workplace service record producer](../task/view-move-request-record-producer.md)

[Create a move-related knowledge base article](../task/create-move-related-kb-article.md)

