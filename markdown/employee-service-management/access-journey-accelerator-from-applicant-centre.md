---
title: Configure pre-hire experience on applicant center
description: Provide continuity in the hiring journey by providing a pre-hire experience on the applicant center.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Applicant Center, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Configure pre-hire experience on applicant center

Provide continuity in the hiring journey by providing a pre-hire experience on the applicant center.

## About this task

Provide applicants with a seamless experience for pre-hire tasks from the applicant center portal. Hired applicants can start their onboarding journey from the applicant center even before their joining day.

## Before you begin

Role required: admin

## Procedure

1.  Create a script in global scope to delete roles.

    For details, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

    **Note:** You may use `hiringdeleteroles.xml`, an existing script to delete roles.

2.  Write the following business rules for an applicant user when the application state becomes hired.

    For details, see [Create a business rule for your service](../../universal-request/task/ur-create-busrule-service.md)

    1.  Delete an external applicant role: **sn\_ta\_hiring\_core.external\_applicant**.

    2.  Create an internal applicant role: **sn\_ta\_hiring\_core.internal\_applicant**.

3.  Copy the journey menu from the employee center portal to the applicant center portal.

4.  Link the applicant center user to the HR profile and create an onboarding journey using the same applicant user.

    For details, see [Create a journey](../../human-resources/task/jny-dsgnr-create-journey.md)


## Result

The applicants are assigned internal roles and they can start their pre-boarding journey from the applicant center giving them a seamless experience with the organization.

**Note:** Giving internal roles to applicants enables access to other portals intended only for employees \(default users\).

**Parent Topic:**[Configuring Applicant Center](../concept/config-applicant-center.md)

