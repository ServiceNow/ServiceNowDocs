---
title: Data encryption for activity variables
description: You can protect sensitive data passed from Orchestration activities by encrypting input and output variables.
locale: en-US
release: yokohama
product: Orchestration
classification: orchestration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create custom activities using custom activity designer templates, Orchestration activity designer, Classic Orchestration, Data and Automation]
---

# Data encryption for activity variables

You can protect sensitive data passed from Orchestration activities by encrypting input and output variables.

The system never stores encrypted variables as clear text. If the MID Server is used to fulfill the activity, the corresponding ECC Queue's input payload is encrypted if an [encrypted output variable](../task/t_CreateAnOutputVariable.md#) is defined in the template. Output variables passed to a downstream activity as input variables maintain their encryption throughout processing.

Inputs that require data encryption come from one of these sources:

-   Workflows: These inputs are provided through the Workflow Editor and must be in the password2 format for two-way encryption.
-   Service catalog requests: These input values are provided to an activity as encrypted variables from a service catalog item.
-   GlideRecord: These are variables attached to any ServiceNow table. The source column in the table must be a password2 type variable.
-   Activity outputs: These are variables passed as outputs from one activity to a downstream activity as inputs, through the data bus.
-   Empty string: The system allows you to define encrypted input variables but never pass a value into the variable.

**Parent Topic:**[Create custom activities using custom activity designer templates](../task/create-custom-activities.md)

