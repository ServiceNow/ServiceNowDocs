---
title: Step 6. Create business rules for a Security Case
description: Create required business rules for a Security Case.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Rollup example use case implementation for a Security Case, Rollup Framework for MSIM, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Step 6. Create business rules for a Security Case

Create required business rules for a Security Case.

## Before you begin

Role required: admin

Create the three following business rules for the new source table Security Case \(sn\_ti\_case\). These business rules are required to maintain the consistency in behavior with base system provided source table such as Security incident \(sn\_si\_incident\).

Business rules for the new source table:

1.  **Deactivate link when inactive**: Once the security case is closed, related information will no longer be shown in Major Security Incident Management workspace page.
2.  **Sync up team info on update**: Major Security Incident details tab shows the information about the all the active teams and users working on different tasks. Once we update assigned to user or assignment group is changed in the security case, we need to update security case team information in the Major Security Incident active team section. These business rules will update new assigned to user and assignment group in the active team section.
3.  **Sync up team info on delete**: Major Security Incident details tab shows the information about the all the active teams and users working on different tasks. Once we close the security case, we no longer need to show security case team information in the Major Security Incident active team section. These business rules will remove the assigned to user and assignment group from the active team.

**Create business rules for new source table:**

## Procedure

1.  Navigate to **System definition** &gt; **Business Rules**.

2.  Run the filter option to filter business rules criteria with below information:

    -   **Name**: Deactivate link when inactive
    -   **Table**: sn\_si\_incident
    ![Business rules](../image/business-rules-step6.png)

3.  Open record and change the table name to a new source table: sn\_ti\_case.

4.  Select and hold \(or right-click\) the menu on the page and select **Insert and Stay** to create the record.

    ![Change the table name](../image/change-table-name-step6.png)

5.  Repeat the procedure for another two business rules as well.

    -   Sync up team info on delete
    -   Sync up team info on update

**Parent Topic:**[Rollup example use case implementation for a Security Case](../concept/use-case-for-a-security-case.md)

