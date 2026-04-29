---
title: Discovery based on Predictive Intelligence
description: Service Mapping uses data processed by Predictive Intelligence to generate suggestions for traffic-based connections.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Automated Service Suggestions, Choose method for discovering and mapping services, Exploring Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Discovery based on Predictive Intelligence

Service Mapping uses data processed by Predictive Intelligence to generate suggestions for traffic-based connections.

## Connection suggestions generated using Predictive Intelligence

Predictive Intelligence evaluates connections between application fingerprints, CIs, and processes, and ranks their relevancy. Service Mapping uses this information to create connections based on connection rules. It also generates connection suggestions for servers and load balancers for you to decide which connections to add or remove from the service instances. The confidence level indicates the likelihood of this connection being part of the service instances.

-   **High** - Commonly a connection to an internal component that is only used by this specific component or application.
-   **Medium** - Commonly a connection to a middleware component used by multiple services, such as IBM MQ or Oracle WebLogic Server.
-   **Low** - Commonly a connection to an application deployed on numerous servers in the organization, typically for monitoring purposes, such as Tivoli Enterprise Monitoring Agents or MID Server.
-   **Very low** - Commonly a connection to a central application used by the entire organization, for example, Microsoft Active Directory or Okta.

If Predictive Intelligence is enabled, Service Mapping automatically adds connections to service instances based on connection rules. These suggestions are generated using traffic-related data from the Configuration Management Database \(CMDB\) and the analysis of application fingerprints, CIs, and processes by Predictive Intelligence.

## Connection rules based on connection suggestions

Connection rules enhance the connection suggestions generated using Predictive Intelligence. Each rule contains a condition that describes an aspect of a traffic-based connection. The fields available in conditions come from the Connection Suggestion \[sa\_ml\_connection\_suggestion\] table, which is only populated when you run top-down discovery. You can base your rules directly on the connection suggestions. For example, create a rule for any connection with confidence level High. Alternatively, if you know which CIs must be part of the service instances, you can choose fields that point at these CIs.

When Service Mapping adds a connection based on connection rules, it performs the following actions:

1.  Associating the connection rule with the connection suggestion.
2.  Changing the connection suggestion **Decision** attribute to `Added By Rule`.
3.  During service rediscovery, adding one level of the actual CI connections to relevant application services.

Every time application services are rediscovered, Service Mapping adds only one level of CI connections. You may want to change the frequency in your discovery schedules to complete mapping of the application services using connection rules.

Service Mapping evaluates only active connection rules and only for connection suggestions that have the Undecided decision attribute. The system applies the rules using the following algorithm:

1.  Service Mapping checks local rules for a CI connection. If multiple rules are relevant for the same CI connection, Service Mapping uses the Order attribute for the sequence: It evaluates the rules from least to greatest Order value. By default, Service Mapping checks only 20 local rules.
2.  If a connection suggestion matches the connection rule condition, Service Mapping adds this connection to the relevant application service.
3.  If Service Mapping finds no match for local rules, the system starts evaluating and applying global rules in ascending order using the Order attribute. By default, the system checks only 20 global rules.
4.  If a connection suggestion matches the rule condition, the system adds it to all application services. If a rule is configured to exclude suggested connections from certain services, the system does not apply this rule to these services.
5.  Every time Service Mapping rediscovers application services of the manual or discovered type, it validates automatically added traffic-based connections against the active connection rules. That way the system ensures that application services contain only relevant connections based on the current and active connection rules.
6.  If a rule is no longer valid, Service Mapping changes the decision attribute for its corresponding connection suggestion to Undecided. Service Mapping also removes the association between the connection rule and the connection suggestion. Unless Service Mapping can apply a different connection rule to CI connections that became irrelevant, Service Mapping removes them from the application services.

If necessary, you can modify the number of the local or global connection rules that the system uses in the algorithm, as described in [Properties installed with Service Mapping](../reference/components-installed-with-service-mapping.md#section_g5w_lcn_c2b).

## Enabling discovery based on Predictive Intelligence

Discovery based on Predictive Intelligence works at the product level. The **sa\_ml.connection\_suggestions.active** property controls this feature. If traffic-based discovery was enabled in your deployment prior to the Quebec release and you used it to discover at least one application service, discovery based on Predictive Intelligence is disabled by default.

**Related topics**  


[Add CIs to multiple application services using connection rules](../task/add-cis-connection-rules-multiple.md)

[Add CIs for single application services using connection rules](../task/add-cis-connection-rules-single.md)

[Add or remove CIs for multiple application services using connection suggestions](../task/manipulate-connections-suggestions-in-bulk.md)

[Add or remove CIs for single application services using connection suggestions](../task/add-remove-ci-connections-services.md)

