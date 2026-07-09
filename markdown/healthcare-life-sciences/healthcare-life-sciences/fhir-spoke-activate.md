---
title: Activate the HL7 FHIR Spoke
description: Install the HL7 FHIR Spoke from the and verify that the required platform plugins are active so that the eight FHIR actions are available in .
locale: en-US
release: australia
topic_type: task
last_updated: "2026-06-16"
reading_time_minutes: 1
keywords: [activate, install, plugins]
---

# Activate the HL7 FHIR Spoke

Install the HL7 FHIR Spoke from the  and verify that the required platform plugins are active so that the eight FHIR actions are available in .

## Before you begin

Role required: admin

The following platform plugins must be active before the spoke's stream actions can be added to a flow:

-    \(`com.glide.hub`\)
-   Flow Designer Action Step — CORE \(`com.glide.hub.action_step.core`\)
-   REST step type \(`com.glide.hub.action_step.rest`\)
-    Action Template — Data Stream \(`com.glide.hub.action_type.datastream`\)

## About this task

HL7 FHIR Spoke is distributed as a scoped application in the . After you install it, the eight FHIR actions appear in the  action picker under the four FHIR  categories.

## Procedure

1.  Request the HL7 FHIR Spoke application from the  and install it on your instance.



2.  Navigate to **All** &gt; **System Definition** &gt; **Plugins** and confirm that the four required plugins listed in the prerequisites are active.

3.  In , create or open a flow, add an action step, and confirm that the FHIR actions appear under the Organization Management, Location Management, Practitioner Management, and PractitionerRole Management categories.


## Result

The HL7 FHIR Spoke is installed and its actions are available to flow authors. Before the actions can read from a FHIR server, configure the connection and credentials. See [Configure the HL7 FHIR connection and credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown).

