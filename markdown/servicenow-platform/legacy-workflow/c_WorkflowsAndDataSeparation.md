---
title: Workflows and data separation
description: Data separation restricts workflow contexts to users who are either in the same domain of the workflow or are members of a parent domain.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow concepts, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Workflows and data separation

Data separation restricts workflow contexts to users who are either in the same domain of the workflow or are members of a parent domain.

![](../image/WorkflowAndDataSeparation.png "Workflow and data separation")

Workflow records in the Workflow Contexts \[wf\_contexts\] table are considered data. Data separation restricts workflow contexts to users who are either in the same domain of the workflow or are members of a parent domain. While a user in a parent domain can see running workflows in a child domain, a user in a child domain cannot see running workflows in a parent domain. If necessary, administrators can use visibility or contains domains to expand who can see domain-specific data.

For example, when an ACME user requests something from the service catalog, a Service Catalog Request workflow context is created in the ACME domain. Similarly, a service catalog request from an Initech user creates a workflow context in the Initech domain. An MSP user in the TOP domain can see both workflow contexts because it is the parent domain for both the ACME and Initech domains. However when an ACME or Initech user logs in, data separation prevents them from seeing each other's service catalog requests. This is expected behavior because each workflow context contains data specific to that domain, such as the item requested and the request's approval history.

