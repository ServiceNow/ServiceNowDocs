---
title: Add a security incident to a security case
description: If you determine that a security incident requires a higher level of analysis, add it to a new or existing case.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Record creation from security incidents, Security incident creation, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Add a security incident to a security case

If you determine that a security incident requires a higher level of analysis, add it to a new or existing case.

## Before you begin

The Threat Intelligence plugin must be activated to use Security Case Management.

Role required: sn\_si.admin, sn\_ti.case\_user\_write

## Procedure

1.  Navigate to the security incident that requires escalation by clicking **Security Incident** &gt; **Incidents** &gt; **Assigned to Me**, and open the security incident.

2.  Click the **Add to Security Case** related link.

    The **Add Security Incident\(s\) to Security Case** dialog box opens.

    ![Add this security incident to an existing or new case](../image/AddSecIncToCase2.png)

3.  If you have a case assigned to you that you want to add this security incident to, fill in the fields as appropriate, then click **Submit**.

    |Field|Description|
    |-----|-----------|
    |Security Case|Select the security case.|
    |Optional notes|As needed, enter additional notes that would be of value to the case analyst.|

4.  If you have one or more cases assigned to you, but want to create a new case and assign the security incident to it, click **Create new case** to show additional fields.

    ![Add this security incident to a new case](../image/AddSecIncToCase.png)

    **Note:** If you do not have any cases assigned to you, the screen above opens first.

5.  Fill in the fields as appropriate.

    |Field|Description|
    |-----|-----------|
    |Security Case Name|Enter the name of the new security case.|
    |Description|Enter a description for the case.|
    |Case Type|Select the type of case being investigated.|
    |Optional notes|As needed, enter additional notes that would be of value to the case analyst.|

6.  Click **Submit**.

    A message appears at the top of the security incident, along with a link to the new case.


**Related topics**  


[Security Case Management](../../threat-intelligence-case-management/concept/case-mgmt.md)

