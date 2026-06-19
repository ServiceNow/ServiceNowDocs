---
title: Create a change, incident, OT change request, or problem from a security incident
description: After you have created and saved a security incident, you can create a change request \(CHG\), incident \(INC\), OT change request, or problem \(PRB\) record from it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/t\_CrtChgOrPrbFromSI.html
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Record creation from security incidents, Security incident creation, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a change, incident, OT change request, or problem from a security incident

After you have created and saved a security incident, you can create a change request \(CHG\), incident \(INC\), OT change request, or problem \(PRB\) record from it.

## Before you begin

Role required: sn\_si.basic or higher

## Procedure

1.  Open a security incident using one of these methods.

    -   Open an exiting security incident by navigating to **Security Incident** &gt; **Unassigned** &gt; **Incidents**, and clicking a security incident.
    -   Create a security incident by navigating to **Security Incident** &gt; **Unassigned** &gt; **Incidents**, select **New**, fill out the form, and save the record.
2.  Right-click in the security incident header bar and select one of the following:

    -   **Create Change**
    -   **Create Incident**
    -   **Create Problem**
    -   **Create OT Change Request**
    **Note:**

    -   The **Create OT Change Request** option is available only when the Operational Change Management plugin \(com.sn\_ot\_chg\_mgmt\) is installed and relevant OT change role is assigned to the user.
    -   This choice applies only if the popup property \(sn\_vul.popup\) is enabled. When you select one of these buttons, a preview window opens to show you the information from the security incident that is used to create the change, incident, or problem. That is, the configuration item, its location, its priority, and the short and long descriptions. If you're creating a Change Request you can edit the **Priority**, **Short description**, and **Description** fields. If you're creating an Incident, you can edit the **Impact**, **Urgency**, **Short description** and **Description** fields. The fields in the associated security incident screen aren't affected.
3.  Select **Submit** to create the change, incident, or problem.


## Result

The change, incident, OT change request, or problem record is created and linked to the security incident.

