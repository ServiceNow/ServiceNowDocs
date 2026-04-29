---
title: Onboard Split to DevOps Change Velocity — Classic
description: Create a Split tool record to connect and discover workspaces, environments, segments, and feature flags from the connected Split tool.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Split, Integrate, DevOps Change Velocity, IT Service Management]
---

# Onboard Split to DevOps Change Velocity — Classic

Create a Split tool record to connect and discover workspaces, environments, segments, and feature flags from the connected Split tool.

## Before you begin

Role required: sn\_devops.admin

## Procedure

1.  Create a tool record in DevOps to automatically connect to Split and get the webhook URL.

    1.  Navigate to **DevOps** &gt; **Tools** &gt; **Create New \(legacy\)** and create a record.

    2.  Enter a **Tool Name** and fill in the tool details.

<table id="table_brq_ccf_rjb"><tbody><tr><td>

Tool Integration

</td><td>

Split

</td></tr><tr><td>

Tool URL

</td><td>

Split tool URL.

 For example:

 `https://api.split.io`

</td></tr><tr><td>

Tool Username

</td><td>

Split username

</td></tr><tr><td>

Tool Password / Access Token

</td><td>

Split password or access token. For information on creating a Split token, see [Enable integration with ServiceNow DevOps in Split tool](enable-integration-servicenow-devops-split.md).

</td></tr></tbody>
</table>        **MID Server** is optional. Select MID Server for an on-premises tool that is attached to a MID Server. Application is automatically set to DevOps and capability is set to REST.

    3.  Select **Submit**.

        The tool is automatically **Connected Successfully** using a connection alias, and HTTP tool connection \(basic authentication credential\).

        **Note:** If you do not have global admin privileges for your tool \(to allow automatic configuration of the webhook URL\), you may need to have the tool admin user configure it for you \(cut and paste the webhook URL into the tool configuration\). Once the webhook is configured in the tool, **Enter Manual Configuration Mode** to connect to the tool manually, then exit.

2.  On successful tool creation, you're taken to the tool record page.
3.  If you want to control access to the tool, add the groups that must be given access to the tool in the **Maintained by** field on the **Access** tab.

    The tasks the users in the groups can perform depends on the roles assigned to them.

    -   DevOps Tool Owner role: Can view and edit the tool.
    -   DevOps App Owner role: Can view the tool and can associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects \(such as plans, repositories, and pipelines\).
    -   DevOps Administrator role: Can edit all tools.
    -   Other DevOps roles: Can view the tool.
    **Note:** Only groups containing users with DevOps roles are available for selection in the **Maintained by** field.

    The **All App Owners can view and associate tool objects to applications** option becomes available for selection if you choose to restrict access to the tool. This option enables all users having the DevOps App Owner role to access the tool. If selected, they’ll be able to view, associate, discover, import historical data, and modify pipeline steps \(if applicable\) of the tool's objects.

4.  Discover workspaces, environments, segments, and feature flags from the connected Split tool by selecting **Discover**.![Discover workspaces, environments, segments, feature flags from Split](../image/split-discover.png)

5.  Automatically configure the webhook URL in Split tool by selecting **Configure**.

    ServiceNow Integration will be activated on Split. Webhooks are auto-configured and notifications are sent from Split tool to DevOps.![Split connection configured in ServiceNow DevOps](../image/split-configure.png)


## Example

The following example specifies how changes made in the Split tool are notified to ServiceNow DevOps through the webhook.

-   Inbound events are created in ServiceNow for status \(Requested, Approved, Rejected or Withdrawn\) of the event.![Inbound events for Split created in ServiceNow](../image/split-inbound-event.png)
-   Feature Flag requests \(**DevOps &gt; Feature Flag &gt; Feature Flag Requests**\) are created or updated based on the status.![Feature flag requests for Split created in ServiceNow](../image/split-feature-flag-requests.png)
-   A change request is created for every Feature Flag request, and work notes on the change request is updated with basic change details on the feature flag.![Change request created for feature flag request](../image/split-change-request.png)

**Parent Topic:**[Split.io integration with DevOps Change Velocity](../concept/split-integration-devops-classic.md)

