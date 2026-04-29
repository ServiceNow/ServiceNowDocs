---
title: Create a named profile
description: Create a named connection profile to use with specific commands. This allows you to specify a different instance or connection protocol for a specific command.
locale: en-US
release: australia
product: ServiceNow CLI
classification: servicenow-cli
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring and managing your ServiceNow CLI connection profiles, ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Create a named profile

Create a named connection profile to use with specific commands. This allows you to specify a different instance or connection protocol for a specific command.

## Before you begin

A default profile must first exist to communicate with an instance.

Role required: none.

## About this task

**Note:** Sensitive credential information is only stored in the OS keychain, not in the configuration file.

## Procedure

1.  Open your system's command-line tool and execute this command.

2.  Specify the name of the named profile in the *profile-name* argument.

    ```
    $ snc configure profile set [--profile profile-name]
    ```

    The CLI prompts you for more information.

3.  Enter the requested values.

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
    $ snc configure profile set --profile user1
    
    Host: 
    https://mytestinstance.service-now.com
    
    Login Method (Basic ,OAuth ,OAuth + MFA): 
    Basic
    
    Username: 
    myusername
    
    Password: 
    mypassword
    ```

4.  Run any command using the values specified in your named profile by adding the  `--profile  <profile-name>` attribute to your command.

    ```
    $ snc record create --profile user1
    ```

    The command creates a record in the instance specified in the `user1` profile with the specified connection options.


**Parent Topic:**[Configuring and managing your ServiceNow CLI connection profiles](configure-profile.md)

