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
-   Configuration Management
-   Customer Service Management
-   Demand Management
-   Governance, Risk, and Compliance \(GRC\)
-   Idea Portal
-   [Incident Management](../../incident-management/concept/c_IncidentManagement.md)
-   [Problem Management](../../problem-management/concept/c_ProblemManagement.md)
-   Process Mining
-   Survey Management

For more information, see [Create improvement initiatives from integrated applications](../task/create-improvmt-from-apps.md).

## Application records you can create from improvement initiatives

-   Change record \([Change Management](../../change-management/concept/c_ITILChangeManagement.md)\)
-   Coaching opportunity \([Coaching opportunity](../../cf-coaching/task/cf-create-coaching-opportunity.md)\)
-   Knowledge base article \(Create a knowledge article\)
-   Demand record \(Demand Management\)
-   Project \(Project Management\)
-   Story record \(Agile Development\)

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


[bundle-crapiref.extension-points]

[bundle-crapiref.scripted-extension-points]

[bundle-crapiref.ui-extension-points]

[bundle-crapiref.client-extension-points]

