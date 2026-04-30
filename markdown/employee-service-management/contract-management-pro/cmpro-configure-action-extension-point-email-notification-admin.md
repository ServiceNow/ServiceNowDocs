---
title: Configure extension point for notifications
description: Add or modify an Action and its functionality on the Standard ticket page for a contract request.
locale: en-US
release: xanadu
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Set up Contracts Core, Configure Contract Management Pro, Contract Management Pro, Employee Service Management]
---

# Configure extension point for notifications

Add or modify an Action and its functionality on the Standard ticket page for a contract request.

## Before you begin

Role required: Admin

-   Review the configuration of the script include, scripted extension points, and widgets.
-   For more information about using and customizing the script includes, see [Script includes](https://servicenow.com/docs/bundle/vancouver-application-development/page/script/server-scripting/concept/c_ScriptIncludes.html).
-   Ensure that you've set the application scope to this application.

## About this task

The base system `ApprovalNotificationWorkspaceURLExt` script provides the configuration of common actions for all request types. You can override these common actions for a specific request type or add more actions.

## Procedure

1.  Add or modify an action in the scripted extension point.

    1.  Navigate to **All** &gt; **System Extension Points** &gt; **Scripted Extension Points**.

    2.  Search and select the **ApprovalNotificationWorkspaceURLExt** extension point.

    3.  Add or modify an implementation for a practice area.

        To add a new implementation for a practice area, click the **Create implementation** related link.

        On the Script Include form, update the script as required.

        1.  To restrict this implementation to the practice area, add the following code to the **canHandle** parameter:

            ```java
             appliesTo(parentRecord) {
                    return <tablename of the parent record>;
                },
                /**
                 * @return {String} workspace to which the user can be navigated to view the contract request from notification
                 * The navigation URL is formed in runtime as '/now/' + (getWorkspaceURL return value/output)  + '/record/' + table '/' + sysID.
                 *
                 * For example:
                 * getWorkspaceURL output is  "legal/counsel-center"
                 * URL formed in runtime is '/now/legal/counsel-center/record/' + table + '/' + sysId
                 */
                getWorkspaceURL: function() {
                    return "legal/counsel-center";
             
                },
            ```

        2.  To add a new action, update the **process** method.

            For reference, see an existing **process** method of the `DefaultLegalTicketActions` script include or the implementation of another practice area.

    4.  Click **Update**.


## Result

To see a list of available default email notifications, go to **All** &gt; **System Notification** &gt; **Notifications** and search for the **Contracts Support** category.

**Parent Topic:**[Set up Contracts Core](../concept/cncore-setup-cmpro.md)

**Related topics**  


[Create a contract type](cncore-create-contract-type.md)

[Create document template categories](cncore-create-doc-tmplt-cat.md)

[Enable users to view email details in activity stream](cncore-enbl-user-email-astream.md)

[Activate a system property to generate a certificate of completion](cncore-config-system-prop-COC.md)

[Configure reminders for expiring contracts](cncore-config-rem-exp-cont.md)

[Configuring external applications for Contract Management Pro](../concept/cncore-set-ext-app-config.md)

[Use default email notifications](cmpro-send-receive-email-notification-admin.md)

[Auto-populate the start date and end date for contract requests](cncore-conf-start-end-date-for-cntrcts.md)

