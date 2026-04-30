---
title: Set up the Continuous Integration and Continuous Delivery \(CICD\) spoke
description: Use basic authentication to authenticate CICD REST API calls on a ServiceNow instance.Create Credential records to the ServiceNow instance. The Continuous Integration and Continuous Delivery \(CICD\) spoke connection and credential alias uses these credentials to authorize actions.Create Connection records to your ServiceNow instance. The Continuous Integration and Continuous Delivery \(CICD\) spoke connection and credential alias uses these connections to perform actions on your ServiceNow instance.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Continuous Integration and Continuous Delivery \(CICD\) Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Continuous Integration and Continuous Delivery \(CICD\) spoke

Use basic authentication to authenticate CICD REST API calls on a ServiceNow instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Continuous Integration and Continuous Delivery \(CICD\) spoke.
-   Role required: admin or sn\_cicd.sys\_ci\_automation.

## Create Credential records for the Continuous Integration and Continuous Delivery \(CICD\) spoke

Create Credential records to the ServiceNow instance. The Continuous Integration and Continuous Delivery \(CICD\) spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **Basic Auth Credentials**.

    A blank Basic Auth Credentials form displays.

4.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record. For example, enter `CICD Credentials`.|
    |User name|The ServiceNow instance user name that authorizes and runs spoke actions and flows. This user must have either the admin or sn\_cicd.sys\_ci\_automation roles.|
    |Password|The password for the ServiceNow instance user.|
    |Active|Enable|
    |Order|Select the order to apply this credential. For example, enter `100`.|

5.  Click **Submit**.


## Create Connection records for the Continuous Integration and Continuous Delivery \(CICD\) spoke

Create Connection records to your ServiceNow instance. The Continuous Integration and Continuous Delivery \(CICD\) spoke connection and credential alias uses these connections to perform actions on your ServiceNow instance.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **CICD**.

3.  From the **Connections** tab, click **New**.

    The system displays a blank HTTP or HTTPS Connection form.

4.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the connection record. For example, enter `CICD Connection`.|
    |Credential|Select the Credential record you created for CICD. For example, select **CICD Credentials**.|
    |Connection URL|The URL of the ServiceNow instance on which the spoke runs actions and flows.|

5.  Click **Submit**.


