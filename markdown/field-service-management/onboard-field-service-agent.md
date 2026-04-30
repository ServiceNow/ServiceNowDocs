---
title: Onboard agents on the Field Service Contractor Portal
description: Onboard a Field Service agent so the contractor company can assign outsourced work order tasks to be performed at the customer location by that agent.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Field Service Contractor Portal, Using Field Service Management, Field Service Management]
---

# Onboard agents on the Field Service Contractor Portal

Onboard a Field Service agent so the contractor company can assign outsourced work order tasks to be performed at the customer location by that agent.

## Before you begin

Role required: wm\_ext\_manager

## Procedure

1.  In a web browser, enter this text in the address bar: `instance.service-now/fsmcp` where *instance* is the first part of an instance URL.

2.  Click **Requests** &gt; **Onboard Agent** in the header menu.

3.  On the form, fill in the fields.

4.  |Field|Description|
|-----|-----------|
|First name|Agent’s first name.|
|Last name|Agent’s last name.|
|User ID|Auto-populated unique identifier for this user. The user ID follows the format `firstname.lastname`.|
|Assignment Group|Group name to which the agent belongs. For example, external.|
|Email|Email address of the agent.|
|Company|Name of the employer.|
|Mobile phone|Mobile number of the agent.|
|Business phone|Phone number of the agent.|
|Additional Manager|Option to assign additional manager role to the agent to handle managerial activities in the absence of primary external manager.|
|Geolocation tracked|Option to enable tracking the real-time location of agent.|

5.  Click **Submit**.


## Result

An external agent of the contractor company is onboarded and the internal manager receives an approval request for the agent.

## What to do next

The internal manager receives a request to approve the onboarding of an agent. For more information, see [Approve or reject requests for onboarding agents](Approve-reject-request-onboard-agent.md).

**Parent Topic:**[Field Service Contractor Portal](../concept/field-service-contractor-portal.md)

