---
title: Create a default profile
description: Create a connection profile that the ServiceNow CLI uses by default. You must create a default profile to set up the CLI's initial connection with an instance.
locale: en-US
release: zurich
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring and managing your ServiceNow CLI connection profiles, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Create a default profile

Create a connection profile that the ServiceNow CLI uses by default. You must create a default profile to set up the CLI's initial connection with an instance.

## Before you begin

Role required: none.

## About this task

By default, the information in this profile is used when you run a command that does not explicitly specify a profile to use.

**Note:** Sensitive credential information is only stored in the OS keychain, not in the configuration file.

## Procedure

1.  Open your system's command-line tool and execute this command.

    ```
    $ snc configure profile set
    ```

    The CLI prompts you for more information.

2.  Enter the requested values.

    When prompting for information, the CLI displays current values in brackets \[\]. To keep an existing value, press the Enter key.

    |Requested information|Description|
    |---------------------|-----------|
    |Host|The host name of the instance to connect to. Supports both the full URL \(https://my-instance.service-now.com\) or just the host name \(my-instance\).|
    |Login method|The login method to use to connect to the instance. Supports `Basic`, `OAuth`, and `OAuth + MFA`.|
    |Username|The user name to use to connect to the instance.|
    |Password|The password to use to connect to the instance.|
    |Client id|The client ID to use to connect to the instance when the login method is OAuth or OAuth + MFA.|
    |Client secret|The client secret to use to connect to the instance when the login method is OAuth or OAuth + MFA.|
    |Authentication code|The authentication code to use to connect to the instance when the login method is OAuth + MFA.|
    |Default output format|Specifies how to format the command results. Options are `json`, `yaml`, `text`, and `table`.|

    ```
    $ snc configure profile set
    
    Host: 
    https://myinstance.service-now.com
    
    Login Method (Basic, OAuth, OAuth + MFA): 
    Basic
    
    Username: 
    myusername
    
    Password: 
    mypassword
    ```

3.  Run any command using the values specified in your default profile by omitting the `--profile` attribute from your command.

    ```
    $ snc record create
    ```

    The command creates a record in the instance specified in the default profile with the specified connection options.


**Parent Topic:**[Configuring and managing your ServiceNow CLI connection profiles](configure-profile.md)

