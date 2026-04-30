---
title: Configure an Action for legal services on the Standard ticket page
description: Add or modify an Action and its functionality on the Standard ticket page for a legal request.
locale: en-US
release: xanadu
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Setting up Legal Request Management, Legal Request Management, Legal Service Delivery, Employee Service Management]
---

# Configure an Action for legal services on the Standard ticket page

Add or modify an Action and its functionality on the Standard ticket page for a legal request.

## Before you begin

-   Review the configuration of the script include, scripted extension points and service portal widgets for legal services installed with the Legal Service Delivery apps.
-   The Actions is one of the sections of a standard ticket page of the Service Portal, so get familiar with the [Standard ticket page](https://www.servicenow.com/docs/access?context=standard-ticket-page&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) and [Service Portal](https://www.servicenow.com/docs/access?context=c_ServicePortal&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).
-   For more information about configuring service portal widgets, see [Service Portal widgets](https://www.servicenow.com/docs/access?context=service-portal-widgets&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).
-   For more information about using and customizing the script includes, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).
-   Ensure that you've set the application scope to Legal Request Management.

Role required: admin

## About this task

The base system `DefaultLegalTicketActions` script provides the configuration of common actions for all legal request types. You can override these common actions for a specific legal request type or add more actions.

## Procedure

1.  Add or modify an action in the scripted extension point.

    1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

    2.  Search and select the **LegalTicketAction** extension point.

    3.  Add or modify an implementation for a practice area.

        -   To add a new implementation for a practice area, click the **Create implementation** related link.

            On the Script Include form, update the script as required.

            1.  To restrict this implementation to the practice area, add the following code to the **canHandle** parameter:

                ```java
                 canHandle: function(tableName) {
                        return tableName == '<TableName>'; //Replace TableName with a practice area table name
                    },
                ```

            2.  To add a new action, update the **process** method.

                For reference, see an existing **process** method of the `DefaultLegalTicketActions` script include or the implementation of another practice area.

        -   To modify an existing implementation, open a class from the Implementations related list.

            On the Script Include form, update the script as required.

            -   To modify an existing action, update the **name** parameter in the JSON object to match the one in the `DefaultLegalTicketActions` script.

                For example, to change the Cancel action's default behavior in a specific practice area, open its extension point implementation keep the **name** parameter as `cancel` while modifying other parameters in the JSON object as required.

            -   To add a new action, create a JSON object and change the name and other parameters as required.
    4.  Click **Update**.

2.  Configure Actions widgets on the standard ticket page for legal services.

    1.  Navigate to **All** &gt; **Service Portal** &gt; **Widgets**.

    2.  Search and select the **Legal Ticket Actions** widget.

    3.  Review the existing script and Angular ng-template for reference and then add or modify them as required.

    4.  Click **Update**.


**Parent Topic:**[Setting up Legal Request Management](../concept/legal-ops-administration.md)

