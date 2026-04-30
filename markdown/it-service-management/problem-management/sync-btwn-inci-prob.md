---
title: Synchronization between incident and problem records
description: Change in a Problem record impacts related Incident records. Notification is sent to the user for each such update.
locale: en-US
release: xanadu
product: Problem Management
classification: problem-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Reference section for Problem Management, Problem Management, IT Service Management]
---

# Synchronization between incident and problem records

Change in a Problem record impacts related Incident records. Notification is sent to the user for each such update.

When you activate the Problem Management Best Practice — Madrid \(com.snc.best\_practice.problem.madrid\) and the Problem Management Best Practice — Madrid — State Model \(com.snc.best\_practice.problem.madrid.state\_model\) plugin, the changes in a Problem record impact incidents that are associated to that Problem.

<table id="table_ady_kd5_5fb"><thead><tr><th>

Plugin

</th><th>

Incident state

</th><th>

Problem state

</th><th>

Action on Problem

</th><th>

Action on Incident

</th></tr></thead><tbody><tr><td>

Problem Management Best Practice — Madrid plugin ```
com.snc.best_practice.problem.madrid
```

</td><td>

Any incident state other than resolved, closed, or canceled.

</td><td>

Any

</td><td>

Click the **Communicate workaround** related link

</td><td>

-   The workaround is copied to the **Work notes** field. A notification is sent to the users listed in the **Assigned to** and **Work notes list** fields. The notification is sent only when the incident state is New, On Hold, or In Progress.
-   The workaround is copied to the **Additional Comments** field. If **Known error** is selected from the **Resolution code** field of the incident, then a notification is sent to the caller and to the users listed in the **Assigned to** and **Watch list** fields.

</td></tr><tr><td>

Problem Management Best Practice — Madrid plugin ```
com.snc.best_practice.problem.madrid
```

</td><td>

Any incident state other than resolved, closed, or canceled.

</td><td>

Any

</td><td>

Click the **Communicate Fix** related link

</td><td>

-   The fix is copied to the **Work Notes** field of the incident record.
-   A notification is sent to the users listed in the **Assigned to** and **Work notes** list fields of the incident record.

</td></tr><tr><td>

Problem Management Best Practice — Madrid — State Model plugin ```
com.snc.best_practice.problem.madrid.state_model
```

</td><td>

**On Hold** and **On hold reason** is **Awaiting Problem**

</td><td>

Problem state is **Closed** or **Resolved** and the problem **Resolution code** is **Fix Applied**

</td><td>

NA

</td><td>

-   The **Resolution notes** on the incident form displays the message `Related problem INCxxxx closed. Please see additional comments for fix notes` , where INCxxxx is the incident number from which the problem was created.
-   The incident state is changed to **Resolved**.
-   The **Resolution code** is changed to **Resolved by problem**.
-   An email notification is sent to the caller and the user who is assigned to the Incident.

</td></tr><tr><td>

Problem Management Best Practice — Madrid — State Model plugin ```
com.snc.best_practice.problem.madrid.state_model
```

</td><td>

**On Hold** and **On hold reason** is **Awaiting Problem**

</td><td>

Problem state is **Closed** or **Resolved** and the problem **Resolution code** is **Risk Accepted**

</td><td>

NA

</td><td>

-   The information from the **Risk accepted reason** field on the Problem form is copied to the **Work notes** field on the Incident form.
-   An email notification is sent to the user who is assigned to the Incident.

</td></tr></tbody>
</table>**Parent Topic:**[Reference section for Problem Management](reference-section-for-problem-management.md)

