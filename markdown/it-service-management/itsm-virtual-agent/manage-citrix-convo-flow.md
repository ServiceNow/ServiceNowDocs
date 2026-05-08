---
title: Citrix session pre-built topics for ITSM Virtual Agent
description: Users can reset any Citrix desktop or application session using Virtual Agent conversation flows. Users can also provision a Citrix desktop or application.
locale: en-US
release: australia
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Using ITSM Virtual Agent pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Citrix session pre-built topics for ITSM Virtual Agent

Users can reset any Citrix desktop or application session using Virtual Agent conversation flows. Users can also provision a Citrix desktop or application.

Natural Language Understanding \(NLU\) is used to identify and trigger the Citrix action that a user wants to perform.

Requirement: [Citrix IT Service Management Connector](https://store.servicenow.com/sn_appstore_store.do#!/store/application/bb5ca9a2db9bd700677d3437b996190f/) \(x\_cion\_citrix\_it\_s\)

Learn how the Citrix ITSM plug-in for ServiceNow can help your team easily deliver a first class experience to your end users, provide a new level of end user self-service, and free up valuable time for your IT team to focus on higher impact work.

## Provision Citrix Desktop/Apps

Virtual Agent can provision a Citrix desktop or an application directly from a conversation.​ The user selects the session type. When requesting a desktop, Virtual Agent asks for the OS and returns the requested item details.

![Provision Citrix Desktop topic.](../image/CitrixProv2.png)

When requesting an application, Virtual Agent sends a link to the Service Portal, where the user can submit the request.

![Provision Citrix application topic.](../image/CitrixProv3.png)

Virtual Agent sends an actionable notification to the user to inform them once the desktop or application has been provisioned, or if the provisioning was unsuccessful.

This topic uses the Request Catalog Item Service Catalog topic block.

## Reset Citrix Sessions

Virtual Agent provides a list of possible sessions to reset, and the user can choose to reset an individual session or all sessions at once.

![Reset Citrix Sessions topic.](../image/ResetCitrix1.png)

If the user does not have any sessions available to reset, Virtual Agent can open an Incident on behalf of the user.

![Reset Citrix Sessions topic with new incident.](../image/ResetCitrix3.png)

This topic uses the Create Incident [topic block](itsm-va-topic-blocks.md).

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](../concept/using-itsm-va.md)

