---
title: Install the ADAM configuration file
description: Install the ADAM configuration file through the Windows command line.
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Use ADAMSync to populate ADAM, Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Install the ADAM configuration file

Install the ADAM configuration file through the Windows command line.

## Before you begin

Role required: admin

## Procedure

1.  Install the configuration file.

    ```
     C:\WINDOWS\adam>adamsync /install localhost:50000 MS-AdamSyncConf-SNC.XML
    ```

2.  Run the synchronization file to log to the console.

    ```
     C:\WINDOWS\adam>adamsync /sync localhost:50000 "ou=users,dc=service-now,dc=adam" /log -
    ```

3.  Review the results by using the ADSIEdit console.

    You should see the new objects and attributes that were created by ADAMSync.

4.  Run ldap to test the UserProxy authentication.

    Automating the sync process

    Set up the sync process as a Windows Scheduled Task. You must either provide the credentials in the config file, command line, or run the Scheduled Task with an account that has access.

    Special notes

    -   You can create multiple configuration files and scheduled jobs to sync ADAM from multiple sources.

        This example imports the sAMAccountName attribute which can be used as the application logon. If you are going to sync source you need to make sure you have a unique attribute value that can be used for the logon credentials. sAMAccountName is guaranteed to be unique within a domain, but not across multiple domains.

    -   If you are using Microsoft Exchange, we recommend excluding cn=SystemMailbox\* objects as part of the object-filter configuration.

