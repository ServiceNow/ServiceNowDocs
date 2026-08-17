---
title: Set up the MID Web Server with a .pem file
description: Install the .pem file into the MID unified keystore and set up the MID Web Server to enable configuring mTLS on your MID Web Server and agent.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/set-mid-web-server.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [MID Web Server and agent mTLS Authentication, Configure the MID Web Server extension, MID Web Server, Event Management setup, Configure, Event Management, ITOM AIOps, IT Operations Management]
---

# Set up the MID Web Server with a .pem file

Install the .pem file into the MID unified keystore and set up the MID Web Server to enable configuring mTLS on your MID Web Server and agent.

## Before you begin

Copy the `labmid/mid.pem` file \(created in the [Create keys and certificates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/create-keys-and-certificates.md) procedure\) to your MID Web Server host directory.

**Note:** This procedure includes commands for both CentOS 7/Linux and Windows Server environments. Select the commands relevant for your host operating system. If working with another Linux distribution, adapt the commands as needed for your specific OS.

Role required: agent\_client\_collector\_admin

## Procedure

1.  In a Linux environment:

    1.  Access the agent subdirectory under the MID Server's host directory.

    2.  Import the .pem file into the MID unified keystore.

        ```
        bin/scripts/manage-certificates.sh -a midwss /<path>/mid.pem;
        bin/scripts/manage-certificates.sh -l;
        ```

        Replace `<path>` with the directory where you copied the mid.pem file.

        The relevant part of the output is: `"defaultsecuritypairhandle,midwss"`

    3.  Validate your MID Server on the instance.

    4.  Select the MID Server on the instance and select **Setup ACC listener**.

        A new MID Web Server is created.

    5.  Navigate to the newly created MID Web Server record \(**ecc\_agent\_ext\_context\_webserver**\) on the instance.

    6.  Select the MID Web Server and set the Keystore certificate alias value to `midwss`.

    7.  Select **Save**.

    8.  Restart the MID Web Server.

2.  In a Windows environment:

    1.  Access the agent subdirectory under the MID Server's host directory.

    2.  Import the .pem file into the MID unified keystore.

        ```
        bin\scripts\manage-certificates.bat -a midwss <path>\mid.pem
        bin\scripts\manage-certificates.bat -l
        ```

        Replace `<path>` with the directory where you copied the mid.pem file.

        The relevant part of the output is: `"defaultsecuritypairhandle,midwss"`

    3.  Validate your MID Server on the instance.

    4.  Select the MID Server on the instance and select **Setup ACC listener**.

        A new MID Web Server is created.

    5.  Navigate to the newly created MID Web Server record \(**ecc\_agent\_ext\_context\_webserver**\) on the instance.

    6.  Select the MID Web Server and set the Keystore certificate alias value to `midwss`.

    7.  Select **Save**.

    8.  Restart the MID Web Server's Windows service using one of the following methods:

        -   Use the Services app on the Windows host.
        -   Use the command line with the MID Server's configured service name:

            ```
            net stop AgentClientCollector
            net start AgentClientCollector
            ```


## What to do next

[Connect the agent to the MID Web Server using TLS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/agent-mid-connect.md).

