---
title: Citrix session pre-built topics for ITSM Virtual Agent
description: Users can reset any Citrix desktop or application session using Virtual Agent conversation flows. Users can also provision a Citrix desktop or application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/itsm-virtual-agent/manage-citrix-convo-flow.html
release: zurich
product: ITSM Virtual Agent
classification: itsm-virtual-agent
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use pre-built topics, ITSM Virtual Agent, IT Service Management]
---

# Citrix session pre-built topics for ITSM Virtual Agent

Users can reset any Citrix desktop or application session using Virtual Agent conversation flows. Users can also provision a Citrix desktop or application.

Natural Language Understanding \(NLU\) is used to identify and trigger the Citrix action that a user wants to perform.

Requirement: [Citrix IT Service Management Connector](https://store.servicenow.com/sn_appstore_store.do#!/store/application/bb5ca9a2db9bd700677d3437b996190f/) \(x\_cion\_citrix\_it\_s\)

## Provision Citrix Desktop/Apps

Virtual Agent can provision a Citrix desktop or an application directly from a conversation.​ The user selects the session type. When requesting a desktop, Virtual Agent asks for the OS and returns the requested item details.

\[Omitted image "CitrixProv2.png"\] Alt text: Provision Citrix Desktop topic.

When requesting an application, Virtual Agent sends a link to the Service Portal, where the user can submit the request.

\[Omitted image "CitrixProv3.png"\] Alt text: Provision Citrix application topic.

Virtual Agent sends an actionable notification to the user to inform them once the desktop or application has been provisioned, or if the provisioning was unsuccessful.

This topic uses the Request Catalog Item [Service Catalog topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/service-catalog/request-topic-blocks-va.md).

## Reset Citrix Sessions

Virtual Agent provides a list of possible sessions to reset, and the user can choose to reset an individual session or all sessions at once.

\[Omitted image "ResetCitrix1.png"\] Alt text: Reset Citrix Sessions topic.

If the user does not have any sessions available to reset, Virtual Agent can open an Incident on behalf of the user.

\[Omitted image "ResetCitrix3.png"\] Alt text: Reset Citrix Sessions topic with new incident.

This topic uses the Create Incident [topic block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/itsm-va-topic-blocks.md).

**Parent Topic:**[Using ITSM Virtual Agent pre-built topics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/itsm-virtual-agent/using-itsm-va.md)

