---
title: Configure a sentiment connector
description: Specify the service URL and other configuration information for third party APIs that are used for sentiment analysis.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Sentiment analysis for surveys, Survey administration, Using surveys, Surveys, Assessments and Surveys, Exploring Service Administration, Service Administration, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure a sentiment connector

Specify the service URL and other configuration information for third party APIs that are used for sentiment analysis.

## Before you begin

Role required: admin

## Procedure

1.  Change the scope of the current session to **Sentiment Analysis**.

2.  Navigate to **Sentiment Analysis** &gt; **Sentiment Connector Configurations**.

3.  Add or edit the connector configuration for a third party vendor such as Google, IBMWatson, and MSAzure.

    **Note:** By default, placeholders are available for configuring connectors for Google, IBMWatson, and MSAzure.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the sentiment analysis connector configuration.|
    |Active|Check box to activate the connector configuration.|
    |Credential Alias|Credential alias associated with the connector configuration. It has a reference to the system level table \(sys\_alias\_list\).|
    |Default|Check box to make this as the default connector configuration.|
    |Description|Description of the connector configuration.|
    |Script|Script to call the Sentiment Analysis API and the normalize the values.|

4.  Configure the connector credentials

    1.  Open the record referred in the **Credential Alias** field.

    2.  Under the **Connections** tab, select the connection.

    3.  In the **Connection URL** field, enter the value.

    4.  Open the record referred in the **Credentials** field.

    5.  Enter the credential information.

        **Note:**

        -   You should obtain the connection credentials from the respective third-party vendors.
        -   If the credential is an API key, specify its value. If the credential is basic authentication, that is, user name and password, specify the corresponding information.
    6.  Select the **Active** check box and click **Update**.

5.  Select the **Active** check box for the connector configuration and click **Update**.


**Parent Topic:**[Sentiment analysis for surveys](../concept/sentiment-analysis.md)

