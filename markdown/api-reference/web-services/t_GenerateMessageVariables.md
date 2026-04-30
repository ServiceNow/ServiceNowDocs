---
title: Generate REST message variables
description: Populate the list of variable substitutions automatically based on variables defined in several REST message HTTP method fields.
locale: en-US
release: zurich
product: Web Services
classification: web-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Message variable substitution, REST, Outbound, Web services, API implementation, API implementation and reference]
---

# Generate REST message variables

Populate the list of variable substitutions automatically based on variables defined in several REST message HTTP method fields.

## Before you begin

Before starting this procedure, create a REST Message record with at least one HTTP method that uses variables.

Role required: web\_service\_admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST Message**.

2.  Select a REST Message record.

3.  Select a method from the HTTP Methods related list.

4.  Click the **Auto-generate variables** related link.

    The **Variable Substitutions** related list is automatically populated for any variables defined in the HTTP Method **Endpoint** field and the **HTTP Headers** and **HTTP Query Parameters** embedded lists. For POST and PUT messages, variables defined in the **Content** field are also used.


## What to do next

You can use the REST Message workflow activity to send the message, or click **Preview Script Usage** to get a sample script. The sample script includes a setStringParameter call for each defined variable substitution that allows you to assign a value to the variable in your script.

**Parent Topic:**[Variable substitution in outbound REST messages](../concept/c_VariableSubstitutionREST.md)

