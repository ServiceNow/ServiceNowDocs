---
title: Determine who can conduct a training for Patient Support Services
description: Add users who can conduct the trainings for Patient Support Services to the Nurse Training Support assignment group.
locale: en-US
release: yokohama
product: Patient Support Services
classification: patient-support-services
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Patient Support Services, Patient Support Services, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Determine who can conduct a training for Patient Support Services

Add users who can conduct the trainings for Patient Support Services to the Nurse Training Support assignment group.

## Before you begin

**Important:**

Starting with the Yokohama release, Patient Support Services is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support knowledge base.

Role required: user\_admin or admin

## About this task

In the Patient Support Services application, the sn\_patientservice.nurse\_educator role is required to conduct trainings for a patient. Trainings are requested by a patient within a program associated with Patient Support Services. By default, the members of the Nurse Training Support assignment group are assigned the sn\_patientservice.nurse\_educator role.

## Procedure

-   Assign the sn\_patientservice.nurse\_educator role to the user who is conducting the training task.

    For more information, see [Assign a role to a user](https://www.servicenow.com/docs/access?context=t_AssignARoleToAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

-   Add the user who is conducting the training task to the Nurse Training Support assignment group.

    For more information, see [Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).


