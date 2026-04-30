---
title: Set up the First Advantage spoke
description: Integrate the ServiceNow instance with your First Advantage account using an API key to authenticate ServiceNow requests.Create a connection record to integrate your ServiceNow instance and the First Advantage server. Your ServiceNow instance uses this connection record to perform the First Advantage spoke actions.Create First Advantage states to be displayed in the State list in your ServiceNow instance.Create the Draft, Ready, and In Progress states in the Task \[task\] table.Create the Complete and Cancelled states in the First Advantage Task \[sn\_fadv\_spoke\_first\_advantage\_task\] table.Create the Complete - Success and Complete - Deal Broken states in the First Advantage Employee Task \[sn\_fadv\_spoke\_first\_advantage\_employee\_task\_table\] table.Receive invite and order event updates at your ServiceNow instance by setting up the webhooks.Create a authorization key to authorise requests from Jenkins.Set up the First Advantage webhook by providing key for the First Advantage webhook client.Access the API endpoint for the invite and order events and share the required details with First Advantage to set up the webhooks.Store the details of the First Advantage accounts and packages by synchronizing First Advantage accounts and packages with ServiceNow.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [First Advantage Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the First Advantage spoke

Integrate the ServiceNow instance with your First Advantage account using an API key to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the First Advantage spoke.
-   Role required: admin.

## Create Connection record for the First Advantage spoke

Create a connection record to integrate your ServiceNow instance and the First Advantage server. Your ServiceNow instance uses this connection record to perform the First Advantage spoke actions.

### Before you begin

Role required: admin.

Acquire the API key from the First Advantage server.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Select **Integrations**.

3.  Select the **Connections** tab.

4.  In the Search all connections field, enter `First Advantage`.

    Confirm that the **Outbound** tab is selected.

5.  On the FirstAdvantage tile, select **View Details**.

    ![View Details button on FirstAdvantage alias tile.](../image/first-adv-view-details.png)

6.  Select **Configure**.

7.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the connection. The default and read-only name of the first record is the same as that of the connection alias. You can provide a different name when you create a connection record by clicking **Add Connection**.|
    |Connection URL|Option to provide the connection URL to the First Advantage server. The URL is [https://rest-ua.fadv.com](https://rest-ua.fadv.com).|
    |Distribution Email|Option to provide a distribution email ID.|
    |Version|Option to provide the version of the API.|
    |API Key|Option to enter the API key that the First Advantage server uses to authenticate access requests.|

    ![First Advantage connection form.](../image/first-adv-conn-form.png)

8.  Select **Configure Connection**.

    The connection record is configured.


## Create First Advantage states in your ServiceNow instance

Create First Advantage states to be displayed in the **State** list in your ServiceNow instance.

### Before you begin

Role required: admin

### Create the Draft, Ready, and In Progress states

Create the Draft, Ready, and In Progress states in the Task \[task\] table.

#### Before you begin

Role required: admin.

#### Procedure

1.  In the Filter navigator, enter `sys_choice.list`.

    The records in the Choice \[sys\_choice\] table are displayed.

2.  Click **New**.

3.  On the form, fill these values and create three records for the Draft state.

    |Field|Value|
    |-----|-----|
    |Table|Task \[task\]|
    |Element|state|
    |Label|Draft|
    |Value|137|

    **Note:**

    -   Ensure that you provide the exact numbers in the **Value** field as mentioned here. The spoke flows will not be triggered if there is any change in these numbers.
    -   Ensure that the record is created in the **Global** application.
4.  Click **Submit**.

5.  Similarly, create records for the Ready and In Progress states.

    |Field|Value|
    |-----|-----|
    |Table|Task \[task\]|
    |Element|state|
    |Label|Ready|
    |Value|173|

    |Field|Value|
    |-----|-----|
    |Table|Task \[task\]|
    |Element|state|
    |Label|In Progress|
    |Value|181|

    **Note:**

    -   Ensure that you provide the exact numbers in the **Value** field as mentioned here. The spoke flows will not be triggered if there is any change in these numbers.
    -   Ensure that the record is created in the **Global** application.

#### Result

The Draft, Ready, and In Progress states are created in the Task \[task\] table

### Create the Complete and Cancelled states

Create the Complete and Cancelled states in the First Advantage Task \[sn\_fadv\_spoke\_first\_advantage\_task\] table.

#### Before you begin

Role required: admin.

#### Procedure

1.  Navigate to **All** &gt; **First Advantage Spoke** &gt; **Order Tasks**.

2.  Click **New**.

    **Note:** Ensure that the record is created in the **First Advantage** application.

3.  Right-click **State** and click **Configure Choices**.

4.  Perform these steps to create the Cancelled state:

    1.  Enter `Cancelled` in **New item text**.

    2.  Enter `149` in **Numeric value**.

        **Note:** Ensure that you provide the exact numbers in the **Numeric value** field as mentioned here. The spoke flows will not be triggered if there is any change in these numbers.

    3.  Click **Add**.

    4.  Click **Save**.

5.  Perform these steps to create the Complete state:

    1.  Enter `Complete` in **New item text**.

    2.  Enter `127` in **Numeric value**.

        **Note:** Ensure that you provide the exact numbers in the **Numeric value** field as mentioned here. The spoke flows will not be triggered if there is any change in these numbers.

    3.  Click **Add**.

    4.  Click **Save**.


#### Result

The Complete and Cancelled states are created in the First Advantage Task \[sn\_fadv\_spoke\_first\_advantage\_task\] table.

### Create the Complete - Success and Complete - Deal Broken states

Create the Complete - Success and Complete - Deal Broken states in the First Advantage Employee Task \[sn\_fadv\_spoke\_first\_advantage\_employee\_task\_table\] table.

#### Before you begin

Role required: admin.

#### Procedure

1.  Navigate to **All** &gt; **First Advantage Spoke** &gt; **Employee Task**.

2.  Click **New**.

    **Note:** Ensure that the record is created in the **First Advantage** application.

3.  Right-click **State** and click **Configure Choices**.

4.  Perform these steps to create the Cancelled state:

    1.  Enter `Complete - Success` in **New item text**.

    2.  Enter `161` in **Numeric value**.

        **Note:** Ensure that you provide the exact numbers in the **Numeric value** field as mentioned here. The spoke flows will not be triggered if there is any change in these numbers.

    3.  Click **Add**.

    4.  Click **Save**.

5.  Perform these steps to create the Complete state:

    1.  Enter `Complete - Deal Broken` in **New item text**.

    2.  Enter `117` in **Numeric value**.

        **Note:** Ensure that you provide the exact numbers in the **Numeric value** field as mentioned here. The spoke flows will not be triggered if there is any change in these numbers.

    3.  Click **Add**.

    4.  Click **Save**.


#### Result

The Complete - Success and Complete - Deal Broken states are created in the First Advantage Employee Task \[sn\_fadv\_spoke\_first\_advantage\_employee\_task\_table\] table.

## Set up First Advantage webhooks

Receive invite and order event updates at your ServiceNow instance by setting up the webhooks.

### Before you begin

Role required: admin

### Create authorization key for the First Advantage spoke

Create a authorization key to authorise requests from Jenkins.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scripts - Background**.

2.  Enter this command in the **Run script \(JavaScript executed on server\)** text field:

    `gs.info(GlideSecureRandomUtil.getSecureRandomString(32));`

3.  Click **Run Script**.

4.  Copy and record the generated value for later use.

    ![Client Secret or Authorization Key](../image/auth-token.png)


### Provide key in your ServiceNow instance

Set up the First Advantage webhook by providing key for the First Advantage webhook client.

#### Before you begin

-   [Create authorization key for the First Advantage spoke](setup-first-adv.md#) and record the value.
-   Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **First Advantage Spoke** &gt; **FADV Webhook Client Details**.

2.  Click **New**.

3.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record.|
    |Authorization Key|Authorization key you had generated. For more information, see [Create authorization key for the First Advantage spoke](setup-first-adv.md#).|

4.  Click **Submit**.


### Access API endpoints

Access the API endpoint for the invite and order events and share the required details with First Advantage to set up the webhooks.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Scripted REST APIs**.

2.  Open the record for the First Advantage spoke, for example, **First Advantage Webhook**.

3.  In the **Resources** tab:

    1.  Open the record for the invite event, for example, **Invite Status**.

    2.  Copy and record the path provided in **Resource path**, for example, `/api/sn_fadv_spoke/fadv/invite_status`.

    3.  Open the record for the order event, for example, **Order Status**.

    4.  Copy and record the path provided in **Resource path**, for example, `/api/sn_fadv_spoke/fadv/order_status`.


#### What to do next

Contact First Advantage to setup webhooks for your ServiceNow instance. For this, share these details with First Advantage:

-   Custom header in this format: `fadvKey <authorization-key>`.

    **Note:**

    -   Ensure that the custom header is in this format only. The spoke flows will not be triggered if there is any change.
    -   Provide the same key you had earlier provided in **First Advantage Spoke** &gt; **FADV Webhook Client Details**.
    -   Use the same case as mentioned here: `fadvKey`.
-   API endpoint for the invite events in this format: `<ServiceNow-instance-URL>/api/sn_fadv_spoke/fadv/invite_status`
-   API endpoint for the order events in this format: `<ServiceNow-instance-URL>/api/sn_fadv_spoke/fadv/order_status`

## Synchronise First Advantage accounts and packages with ServiceNow

Store the details of the First Advantage accounts and packages by synchronizing First Advantage accounts and packages with ServiceNow.

### Before you begin

Role required: First Advantage admin

### Procedure

1.  Navigate to **All** &gt; **First Advantage Spoke** &gt; **Accounts**.

2.  Click **New**.

3.  On the form, fill in the values.

    |Field|Description|
    |-----|-----------|
    |Primary Account|Option to specify that the account is a primary account. Select the check box.|
    |Account ID|ID of the primary account.|
    |Account Name|Name of the primary account.|

4.  Click **Submit**.

    The primary account is created and the record is displayed.

5.  Navigate to **First Advantage Spoke** &gt; **Accounts**.

6.  Click the **Get Accounts** related list.

7.  Navigate to **First Advantage Spoke** &gt; **Packages**.

8.  Click the **Get Packages** related link.


### Result

The First Advantage account and package details are retrieved.

**Note:** Only users with the FADV admin role can synchronize the account and package details. Users with FADV user role can only view the retrieved details.

