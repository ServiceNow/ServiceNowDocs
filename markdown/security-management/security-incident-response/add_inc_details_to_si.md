---
title: Add information to a security incident
description: After a security incident is created, you can add more details to aid in analysis, such as access roles and different kinds of notes.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add information to a security incident

After a security incident is created, you can add more details to aid in analysis, such as access roles and different kinds of notes.

## Before you begin

Role required: sn\_si.basic

## Procedure

1.  If it is not already open, open the security incident you want to update.

2.  Click the **Incident Details** tab.

3.  Fill in the fields, as needed.

<table id="table_l2p_dcs_ns"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Read access

</td><td>

Gives a user with the **special access** role read access to the security incident. The user is able to read and write work notes. **Note:**

-   If a user is added to both **Read access** and **Privileged access** lists, then only the **Privileged access** permissions persist.
-   User with sn\_si.admin role only can modify both read access and privileged access.


</td></tr><tr><td>

Watch list

</td><td>

Click the lock icon to add users who are notified when changes to the security incident occur. After the field is unlocked, options are available for adding or removing multiple users or entering user email addresses. When you have completed your entries, click the lock icon to lock the field.

</td></tr><tr><td>

Privileged access

</td><td>

Gives a user with the **special access** role read and write access to all fields of the security incident except **Assigned to**. Users with special access roles have their own module containing all security incidents assigned to them. No other modules are available to them. No one else can see the **Visible to Me** module.**Note:**

Only an assigned user or someone with a security role \(for example, sn\_si\_analyst or sn\_si.admin\) can change the **Assigned to** field.

If a user is added to both **Read access** and **Privileged access** lists, then only the **Privileged access** permissions persist.

</td></tr><tr><td>

Work notes list

</td><td>

Click the lock icon \(![Lock](../../security-operations-common/common/images/lock.png)\) to add users who are notified when new work notes are added. After the field is unlocked, options are available for adding or removing multiple users or entering user email addresses. When you have completed your entries, click the lock icon to lock the field.

</td></tr><tr><td>

Description

</td><td>

Enter a full description of the security incident, along with any information that can help to find the cause or resolve the issue.

</td></tr><tr><td>

Secure notes

</td><td>

Only user roles with sn\_si.admin and sn\_si.analyst can view or edit the secure notes.

</td></tr><tr><td>

Work notes

</td><td>

Type work notes that are not visible to the customer. Work notes appear in the **Activity** area.

</td></tr><tr><td>

Activity

</td><td>

Displays information manually entered in Work notes, and all dynamically updated task activity \(actions, comments, work notes, and so on\) on related records for this security incident. Work notes appear with a yellow color band.

![Manually-entered work note](../image/manual-work-note.png)

 Automatically generated notes appear with a gray color band.

![Automatically-generated work note](../image/auto-work-note.png)

</td></tr></tbody>
</table>4.  You can limit the types of information displayed in the **Activity** field by clicking the filter \(![Filter](../image/filter-icon.png)\) icon.

    ![Filter activities](../image/filter.png)

    **Note:** The **Automation activity** check box allows you to include any enrichment performed by this security incident, including workflow activities, risk score updates, and so forth.

5.  Click any of the following tabs to further update the security incident:

    -   [Related Records](add-rel-recs-to-si.md)
    -   [Post Incident Review](../concept/c_PostIncidentReview.md)
    -   [Closure Information](add-closure-info-to-si.md)
6.  When you have completed your entries, click **Submit**.


