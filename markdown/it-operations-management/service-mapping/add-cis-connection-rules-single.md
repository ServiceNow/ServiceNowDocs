---
title: Add CIs for single application services using connection rules
description: Create rules for automatically adding traffic-based connections and the CIs they lead to in discovered service instances. Add CIs to specific application services using connection rules.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Map a single application service using classic Service Mapping, Application service mapping using classic Service Mapping, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Add CIs for single application services using connection rules

Create rules for automatically adding traffic-based connections and the CIs they lead to in discovered service instances. Add CIs to specific application services using connection rules.

## Before you begin

-   Analyze the infrastructure you are mapping to identify the most common connections. These common connections are good candidates for connection rules.
-   Confirm that discovery based on Predictive Intelligence is enabled. Navigate to the System Property \[sys\_properties\] table and verify that the **sa\_ml.connection\_suggestions.active** property is set to **True**.
-   [Discover applications based on fingerprints](../../discovery/task/discover-application-based-process.md).

Role required: service\_mapping\_admin

## About this task

Connection rules enhance the connection suggestions generated using Predictive Intelligence. Each rule contains a condition that describes an aspect of a traffic-based connection. The fields available in conditions come from the Connection Suggestion \[sa\_ml\_connection\_suggestion\] table, which is only populated when you run top-down discovery. You can base your rules directly on the connection suggestions. For example, create a rule for any connection with confidence level High. Alternatively, if you know which CIs must be part of the service instances, you can choose fields that point at these CIs.

You can create connection rules that apply to specific application services or to all application services. If the rule is for a specific service, but the rule condition points at a CI that is part of multiple services, Service Mapping adds this CI to all relevant services.

For information about Service Mapping evaluating and applying connection rules, see [Traffic-based discovery in Service Mapping](../concept/traffic-based-discovery.md).

In addition to connection rules that add CIs to specific services, you can [create rules for adding CIs to multiple application services](add-cis-connection-rules-multiple.md).

## Procedure

1.  Navigate to **Service Mapping** &gt; **Administration** &gt; **Connection Rules**.

    Alternatively, from a service application map, select **Suggestions** &gt; **Local Rules**.

2.  Create a new connection rule by clicking **New**.

    Alternatively, customize an existing rule by clicking the rule name in the list.

3.  Select **Active** to start using this connection rule.

    Service Mapping evaluates only active connection rules.

4.  Enter a unique and meaningful name in the **Name** field.

5.  Enter the value that Service Mapping uses for the sequence in the **Order** field.

6.  Configure the filter condition in the **Condition** area.

    1.  Select the field, operator, and the value.

        For example, to add outgoing connections for any Tomcat server, configure the following filtering condition.

        ![Filtering condition for Tomcat](../image/connection-rule-condition-example.png)

    2.  To create an additional filtering condition, click **Add Filter Condition**.

    3.  To create an additional filtering condition using the OR operator, click **Add "OR" Clause**.

7.  Select `Local` from the **Scope** list.

8.  From the **Discovered Application Service** list, select an existing service to which this rule applies.

9.  Click **Update**.


## What to do next

Verify that Service Mapping added CIs as expected by performing the following steps:

1.  Open the map for the application service you selected for this connection rule.
2.  Click **Discover** at the top of the map window.
3.  After the application service is rediscovered, check that CIs are added correctly based on the connection rule.

**Parent Topic:**[Map a single application service using classic Service Mapping](t_DefineNewBusinessService.md)

