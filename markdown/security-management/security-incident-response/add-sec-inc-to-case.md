---
title: Add a security incident to a security case
description: If you determine that a security incident requires a higher level of analysis, add it to a new or existing case.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
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

2.  Select the more actions icon \(![](../image/more-actions-icon.png) and select **Add to Security Case**.

    The **Add Security Incident\(s\) to Security Case** dialog box opens.

3.  If you have a case assigned to you that you want to add this security incident to, fill in the fields as appropriate, then select **Submit**.

    |Field|Description|
    |-----|-----------|
    |Security Case|Select the security case.|
    |Optional notes|As needed, enter additional notes that would be of value to the case analyst.|

4.  If you have one or more cases assigned to you, but want to create a case and assign the security incident to it, select **Create New Case** to show additional fields.

5.  Fill in the fields as appropriate.

    |Field|Description|
    |-----|-----------|
    |Security Case Name|Enter the name of the new security case.|
    |Description|Enter a description for the case.|
    |Case Type|Select the type of case being investigated.|
    |Optional notes|As needed, enter additional notes that would be of value to the case analyst.|

6.  Select **Create**.

    A message appears at the top of the security incident, along with a link to the new case.


**Related topics**  


[Security Case Management](../../threat-intelligence-case-management/concept/case-mgmt.md)

