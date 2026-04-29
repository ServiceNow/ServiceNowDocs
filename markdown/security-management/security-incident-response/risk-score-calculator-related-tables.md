---
title: Risk Score Calculator for Additional Related Tables
description: The Risk Score Calculator is provisioned with one risk-scoring rule as part of the base system to calculate the risk score of security incidents based on user-defined criteria. However, you can customize and include additional related tables to calculate the risk score.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Define the new Risk Score Calculator Rules, Configure, Security Incident Response Workspace, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Risk Score Calculator for Additional Related Tables

The Risk Score Calculator is provisioned with one risk-scoring rule as part of the base system to calculate the risk score of security incidents based on user-defined criteria. However, you can customize and include additional related tables to calculate the risk score.

## Before you begin

Role required: sn\_si.admin.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Incidents** &gt; **Show All Incidents**.

2.  Select any security incident record.

3.  Select the **Additional actions** option next to the security incident number.

4.  Go to **Configure** &gt; **Related Lists**.

5.  Go to the View name, and select **Risk Score Calculator**.

    After you select the view, choose the required related list that you want to add from the slush bucket. For example, Associated Sightings.

6.  Select **Save**.

    You have successfully added the new related lists or tables for which you want to calculate the risk score.

    **Important:** To calculate the risk score for the security incidents that have new criteria with the newly created related lists, you have to define business rules on the base table of the related list.

7.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

    You can use the following two business rules as reference to create your own business rules:

    -   Add Security Incidents \(SIs\) to Score Calculator Queue
    -   Add Relation to Score Calculator Queue \(This is applicable for m2m tables\)
    ![Business rules](../image/risk-br-list-view.png "Business rules")

8.  For example, to get the associated observables criteria to work, we have defined two business rules.

    The first is the **Add SIs To Score Calculator Queue** business rule.

    For example, a new security incident is created and associated with an observable \(`Observables[sn_ti_observable]`\) table. After threat lookup, the observable is found to be malicious. You then need to add all the security incidents associated with this malicious observable to the Queue to recalculate the risk score of the security incidents.

    ![Add SIs To Score Calculator Queue business rule](../image/risk-br-si-score.png "Add SIs To Score Calculator Queue")

    The second is the **Add Relation To Score Calculator Queue** business rule.

    For example, a new security incident is created or deleted and associated with an observable \(`Task Observables[sn_ti_m2m_task_observable]`\) table. So, there’s a change in the association of the security incident. You then need to add that security incident to the Queue to recalculate the risk score of the security incident.

    ![Add Relation To Score Calculator Queue business rule](../image/risk-br-relation-score.png "Add Relation To Score Calculator Queue")


**Parent Topic:**[Define the new Risk Score Calculator Rules](define-risk-score-calculator-rules-sir.md)

