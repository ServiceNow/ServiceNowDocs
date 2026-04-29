---
title: Create a change, incident, or problem from a security incident
description: After you have created and saved a security incident, you can create a change request \(CHG\), incident \(INC\), or problem \(PRB\) record from it.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Record creation from security incidents, Security incident creation, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a change, incident, or problem from a security incident

After you have created and saved a security incident, you can create a change request \(CHG\), incident \(INC\), or problem \(PRB\) record from it.

## Before you begin

Role required: sn\_si.basic or higher

## Procedure

1.  Open a security incident using one of these methods.

    -   Open an exiting security incident by navigating to **Security Incident** &gt; **Unassigned** &gt; **Incidents**, and clicking a security incident.
    -   Create a security incident by navigating to **Security Incident** &gt; **Unassigned** &gt; **Incidents**, click **New**, fill out the form, and save the record.
2.  Right-click in the security incident header bar and click one of the following:

    -   **Create Change**
    -   **Create Incident**
    -   **Create Problem**
    **Note:** This choice applies only if the popup property \(sn\_vul.popup\) is enabled. When you click one of these buttons, a preview window opens to show you the information from the security incident that is used to create the change, incident, or problem. That is, the configuration item, its location, its priority, and the short and long descriptions. If you are creating a Change Request you can edit the **Priority**, **Short description**, and **Description** fields. If you are creating an Incident, you can edit the **Impact**, **Urgency**, **Short description** and **Description** fields. The fields in the associated security incident screen are not affected.

3.  Click **Submit** to create the change, incident, or problem.


