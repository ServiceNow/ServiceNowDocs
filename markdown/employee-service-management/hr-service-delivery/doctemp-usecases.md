---
title: Use Cases
description: Possible use cases for Document Templates.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Exploring Document Templates, Document Templates, E-signature applications of HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Use Cases

Possible use cases for Document Templates.

## Submitting and approving a document online

![Submit and review a document online.](../image/doc-template-workflow.png)

This is a use case where a document is to be filled out by an employee and reviewed by an HR agent.

An administrator configures an HR service \(by selecting a document template and enabling the case option\) and creates a case with that HR service. When the state of the case changes to Ready or Work in progress, document tasks get initiated for both employee and HR agent.

The employee fills in the details and submits the document for review. If there are no corrections, the HR agent approves the document, else, the HR agent adds notes and rejects the document.

Document tasks are again initiated for both employee and HR agent. The employee makes the appropriate revisions and resubmits the document. After the HR agent approves the document, it gets added as an attachment to the case.

## Completing onboarding activities for an employee

This is a use case where an employee requires to complete onboarding activities such as submitting a document, requesting an ID card, and requesting a laptop.

An administrator configures an HR service \(by selecting the document template and enabling the case option\) and configures an activity in a life cycle event with that HR service.

When the lifecycle activity is triggered, a case gets created with that HR service. When the state of the case changes to Ready or Work in progress, a document task gets initiated for the employee. After all the tasks of the HR case are complete, the document \(submitted by the employee\) gets added as an attachment to the case.

