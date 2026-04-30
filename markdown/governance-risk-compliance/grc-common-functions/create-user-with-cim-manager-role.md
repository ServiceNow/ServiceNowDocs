---
title: Create a user with the sn\_grc\_cim.admin role
description: Create a user with the sn\_grc\_cim.admin role to perform the tasks that are related to the content integration and import process.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [GRC: integrations with third-party content, GRC integrations, Common GRC features, Governance, Risk, and Compliance]
---

# Create a user with the sn\_grc\_cim.admin role

Create a user with the sn\_grc\_cim.admin role to perform the tasks that are related to the content integration and import process.

## Before you begin

**Note:** Ensure that you have installed the GRC: integrations with third-party content application in your instance. For more information, see [GRC: integrations with third-party content](../concept/integrations-third-party-content.md).

Role required: sn\_grc\_cim.admin, sn\_compliance.admin

## Procedure

1.  Log in to an instance with the sn\_compliance.admin role and assign the sn\_grc\_cim.admin role to a user.

    **Note:** The sn\_compliance.manager role inherits the sn\_grc\_cim.manager role. Similarly, the sn\_compliance.admin role inherits the sn\_grc\_cim.admin role.

    As a user with the sn\_grc\_cim.admin role, you can access all the APIs that are required to insert the records into the GRC: integrations with third-party content application. As a user with the sn\_grc\_cim.manager role, you have the write access to the tables of the GRC: integrations with third-party content application.

2.  Navigate to the GRC: Policy and Compliance integrator application in an instance to execute the workflow.

    For the next steps that you must do in the GRC: Policy and Compliance integrator application workflow, see [Workflow for GRC: Policy and Compliance integrator](../../grc-policy-compliance-integrator/concept/integrator-workflow.md).


**Parent Topic:**[GRC: integrations with third-party content](../concept/integrations-third-party-content.md)

