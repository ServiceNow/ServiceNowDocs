---
title: Install the .pem file in the MID unified keystore and set up the MID Web Server
description: Install the .pem file into the MID unified keystore and set up the MID Web Server to enable configuring mTLS on your MID Web Server and agent.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [MID Web Server and agent mTLS Authentication, Configure the MID Web Server extension, MID Web Server, Event Management setup, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Install the .pem file in the MID unified keystore and set up the MID Web Server

Install the .pem file into the MID unified keystore and set up the MID Web Server to enable configuring mTLS on your MID Web Server and agent.

## Before you begin

Copy the `labmid/mid.pem` file \(created in the [Create keys and certificates](create-keys-and-certificates.md) procedure\) to your MID Web Server host directory.

Role required: agent\_client\_collector\_admin

## Procedure

1.  Access the `agent` subdirectory under the MID Server's host directory.

2.  Run the following commands:

    ```
    bin/scripts/manage-certificates.sh -a midwss /<path>/mid.pem; 
    bin/scripts/manage-certificates.sh -l;
    ```

    The relevant part of the output is, `"defaultsecuritypairhandle,midwss”`

3.  Validate your MID Server on the instance.

4.  Select the MID Server on the instance and select **Setup ACC listener**.

    A new MID Web Server is created.

5.  Navigate to the newly created MID Web Server record \(**ecc\_agent\_ext\_context\_webserver**\) on the instance.

6.  On the instance, select the MID Web Server and set the **Keystore certificate alias** value to **midwss**.

7.  Select **Save**.

8.  Restart the MID Web Server.


## What to do next

[Connect the agent to the MID Web Server using TLS](agent-mid-connect.md).

**Parent Topic:**[MID Web Server and agent mTLS Authentication](../../event-management/concept/mid-web-server-mTLS-authentication.md)

