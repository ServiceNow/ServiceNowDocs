---
title: Applications integrated with Continual Improvement Management
description: CIM provides integrations with other ServiceNow applications to enable you to create improvement initiatives from these applications. You can also create records for integrated applications from improvement initiatives.
locale: en-US
release: zurich
product: Continual Improvement Management
classification: continual-improvement-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Overview, Continual Improvement Management, IT Service Management]
---

# Applications integrated with Continual Improvement Management

CIM provides integrations with other ServiceNow® applications to enable you to create improvement initiatives from these applications. You can also create records for integrated applications from improvement initiatives.

You can link multiple tasks from integrated applications to a single CIM task and link multiple CIM tasks to a single integrated application task.

## Applications from which you can create Improvement Initiatives

-   [Benchmarks](../../benchmarks/reference/benchmarks-landing.md)
-   [Coaching](../../cf-coaching/reference/cf-coaching-landing.md)
-   [Configuration Management](https://www.servicenow.com/docs/access?context=manage-cmdb&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
-   [Customer Service Management](https://www.servicenow.com/docs/access?context=c_CustomerServiceManagement&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)
-   [Demand Management](https://www.servicenow.com/docs/access?context=c_DemandManagement&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)
-   [Governance, Risk, and Compliance \(GRC\)](https://www.servicenow.com/docs/access?context=r_WhatIsGRC&version=zurich&pubname=zurich-governance-risk-compliance&ft:locale=en-US)
-   [Idea Portal](https://www.servicenow.com/docs/access?context=idea-portal&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)
-   [Incident Management](../../incident-management/concept/c_IncidentManagement.md)
-   [Problem Management](../../problem-management/concept/c_ProblemManagement.md)
-   [Process Mining](https://www.servicenow.com/docs/access?context=process-mining&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US)
-   [Survey Management](https://www.servicenow.com/docs/access?context=r_SurveyManagementLandingPage&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
-   [Vendor Management Workspace](../../vendor-management-workspace/reference/vendor-management-workspace-landing-page.md)

For more information, see [Create improvement initiatives from integrated applications](../task/create-improvmt-from-apps.md).

## Application records you can create from improvement initiatives

-   Change record \([Change Management](../../change-management/concept/c_ITILChangeManagement.md)\)
-   Coaching opportunity \([Coaching opportunity](../../cf-coaching/task/cf-create-coaching-opportunity.md)\)
-   Knowledge base article \([Create a knowledge article](https://www.servicenow.com/docs/access?context=create-knowledge-article&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)\)
-   Demand record \([Demand Management](https://www.servicenow.com/docs/access?context=c_DemandManagement&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)\)
-   Project \([Project Management](https://www.servicenow.com/docs/access?context=c_ProjectApplicationOverview&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)\)
-   Story record \([Agile Development 2.0](https://www.servicenow.com/docs/access?context=agile-landing-page&version=zurich&pubname=zurich-it-business-management&ft:locale=en-US)\)

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

-   **[Create improvement initiatives from integrated applications](../task/create-improvmt-from-apps.md)**  
Create improvement initiatives from applications integrated with Continual Improvement Management to enable planning, implementation, monitoring, and impact assessment of improvements in a centralized framework.
-   **[Create application records from improvement initiatives](../task/create-app-records.md)**  
Create records for integrated applications from improvement initiatives or CIM tasks to transform improvement initiatives into broader, actionable efforts to enable improvements across teams and processes.
-   **[Configure CIM integration property](../task/configure-cim-int-property.md)**  
Configure the CIM sn\_cim.initiative\_copy\_attributes integration property to define field values to be copied from an improvement initiative to application records that you create from the initiative.

**Parent Topic:**[Continual Improvement Management overview](../concept/get-started-cim.md)

**Related topics**  


[Using extension points to extend application functionality](https://www.servicenow.com/docs/access?context=extension-points&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

[Using scripted extension points in server-side scripts](https://www.servicenow.com/docs/access?context=scripted-extension-points&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

[Using UI extension points in server-side UI macros](https://www.servicenow.com/docs/access?context=ui-extension-points&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

[Using client extension points in client-side UI scripting](https://www.servicenow.com/docs/access?context=client-extension-points&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

