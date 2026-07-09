---
title: Add a document list definition to a service definition
description: Add a document list definition to a service definition by using the Insurance claims application so that you can define the required documents that a customer needs to provide for a particular claim.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/financial-services-operations/insurance-claims/add-document-list-definition-to-service-definition.html
release: yokohama
product: Insurance Claims
classification: insurance-claims
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Creating a service definition for Insurance claims, Setting up Insurance claims, Insurance claims, Claims applications, Using insurance applications, Financial Services Operations \(FSO\)]
---

# Add a document list definition to a service definition

Add a document list definition to a service definition by using the Insurance claims application so that you can define the required documents that a customer needs to provide for a particular claim.

## Before you begin

Role required: admin

## About this task

After setting up FSO Document Processor and creating a document list definition to detail the required documents for an insurance claim, link it to the claim's service definition by updating the Insurance claims document rules decision table.

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Decision tables**.

3.  Open **Insurance claims document rules**.

4.  Add a new decision row to the decision table.

5.  In the Case service definition column, select your claim service definition.

6.  In the Answer column, select the document list record.

7.  Select **Save**.


## Result

This decision table executes in the background when a case is created through the first notice of loss playbook. It also creates a document verification task on the case.

**Parent Topic:**[Creating a service definition for Insurance claims](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/insurance-claims/create-service-definitions-for-insurance-claims.md)

**Related topics**  


[Integrating with Document Processor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/integrating-with-document-processor.md)

