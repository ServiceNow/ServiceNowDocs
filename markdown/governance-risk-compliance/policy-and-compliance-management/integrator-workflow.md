---
title: Workflow for GRC: Policy and Compliance integrator
description: You can install the GRC: Policy and Compliance integrator application from the ServiceNow Store and execute the workflow to complete the data import process.
locale: en-US
release: yokohama
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [GRC: Policy and Compliance integrator, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Workflow for GRC: Policy and Compliance integrator

You can install the GRC: Policy and Compliance integrator application from the ServiceNow Store and execute the workflow to complete the data import process.

The GRC: Policy and Compliance integrator application workflow consists of the following steps:

1.  Download the GRC: Policy and Compliance integrator application from the ServiceNow Store. When you download the GRC: Policy and Compliance integrator application, the GRC: integrations with third-party content and Policy and Compliance Management applications are automatically downloaded in your instance.
2.  Log in with the sn\_compliance.admin role into an instance and assign the sn\_grc\_cim.admin role to a user.
3.  Use the APIs and staging tables that are supported with the applications and move the data from the staging tables into the GRC: Policy and Compliance Management application.

    For more information about how to integrate batch records and assign library import tasks with the GRC: Policy and Compliance Management application, see [Using the GRC: Policy and Compliance integrator to display batch records and import tasks](integrator-in-classic-ui.md), [Accessing the batch records in the content integration batch table](api-batch.md), and [Assign a library import task for approval](../task/assign-lib-import-task.md).


