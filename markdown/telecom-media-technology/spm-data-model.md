---
title: Customer Service Problem Management data model
description: Customer Service Problem Management \(CSPM\) provides a framework that enables you to follow a structured approach to handle and resolve customer-reported issues. The framework ensures a seamless and satisfactory customer experience.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Customer Service Problem Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Customer Service Problem Management data model

Customer Service Problem Management \(CSPM\) provides a framework that enables you to follow a structured approach to handle and resolve customer-reported issues. The framework ensures a seamless and satisfactory customer experience.

CSPM follows the TeleManagement Forum \(TMF\) defined framework to manage service problems. These problems arise when customers experience service disruptions, or when the network operations center \(NOC\) team identifies network faults and raise complaints, such as service disruptions, errors, or other issues. The CSPM application focuses on the test diagnostic capability to resolve service problems. This includes conducting relevant tests to diagnose the root cause of the problem and then suggesting resolutions based on the test results.

## Customer Service Problem Management data model life cycle

CSPM enables a service-related problem to move through the various stages of Service Problem Management's life cycle to get resolved.![Different stages of Customer Service Problem Management life cycle](../image/mmasset0020424-customer-service-problem-management-lifecycle-landing.png)

|Stage|Description|
|-----|-----------|
|Verify|Verify the case created for a service problem experienced by the customer. This includes reviewing the details provided in the case. If necessary, the agent can also modify the service based on the problem. Based on these details, the system suggests the diagnostic tests.|
|Diagnose|System-derived test specifications, defined during the initial setup. These specifications are crucial for diagnosing the root cause of service problems. Agents can run these tests immediately or schedule them for a later time. Additionally, the system enables agents to view and run these tests.|
|Repair|Based on the diagnostic test results, the system generates the repair tasks to fix the problem.|
|Test and Resolve|Service problem fulfillment coordination that follows the fulfillment flow.|
|Close|Final step in the Service Problem Management life cycle.|

## Customer Service Problem Management data model

The following diagram shows the applications, tables, and their relationships that build the CSPM data model.![Data model of Customer Service Problem Management](../image/mmasset0020436-serviceprbmodel.png)

The CSPM data model uses a combination of these tables to store data:

-   Tables that are from the Service Test Management application includes the following tables:
    -   Test Definition
    -   Test Measure Definition
    -   Test Definition Characteristics
    -   Test Definition Relationship
    -   Specification to Test Definition Relationship
    -   Threshold Rule
    -   Measure Consequences
    -   Diagnostic Task
    -   Resolution Task
-   Table that is from the Customer Service Problem Management application includes, service problem case.

The Customer Service Problem Management \(CSPM\) data model relies on Northbound and Southbound APIs to manage and execute test processes.

Northbound APIs play a critical role during the design phase by creating and managing essential components like test definitions, characteristics, measures, and thresholds. These APIs enable the CSPM system to define the specifications and parameters for each test, such as the test type and scope, which are then used to generate unique test runs with identifiers, such as external IDs or sys\_id. After these test definitions are established, Northbound APIs facilitate the creation of test runs based on these predefined specifications. If a test requires further breakdown into smaller tasks, the Northbound APIs handle this decomposition. For more information, see [Service Test Management Open API](https://www.servicenow.com/docs/access?context=service-test-management-api&version=australia&pubname=australia-api-reference&ft:locale=en-US).

Southbound APIs come into the picture when it’s time to execute the tests. For example, if the test involves running a speed test, it isn’t conducted directly on your system but instead on an external device, such as a router or another network component. The Southbound APIs are responsible for sending these test instructions to the external systems where the tests are to be performed. For more information, see [Integrating Customer Service Problem Management with southbound external systems](../concept/cspm-integrate-southbound.md).

Overall, Northbound APIs are used to design and set up the tests within the CSPM application, while Southbound APIs handle the execution of these tests on external systems. This two-tiered approach promotes a seamless flow from test definition to execution across different platforms.

