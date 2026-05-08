---
title: Managing external event sources
description: Create and manage external event sources for a spoke or a scoped application that listen to events occurring in an application outside ServiceNow. Then, you can create external trigger definitions and associate them with the external event sources. When the event that you specify in the external trigger definition occurs, it starts one or more flows on your ServiceNow instance. Create an external event source for a spoke or scoped application that listens to events occurring in an application or system outside ServiceNow. Based on the external event source, you can create an external trigger definition that receives communication from the external event source and starts a flow on your ServiceNow instance.Update an external event source that is in the draft or published state.Delete an external event source in the draft or published state that is not associated with an external trigger definition.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
---

# Managing external event sources

Create and manage external event sources for a spoke or a scoped application that listen to events occurring in an application outside ServiceNow. Then, you can create external trigger definitions and associate them with the external event sources. When the event that you specify in the external trigger definition occurs, it starts one or more flows on your ServiceNow instance.

## Before you begin

Role required: trigger\_designer \(Can create, read, update, or delete external event sources\) and trigger\_designer\_read \(can perform read-only operations on the external event sources that the trigger\_designer role creates.\)

Confirm that you have installed the External Trigger Builder plugin on your instance. External Trigger Builder v1.0.3 is the latest available version.

## About this task

An external event source is an end point on your ServiceNow instance which listens to a system or application outside of ServiceNow. After the application outside ServiceNow sends an event to the external event source, it enables a trigger definition to start one or more flows. For example, you define an external event source for an issue-tracking software that communicates with an external trigger definition that you have defined. The external trigger definition listens to the event source and starts a flow when a new issue is created in the issue-tracking software. Both the external event source and the trigger definitions are defined on your ServiceNow instance. An external trigger definition gives a set of conditions that tells your ServiceNow instance when to start a flow.

**Parent Topic:**[Create a saved external trigger](create-saved-external-trigger.md)

## Create an external event source

Create an external event source for a spoke or scoped application that listens to events occurring in an application or system outside ServiceNow. Based on the external event source, you can create an external trigger definition that receives communication from the external event source and starts a flow on your ServiceNow instance.

### Before you begin

Role required: trigger\_designer \(Can create, read, update, or delete external event sources\) and trigger\_designer\_read \(can perform read-only operations on the external event sources that the trigger\_designer role creates.\)

Confirm that you have installed the External Trigger Builder plugin on your instance.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Click the spoke.

    The **Spokes** tab is selected by default. If it isn’t selected already, confirm that you have selected it.

    ![Spoke selection for external event source creation.](../images/external-event-src-select-spoke.png)

4.  On the left panel, click Event sources.

    ![Event sources menu.](../images/external-event-source-event-src-menu.png)

5.  Click **Create event source**.

6.  In the Event Source name field, provide a unique name to the external event source.

7.  In the Description field, enter a description of the external event source.

    ![Create external event source screen.](../images/external-event-source-create-external-event-src-scrn.png)

8.  Click **Create event source**.

    The external event source is created in the draft state.

9.  View the external event source in the draft state.

    1.  Select the spoke tab.

        ![Spoke tab is clicked.](../images/external-event-src-view-draft.png)

    2.  Select the **Drafts** tab.

        The external event source that you created, appears.

        **Tip:** If the external event source doesn't appear, refresh the page, and then select the **Drafts** tab.

10. Under the Authentication heading, select the method to authenticate the webhook that the external application sends to your ServiceNow instance.

    The following authentication methods are available.

    -   Basic
    -   OAuth
    -   Hash
    -   Token
    If you choose the Hash or Token authentication method, then you must specify the information given in the table.

<table id="table_yy3_vmr_gfc"><thead><tr><th>

Authentication method

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Basic

</td><td>

 

</td><td>

Option to specify that user names and passwords that the external application sends will be authenticated.

</td></tr><tr><td>

OAuth

</td><td>

 

</td><td>

Option to specify that OAuth mechanism will be used to authenticate the webhooks from the external application.

</td></tr><tr><td rowspan="5">

Hash

</td><td>

Authentication Location

</td><td>

Option to specify the location where the external application or system includes the hash when sending the message. The available locations are:-   Query parameters
-   Header


</td></tr><tr><td>

Parameter Name

</td><td>

