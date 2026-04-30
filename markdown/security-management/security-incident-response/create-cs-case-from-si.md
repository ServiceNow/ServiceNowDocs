---
title: Create a Customer Service case from a security incident
description: Security Incident Response ships with a default field mapping that maps a security incident to a Customer Service \(CS\) case. You can create a CS case from any security incident, edit the Priority, and also add Optional notes.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Record creation from security incidents, Security incident creation, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create a Customer Service case from a security incident

Security Incident Response ships with a default field mapping that maps a security incident to a Customer Service \(CS\) case. You can create a CS case from any security incident, edit the **Priority**, and also add **Optional notes**.

## Before you begin

Role required: sn\_si.basic and sn\_customerservice\_agent

**Note:** The Customer Service plugin must be activated to perform this task.

## Procedure

1.  Navigate to **Security Incident**.

2.  Open the security incident that you want to add a CS case to.

3.  Click **Create Customer Service Case** in the top header.

    ![Create Customer Service button](../image/CreateCSCase.png)

    The pop-up window is prepopulated with information from the security incident based on your field mapping.

4.  You can select a new **Priority** and add any **Optional notes**.

    **Note:** The **Priority** field overwrites the default setting. The **Optional notes** are appended to the incident.

    ![Create Customer Service case](../image/CreateCSMPopup.png)

5.  Click **Submit.**

    A CS case is created and displayed in the Customer Service Cases related list in the security incident.

6.  You can click the CS case link to follow up on the case.


**Related topics**  


[Customer service case management](https://www.servicenow.com/docs/access?context=configure-csm-case-management&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)

