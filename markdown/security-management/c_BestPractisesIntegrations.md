---
title: Tips for writing integrations
description: Avoid some of the pitfalls you can encounter when writing your own integrations by following these guidelines.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [ServiceNow Security Operations integration development guidelines, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Tips for writing integrations

Avoid some of the pitfalls you can encounter when writing your own integrations by following these guidelines.

## Use ServiceNow platform functionality whenever possible

Mostly, the integration capabilities built into Security Operations applications \(Security Incident Response, Threat Intelligence, and Vulnerability Response\) are intended to enhance or streamline existing ServiceNow platform integration functionality. When writing integrations, always make sure to use platform functionality when it exists. Here are some common ServiceNow functionalities that can be used rather than “rolling-your-own.”

-   Outbound web services – for most interactions with third-party systems, communication are through web services. In those cases, utilize platform outbound web services \(REST and SOAP are supported\).
-   A data sources/import sets/transform map – for processing data and inserting into ServiceNow tables, the preferred mechanism is to use data sources and associated components.

## Use Security Operations integration frameworks whenever possible

Because Security Operations integration mechanisms have solved many common problems, it is not necessary to reimplement basic functionalities for every integration. For example, the vulnerability data and threat source frameworks support handling multiple pages and passing that data to data sources/transforms/import sets. Similarly, the scan or lookup source framework provides configurable rate limiting functionality. As a rule, when implementing a feature or set of features, check to see if the existing Security Operations integration framework covers your use case. If so, use that framework.

## Extend the existing Security Operations integration frameworks as needed

Most of the tables and scripts used by Security Operations integration frameworks were intended to be extended to suit future needs. If a use case is encountered while you are writing an integration, extend an integration table or script to better suit that use case.

## Provide feedback to ServiceNow for issues encountered during integration

As an integration is being developed or tested, be sure to provide feedback when issues are encountered. Even if a workaround is required, Customer Service and Support personnel can provide an improvement in future releases that could alleviate the issue for future integrations.

## Test under reasonable load

A common issue with integrations is that they are not equipped to handle realistic loads. Because each integration is a scoped application, there are more limitations imposed by the platform to ensure system stability. These limitations may result in long running jobs or API calls being terminated. You can ensure that long running processes or processes that process lots of data are handled gracefully by reducing the time each call or process takes \(usually by providing a means of paginating API requests or chunking large sets of data\).

**Parent Topic:**[ServiceNow Security Operations integration development guidelines](c_IntegrationWritingGuidelines.md)

**Related topics**  


[Types of ServiceNow integrations provided](c_TypesOfIntegrationsProv.md)

[Security Operations Integration Configurations](../../security-operations-common/concept/third-party-integrations.md)

[Integration troubleshooting](c_IntegrationTroubleshooting.md)

