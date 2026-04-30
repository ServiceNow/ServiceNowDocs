---
title: Set up Jenkins spoke
description: Integrate the ServiceNow instance and Jenkins using basic authentication to authenticate ServiceNow requests.Create Credential records to the Jenkins server. The Jenkins spoke connection and credential alias uses these credentials to authorize actions.Create Connection records to your Jenkins account. The Jenkins spoke connection and credential alias uses these connections to perform actions on Jenkins.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Jenkins Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up Jenkins spoke

Integrate the ServiceNow instance and Jenkins using basic authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Jenkins spoke.
-   Role required: admin.

## Create Credential records for the Jenkins spoke

Create Credential records to the Jenkins server. The Jenkins spoke connection and credential alias uses these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **Basic Auth Credentials**.

    A blank Basic Auth Credentials form displays.

4.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record. For example, enter `Jenkins Credentials`.|
    |User name|Your Jenkins user name.|
    |Password|Your Jenkins password.|
    |Active|Enable|
    |Order|Select the order to apply this credential. For example, enter `100`.|

5.  Click **Submit**.


## Create Connection records for the Jenkins spoke

Create Connection records to your Jenkins account. The Jenkins spoke connection and credential alias uses these connections to perform actions on Jenkins.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **Jenkins**.

3.  From the **Connections** tab, click **New**.

    The system displays a blank HTTP\(s\) Connection form.

4.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the connection record. For example, enter `Jenkins Connection`.|
    |Credential|Select the Credential record you created for Jenkins. For example, select **Jenkins Credentials**.|
    |Connection URL|The URL of the host machine where Jenkins is installed.|

5.  Click **Submit**.


