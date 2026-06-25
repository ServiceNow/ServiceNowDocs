---
title: Review move conflicts
description: You can review the reason behind a move request conflict and decide how to resolve the conflict.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/review-conflicts.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage, Workplace Move Management, Workplace Service Delivery, Employee Service Management]
---

# Review move conflicts

You can review the reason behind a move request conflict and decide how to resolve the conflict.

If the state of a move request is set to Closed incomplete, it means that the move request couldn’t be completed due to various reasons. As a move manager, you can review if there are any conflicts with the move request in the Conflicts review related list.

The different types of conflicts are as follows:

-   **Selected destination location is not active**: Conflict due to inactive to location selected to move.
-   **Selected destination location is already occupied**: Conflict due to unavailability of the location selected to move.
-   **The cost centre/department of user and the selected destination location does not match**: Conflict due to mismatch in the user's cost centre/department and the location selected to move. The conflict is considered based on the Allocation type \[**sn\_wsd\_core.ALLOCATION\_TYPE**\] system property
-   **The selected destination location is a flexible location**: Conflict due to the location that is selected to move is a flexible location.
-   **Created a workplace move request for a space that is a workplace profile of another user**

You can also customize the list of validations that you want to run on a move request. You can add validations or change existing validations in the **WSDMoveRequestValidations** script include.

**Parent Topic:**[Managing Workplace Move Management requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/workplace-mov-mgmt-setup.md)

**Related topics**  


[Create a move request on behalf of an employee]()

[Raise a move request for a space change]()

[Update a move request workplace service]()

[Update a move-related workplace service record producer]()

[Create a move-related knowledge base article]()

