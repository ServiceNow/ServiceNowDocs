---
title: Standard Ticket page for Universal Request
description: The Universal Request standard ticket page enables requesters to view the details of their universal requests from the Service Portal.
locale: en-US
release: xanadu
product: Universal Request for HR Service Delivery
classification: universal-request-for-hr-service-delivery
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Configuring Universal Request, Setting up and configuring Universal Request, Universal Request, Employee Service Management]
---

# Standard Ticket page for Universal Request

The Universal Request standard ticket page enables requesters to view the details of their universal requests from the Service Portal.

A requester can view the aggregated and simplified view of the UR activity and all activities from one or more child department tickets \(primary tickets\). Using the UR standard ticket page has the following advantages:

-   A ticket reference number \(UR number\) that is always consistent for the requester, even when the request is transferred between various departments.
-   The UR state details that is derived from the mapping between the UR states and the states of the primary ticket associated with UR. With this state mapping enabled, the requester sees only the UR state.
-   An activity stream that shows a logical and sequential record of comments to and from any fulfiller who worked on the UR or its primary tickets.
-   An info region that displays department-specific fields of the current primary ticket. For example, configure the page to show **Opened For** and **Subject Person** fields from a child HR case, or to show **Caller** and **Urgency** fields from a child IT incident.

![Consistent page views in the standard ticket page.](../images/ur-std-tkt-similarview.png)

The Standard ticket page configuration for UR tickets enables you to determine what you want to display as a view. By default, a Universal Request Standard Ticket configuration is available that you can use and customize. Information displayed in different sections of a standard ticket page depends on the individual request type.

**Note:** If you are upgrading from a previous release and want to use the Standard Ticket page for your department, ensure that you enable the **Page Route map** in Service Portal. For more information, see [Enable the page route map for standard ticket page](https://www.servicenow.com/docs/access?context=config-pageroutemap-stpage&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

![Universal Request standard ticket page](../images/ur-std-ticket-page.png)

<table id="table_cv4_kmd_gdb"><thead><tr><th>

SI \#

</th><th>

UI Component

</th><th>

Information displayed

</th></tr></thead><tbody><tr><td>

1

</td><td>

Header section

</td><td>

Displays the information submitted for the Universal Request record, such as the UR request number, created and updated details of the request, and the current status. This section is not a configurable section. **Updated** field displays the details of the last activity time of the primary ticket if it exists. If there is no primary ticket attached, the **Updated** field displays the last activity time of the Universal Request.

</td></tr><tr><td>

2

</td><td>

Number

</td><td>

Displays the unique UR number that identifies the request.

</td></tr><tr><td>

3

</td><td>

State

</td><td>

Shows the state of the Universal Request.

</td></tr><tr><td>

4

</td><td>

Short Description

</td><td>

Always displays the short description of the Universal Request submitted.

</td></tr><tr><td>

5

</td><td>

Actions region

</td><td>

Actions that are configured as part of the primary ticket page. If the primary ticket does not exist, then the default actions of the Universal Request are displayed.The default UR actions are:

-   **Accept/Reject resolution**: To review the resolution provided and choose to either accept or reject the resolution.
-   **Close**: To cancel the UR if the UR is no longer required.

**Note:** An UR can be canceled only if there are no active or closed primary tickets attached to it. Also, the state of UR must be either **New** or **In Progress**.


</td></tr><tr><td>

6

</td><td>

Info region

</td><td>

Configurable fields that are part of the primary ticket. If the primary ticket does not exist, then the default fields configured for Universal Request are displayed.

</td></tr><tr><td>

7

</td><td>

Tabs section

</td><td>

Tabs that are configured as part of the primary ticket page. If the primary ticket does not exist, then the default tabs, such as the **Activity** and **Attachments** are displayed.

</td></tr><tr><td>

9

</td><td>

Activity stream

</td><td>

Displays the activity and attachments from UR, and all the previously associated primary tickets in a sequential order.

</td></tr></tbody>
</table>When a routing agent chooses not to share additional comments or attachments while routing, a system-generated message displays in the header and activity stream. However, the requester can view all comments in the activity stream.

![Message displayed when the additional comments and attachments is not shared](../images/ur-hidden-info.png)

When a user clicks to view the Standard Ticket page from a department ticket that was previously a primary ticket of the UR, then the Standard Ticket configuration validates and displays a message asking the user to open the latest page that displays only the activity streams and attachments. The following image displays the message containing a link to open the latest activity stream.

![Message containing a link to open the latest page.](../images/ur-std-tkt-stalemsg.png)

-   **[Configure Standard Ticket page for Universal Request](../task/config-standard-ticket.md)**  
Use the Standard ticket page configuration for Universal Request to provide a consistent layout across all tickets raised and associated.

**Parent Topic:**[Configuring Universal Request](configure-ur.md)

**Related topics**  


[Configure Standard Ticket page for Universal Request](../task/config-standard-ticket.md)

