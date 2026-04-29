---
title: Applications integrated with Continual Improvement Management
description: CIM provides integrations with other ServiceNow applications to enable you to create improvement initiatives from these applications. You can also create records for integrated applications from improvement initiatives.
locale: en-US
release: australia
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Overview, Continual Improvement Management, IT Service Management]
---

# Applications integrated with Continual Improvement Management

CIM provides integrations with other ServiceNow® applications to enable you to create improvement initiatives from these applications. You can also create records for integrated applications from improvement initiatives.

You can link multiple tasks from integrated applications to a single CIM task and link multiple CIM tasks to a single integrated application task.

## Applications from which you can create Improvement Initiatives

-   [Benchmarks](../../benchmarks/reference/r_Benchmarks.md)
-   [Coaching](../../cf-coaching/reference/cf-coaching-landing.md)
-   [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)
-   [Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)
-   [Demand Management](https://www.servicenow.com/docs/access?context=c_DemandManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Governance, Risk, and Compliance \(GRC\)](https://www.servicenow.com/docs/access?context=r_WhatIsGRC&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US)
-   [Idea Portal](https://www.servicenow.com/docs/access?context=idea-portal&version=australia&pubname=australia-it-business-management&ft:locale=en-US)
-   [Incident Management](../../incident-management/concept/c_IncidentManagement.md)
-   [Problem Management](../../problem-management/concept/c_ProblemManagement.md)
-   [Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=australia&pubname=australia-now-intelligence&ft:locale=en-US)
-   [Survey Management](https://www.servicenow.com/docs/access?context=r_SurveyManagementLandingPage&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

For more information, see [Create improvement initiatives from integrated applications](../task/create-improvmt-from-apps.md).

## Application records you can create from improvement initiatives

-   Change record \([Change Management](../../change-management/concept/c_ITILChangeManagement.md)\)
-   Coaching opportunity \([Coaching opportunity](../../cf-coaching/task/cf-create-coaching-opportunity.md)\)
-   Knowledge base article \([Create a knowledge article](https://www.servicenow.com/docs/access?context=create-knowledge-article&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)\)
-   Demand record \([Demand Management](https://www.servicenow.com/docs/access?context=c_DemandManagement&version=australia&pubname=australia-it-business-management&ft:locale=en-US)\)
-   Project \([Project Management](https://www.servicenow.com/docs/access?context=c_ProjectApplicationOverview&version=australia&pubname=australia-it-business-management&ft:locale=en-US)\)
-   Story record \([Agile Development](https://www.servicenow.com/docs/access?context=agile-development&version=australia&pubname=australia-it-business-management&ft:locale=en-US)\)

For more information, see [Create application records from improvement initiatives](../task/create-app-records.md).

## Summary of CIM Integration with other applications

|Application|Application record|Create improvement initiative|Create application record from improvement initiative|
|-----------|------------------|-----------------------------|-----------------------------------------------------|
|GRC|
|Audit Management|Issue record|X|--|
|Strategic Portfolio Management|
|Agile Development|Story record|--|X|
|Demand Management|Demand record|X|X|
|Project Management|Project record|--|X|
|IT Operations Management|
|CMDB|Remediate Duplicate Task record|X|--|
|IT Service Management|
|Benchmarks|Benchmarks recommendation|X|--|
|Change Management|Change record|--|X|
|Major Incident Management|Post incident review workbench|X|--|
|Problem Management|Problem record|X|--|
|Platform Capabilities|
|Knowledge Management|Knowledge base article|--|X|
|Survey Management|Survey|X|--|
|Service Management|
|Coaching|Coaching opportunity|X|X|

-   **[Integrate Continual Improvement Management using extension point](../task/integrate-extension-api.md)**  
Integrate CIM with other applications by using the CIMIntegrationAPI extension point. It defines the inbound and outbound extension points for integrating CIM with other applications.

**Parent Topic:**[Continual Improvement Management overview](../concept/get-started-cim.md)

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

[Using scripted extension points in server-side scripts](https://www.servicenow.com/docs/access?context=scripted-extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

[Using UI extension points in server-side UI macros](https://www.servicenow.com/docs/access?context=ui-extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

[Using client extension points in client-side UI scripting](https://www.servicenow.com/docs/access?context=client-extension-points&version=australia&pubname=australia-api-reference&ft:locale=en-US)

