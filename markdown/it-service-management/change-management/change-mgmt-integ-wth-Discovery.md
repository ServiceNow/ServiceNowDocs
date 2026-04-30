---
title: Change Management integration with ITOM Visibility
description: If your organization is subscribed to ITOM Discovery or ITOM Visibility, integration with these ITOM products is automatically enabled. With this integration, any configuration item \(CI\) with an IP address that is part of a change request process can be maintained automatically. Change request fulfillers can also manually request the discovery process for a CI.
locale: en-US
release: zurich
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Change management integrations, Reference, Change Management, IT Service Management]
---

# Change Management integration with ITOM Visibility

If your organization is subscribed to ITOM Discovery or ITOM Visibility, integration with these ITOM products is automatically enabled. With this integration, any configuration item \(CI\) with an IP address that is part of a change request process can be maintained automatically. Change request fulfillers can also manually request the discovery process for a CI.

## Enabling integration

Depending on subscriptions purchased by your organization, you must install and configure the following plugins:

-   For ITOM Discovery - the Discovery plugin \(com.snc.discovery\)
-   For ITOM Visibility - the Discovery plugin \(com.snc.discovery\) and Service Mapping plugin \(com.snc.service-mapping\)

## Integration with ITOM Discovery

When Discovery is activated, Change Management exposes three new properties within the Change Properties module \(**Change Management** &gt; **Administration** &gt; **Change Properties**\):

<table id="table_jh5_w4s_jdb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configures how discovery is triggered for Affected CIs \(automatically, manually or off\)

</td><td>

Determines whether to trigger discovery for the affected CIs automatically, manually, both, or not at all.Type: Choice list

 Values: Off, Both, Automatic, Manual

 Default value: Off

 **Note:** If the property below is set to Both, and you trigger discovery manually, then the automatic discovery will not be triggered for that change request.

</td></tr><tr><td>

List of Change Request states \(comma-separated\) where discovery can be triggered manually

</td><td>

Defines the change request state values to allow discovery to be manually initiated. For these defined state values, the Initiate Discovery related link is available.Type: String

 Default value: Implement, Review

 **Note:** If there are multiple languages used on the instance, then this property needs to be set to the internal state value for Review.

</td></tr><tr><td>

List of Change Request states \(comma-separated\) where discovery triggers automatically. E.g. when the Change Request's state changes to Review

</td><td>

Defines the change request state values for which discovery is automatically triggered. Discovery initiates when transitioning to the state values listed.Type: String

 Default values: Review

 **Note:** If there are multiple languages used on the instance, then this property needs to be set to the internal state value for Review.

</td></tr></tbody>
</table>**Note:** For the last two properties in the above table, if there are multiple languages used on the instance, then the property needs to be set to the internal value, which is 0, for Review.

In addition to the new properties, the **Discovery State** and the **Discovery last updated** fields get added to the **Affected CI** related list. **Discovery State** provides one of five status values and a corresponding icon to reflect that status:

-   In Progress
-   Completed Successfully
-   Completed w/Warning
-   Completed w/Error
-   Cancelled

The Discovery State value is presented as a link to the corresponding Discovery log file. The **Discovery last updated** field contains a date and time stamp indicating the last time Discovery was executed.

If you have opted to manually initiate the Discovery module, or opted for both manual and automatic initiation, then the **Initiate Discovery** related link appears in the Related Links section when the state of the change request matches one of the defined states in the property. When Discovery is triggered, the values in the **Discovery State** and the **Discovery last updated** fields change.

![change management integration with discovery](../image/cm-integration-discovery.png "Change management integration with discovery")

## Integration with ITOM Visibility

You can view the changes in the context of application services. Service maps available in Service Mapping show changes to an application service as a whole and to the individual configuration items \(CIs\) comprising the service.

If the ServiceNow AI Platform is configured to validate changes, all changes are evaluated and rendered as valid or not. If a change is valid, its change record on the service instance map is marked as approved. For more information about configuring the platform for change validation, see [Managing proposed changes](https://www.servicenow.com/docs/access?context=c_ProposedChanges&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US).

The type of change mark depends on the nature of changes that it represents:

-   **Light gray balloon \(![Light grey balloon icon](../../service-mapping/image/ChangeHistoryBalloonsLightGray.png)\)**

    Unapproved change that does not influence the service instance behavior. For example, a change in a network path or adding a node to a cluster.

-   **Dark gray balloon \(![Dark gray balloon icon](../../service-mapping/image/ChangeHistoryBalloonsDarkGray.png)\)**

    Unapproved change that changes the service instance behavior.

-   **Green balloon \(![Green balloon icon](../../service-mapping/image/ChangeHistoryBalloonsGreen.png)\)**

    An approved change in deployments where the ServiceNow AI Platform is configured to validate changes.

-   **Double balloon \(![Green balloon icon](../../service-mapping/image/ChangeHistoryBalloonsDouble.png)\)**

    Multiple separate changes that happened a short time from each other.


**Parent Topic:**[Change management integrations](change-mgmt-integrations.md)

**Related topics**  


[Discovery](https://www.servicenow.com/docs/access?context=r-discovery&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)

[View the change history of application services](https://www.servicenow.com/docs/access?context=t_ViewCIChanges&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)

[View the change history of application services in Agent Workspace](https://www.servicenow.com/docs/access?context=workspace-view-history-app-service&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)

