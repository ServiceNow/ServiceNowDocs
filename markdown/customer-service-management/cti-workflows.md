---
title: Computer Telephony Integration Workflows
description: Computer Telephony Integration \(CTI\) enables customer service agents to place and receive phone calls in ServiceNow applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/cti-workflows.html
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrating with Computer Telephony Integration \(CTI\), Integrate, Customer Service Management]
---

# Computer Telephony Integration Workflows

Computer Telephony Integration \(CTI\) enables customer service agents to place and receive phone calls in ServiceNow applications.

The following sample workflows show how CTI can be integrated with Interaction Management System \(IMS\) and OpenFrame \(OF\) to support outgoing and incoming telephone calls.

## CTI integration for outgoing call

The following workflow describes the logical sequence of actions when an outgoing call is triggered using the OpenFrame window.

\[Omitted image "cti-outgoing-successrejectbusy.png"\] Alt text: CTI integration work flow for outgoing call-Success and Reject/busy

## CTI integration for incoming call

The following workflow describes the logical sequence of actions when an incoming call is received using the OpenFrame window.

\[Omitted image "ctiims-workflow.png"\] Alt text: CTI and IMS integration work flow for incoming call

## CTI integration for transferring call

The following workflow describes the logical sequence of actions when an incoming call is transferred to an agent.

\[Omitted image "cti-call-transfer.png"\] Alt text: CTI integration workflow for call transfer.

## CTI call interactions operations

CTI integration with IMS and OF uses the `OpenframeInteractionUtility` script. You can use the`createOrUpdateInteractionForOpenframe` method from the utility script to create an interaction. For more information about creating interaction using APIs, see Understanding the Interaction Management API see the [Understanding the Interaction Management API \[KB1941272\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB1941272) article in the Now Support Knowledge Base.

\[Omitted image "cti-legend.png"\] Alt text: FMS and CTI integration legend.