Option to specify the name of the field where you can find the hash.

</td></tr><tr><td>

Hash algorithm

</td><td>

Option to specify the algorithm using which the hash is calculated. The available algorithms are:-   HmacSHA256
-   HmacSHA384
-   HmacSHA512


</td></tr><tr><td>

Prefix

</td><td>

Option to specify a value that may come before the hash.

</td></tr><tr><td>

HMAC Util Script

</td><td>

Option to specify the script that generates or validates the hash.To know more about HMAC, see Configure HMAC - Token-based authentication.

</td></tr><tr><td rowspan="3">

Token

</td><td>

Authentication Location

</td><td>

Option to specify the location where the external system includes the token when sending the message. The available locations are:-   Query parameters
-   Header


</td></tr><tr><td>

Parameter Name

</td><td>

Option to specify the name of the field where you can find the token.

</td></tr><tr><td>

Prefix

</td><td>

Option to specify a value that may come before the token.

</td></tr></tbody>
</table>11. Click **Publish**.

    The external event source is available for you to associate with an external trigger definition.

    ![External event source published.](../images/external-event-src-published.png)

12. View the published external event source.

    1.  Select the spoke tab.

        ![Spoke tab selected.](../images/external-event-src-view-pub-event.png)

    2.  Select the **Published** tab.

    The external event source that you published, appears.

    **Tip:** If the external event source doesn't appear, refresh the page and select the **Drafts** tab.


### What to do next

[Create a saved external trigger](create-saved-external-trigger.md) and associate it with the external event source that you created.

## Update an external event source

Update an external event source that is in the draft or published state.

### Before you begin

Role required: trigger\_designer \(Can create, read, update, or delete external event sources\) and trigger\_designer\_read \(can perform read-only operations on the external event sources that the trigger\_designer role creates.\)

Confirm that you have installed the External Trigger Builder plugin on your instance.

### About this task

You can update all information of an external event source in the draft state but only its name and description in the published state.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Click the spoke that has the external event source defined.

    The **Spokes** tab is selected by default. If it isn’t selected, confirm that you have selected it.

    ![Spoke selection for external event source creation.](../images/external-event-src-select-spoke.png)

4.  On the left panel, click Event sources.

    ![Event sources menu.](../images/external-event-source-event-src-menu.png)

5.  To update an event source in the draft state, do the steps.

    1.  Click the **Drafts** tab.

    2.  Click the external event source that you want to update.

    3.  Click the ellipsis button \(![Ellipsis icon to update external event source.](../images/external-event-src-ellipsis-icon.png)\) and then click Properties.

    4.  In the Event source properties form, update the information.

    5.  Click **Update**.

        The external event source is updated.

6.  To update an event source in the published state, do the steps.

    1.  Click the **Published** tab.

    2.  Click the external event source that you want to update.

    3.  Click the ellipsis button \(![Ellipsis icon to update external event source.](../images/external-event-src-ellipsis-icon.png)\) and then click Properties.

    4.  In the Event source properties form, update the information in the following fields.

        -   Event source name
        -   Description
    5.  Click **Update**.

        The external event source is updated.


## Delete an external event source

Delete an external event source in the draft or published state that is not associated with an external trigger definition.

### Before you begin

Role required: trigger\_designer \(Can create, read, update, or delete external event sources\) and trigger\_designer\_read \(can perform read-only operations on the external event sources that the trigger\_designer role creates.\)

Confirm that you have installed the External Trigger Builder plugin on your instance.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Click the spoke that has the external event source defined.

    The **Spokes** tab is selected by default. If it isn’t selected, confirm that you have selected it.

    ![Spoke selection for external event source creation.](../images/external-event-src-select-spoke.png)

4.  On the left panel, click Event sources.

    ![Event sources menu.](../images/external-event-source-event-src-menu.png)

5.  Click the **Published** or **Drafts** tab.

6.  Click the external event source that you want to delete.

7.  Click the ellipsis button \(![Ellipsis icon to update external event source.](../images/external-event-src-ellipsis-icon.png)\) and then select Properties.

8.  Click **Delete**.

9.  On the Delete event source dialog, click **Delete**.

    The external event source is deleted.

    **Note:** You can't delete an external event source that has one or more external triggers associated.


