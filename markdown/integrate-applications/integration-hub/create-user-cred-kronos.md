---
title: Provide Kronos user credentials
description: Create a record to provide details and credentials of the required Kronos user. The Kronos spoke uses these user credentials to perform actions in Kronos.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/create-user-cred-kronos.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure a connection, UKG Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Provide Kronos user credentials

Create a record to provide details and credentials of the required Kronos user. The Kronos spoke uses these user credentials to perform actions in Kronos.

## Before you begin

Role required: admin.

Verify that you provide credentials of a manager user or Kronos superuser. With these credentials, time off requests of both employee and manager can be managed.

## Procedure

1.  Navigate to **All** &gt; **Kronos** &gt; **Credentials**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Descriptions|
    |-----|------------|
    |Name|Name to uniquely identify the record.|
    |Application Key|Application Key of the Kronos user.|
    |User name|User name to log in to the user's account in Kronos.|
    |Password|Password of the Kronos user account.|
    |Connection &amp; Credential Alias|Default alias record associated with the Kronos spoke.|
    |Refresh Token Expires|Date and time by when the Kronos refresh token expires. The Kronos spoke generates a new refresh token periodically, before the current refresh token expires.|

4.  Select **Submit**.

5.  To generate the Kronos token, select the **Get Kronos Token** related link.


## Result

The Kronos - Get Kronos Token subflow is triggered. The subflow uses the details provided during spoke setup to retrieve a valid refresh token from Kronos. The subflow then updates the value of **Refresh Token Expires**.

**Note:** To access more details about the Kronos refressh token, navigate to **System OAuth** &gt; **Manage Tokens.**. Here, a record is created for each refresh token.

