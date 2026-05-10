---
title: Connection Suggestions list
description: Review details of connection suggestions to decide which connections are relevant for application services.
locale: en-US
release: australia
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Connection Suggestions list

Review details of connection suggestions to decide which connections are relevant for application services.

<table id="table_gq2_nkh_2nb"><thead><tr><th>

Column

</th><th>

Description

</th></tr></thead><tbody><tr><td>

From

</td><td>

The CI class or fingerprint process of the CI that is the connection source. This field appears only when you access connection suggestions by navigating to **Service Mapping** &gt; **Administration** &gt; **Connection Suggestions**.

</td></tr><tr><td>

To

</td><td>

The CI class, or fingerprint, or process of the CI that is the connection target.

</td></tr><tr><td>

Target Host

</td><td>

The host of the CI that is the connection target.If the [**VIP**](connection-suggestions-list.md#VIP-connect-suggest) column shows **true**, the target host is a load balancer member. When you select such a target host, the system adds the load balancer and all its members as CIs in the application service.

</td></tr><tr><td>

IP

</td><td>

The IP of the CI that is the connection target.

</td></tr><tr><td>

Port

</td><td>

The port of the CI that is the connection target.

</td></tr><tr><td>

Confidence

</td><td>

The confidence level indicates the likelihood of this connection being part of the service instances.

-   **High** - Commonly a connection to an internal component that is only used by this specific component or application.
-   **Medium** - Commonly a connection to a middleware component used by multiple services, such as IBM MQ or Oracle WebLogic Server.
-   **Low** - Commonly a connection to an application deployed on numerous servers in the organization, typically for monitoring purposes, such as Tivoli Enterprise Monitoring Agents or MID Server.
-   **Very low** - Commonly a connection to a central application used by the entire organization, for example, Microsoft Active Directory or Okta.

If the confidence level appears as **N/A**, wait until the application fingerprints training is complete. See the [Application fingerprint training status report](readiness-dashboard-ml.md).

 Confidence level is available only if fingerprint based discovery is enabled. See [Discover applications based on fingerprints](../../discovery/task/discover-application-based-process.md) for more information.

</td></tr><tr><td>

Decision

</td><td>

This value indicates the outcome of the previous action taken on this connection suggestion:-   **Added manually** - You added a connection based on this suggestion.
-   **Excluded manually** - You removed a connection based on this suggestion.
-   **Undecided** - You reset the previous decision to add or remove a connection based on this suggestion.
-   **Added by rule** - Service Mapping added a connection based on a connection rule.

</td></tr><tr><td>

Rule

</td><td>

The rule that Service Mapping applied to add a connection.

</td></tr><tr><td id="VIP-connect-suggest">

VIP

</td><td>

The target host is a load balancer member. The system shows this information only for load balancers that you previously discovered using horizontal discovery. This field appears only when you access connection suggestions by navigating to **Service Mapping** &gt; **Administration** &gt; **Connection Suggestions**.

</td></tr><tr><td>

Decision changed by

</td><td>

The user who changed the decision last time.If the decision was changed by a rule, this field shows the MID Server user. For more information about setting up MID Server user role, see [Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server/t_SetupMIDServerRole.md).

 This field appears only when you access connection suggestions by navigating to **Service Mapping** &gt; **Administration** &gt; **Connection Suggestions**.

</td></tr><tr><td>

Updated

</td><td>

The timestamp of when this connection last changed.

</td></tr></tbody>
</table>**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

**Related topics**  


[Discovery based on Predictive Intelligence](../concept/predictive-intelligence-discovery.md)

[Add or remove CIs for single application services using connection suggestions](../task/add-remove-ci-connections-services.md)

[Add or remove CIs for multiple application services using connection suggestions](../task/manipulate-connections-suggestions-in-bulk.md)

