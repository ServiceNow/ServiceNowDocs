---
title: Integrating Customer Service Problem Management with southbound external systems
description: If you have a Customer Service Problem Management subscription, you can submit outbound service test run requests to various external systems by integrating the Customer Service Problem Management application with the external southbound systems.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Customer Service Problem Management]
---

# Integrating Customer Service Problem Management with southbound external systems

If you have a Customer Service Problem Management subscription, you can submit outbound service test run requests to various external systems by integrating the Customer Service Problem Management application with the external southbound systems.

## Overview of southbound test

When the tests are executed, requests are sent to the southbound test and diagnostics systems. These systems then determine the test outcomes and identify any failures.

Using this integration, a Communications Service Provider \(CSP\) can do the following tasks:

-   Trigger outbound requests for one or more service test runs by using the TeleManagement Forum \(TMF\) 653 Open POST order API.
-   Share updates with the external systems about the inflight changes to the existing test runs that have outbound requests.
-   Manage the inbound response of the outbound requests for the test run.
-   Manage the errors and exceptions for the outbound requests and inbound responses.

## How the integration works

The integration process for CSPM with the external service test management systems is as follows:

1.  As the administrator, you activate the Test Specification Open API to capture the test runs from the service problem case.

    To learn more, see [Service Test Management Open API](https://www.servicenow.com/docs/access?context=service-test-management-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

2.  The integration now begins:
    1.  The test manager creates the test run in the test run table.
    2.  The generated payload is sent to the endpoint of the external fulfillment system.

        For more information on configuring external system endpoints by creating an integration request, see [Workflow Studio flow integrations](https://www.servicenow.com/docs/access?context=flow-designer-integrations&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

        **Note:**

        -   If the test run is configured as hierarchical in the decision table, the system sends all the child service test runs in the hierarchy to the external system that is configured in the application spoke selector.
        -   If the test run is configured as non-hierarchical in the decision table, the systems send only the individual test run to the external system that is configured in the application spoke selector.
        To learn more about spokes, see [Building spokes using Spoke Generator](https://servicenow.com/docs/csh?topicname=spoke-builder&version=vancouver&pubname=vancouver-build-workflows).

3.  If the fulfillment request is successful, a response is received from the external system and is captured in the Test Run table \(sn\_st\_mgmt\_test\).

    **Note:** The customer must fill the id field of the test measures.


