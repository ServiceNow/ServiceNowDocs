---
title: Configuring and managing your ServiceNow CLI connection profiles
description: Create a connection profile to connect with your instance, view connection profiles, refresh your connection and available commands, or delete profiles you no longer need.
locale: en-US
release: zurich
product: ServiceNow CLI
classification: servicenow-cli
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ServiceNow CLI, Building low-code applications, Developing your application, Building applications]
---

# Configuring and managing your ServiceNow CLI connection profiles

Create a connection profile to connect with your instance, view connection profiles, refresh your connection and available commands, or delete profiles you no longer need.

The ServiceNow CLI stores profile information in a `config.json` file which, by default, is stored in your home directory at the following path:

-   Linux and Mac: `~/.snc/config.json`
-   Windows: `%USERPROFILE%\.snc\config.json`

The CLI uses this file to determine what information to use to connect to an instance, and what settings to use to generate output. By default, the ServiceNow CLI uses the settings found in the default profile to connect to an instance. To use alternate settings, you can create and reference additional named profiles. For more information, see [Configuring and managing your ServiceNow CLI connection profiles](configure-profile.md).

The following example shows a  configuration  file with a default profile and a named profile. Each profile can use different credentials and specify different hosts and output formats.

```
{
   "profiles":{
      "default":{
         "host":"https://myinstance.service-now.com",
         "loginmethod":"basic",
         "username":"admin",
         "output":"json",  
         "hostversion":"Paris",
         "appversion":"1.0"
         },
      "user1":{
         "host":"https://otherinstance.service-now.com",
         "loginmethod":"basic",
         "username":"user1",
         "output":"yaml",
         "hostversion":"Paris",
         "appversion":"1.0"
         }
      }
}
```

-   **[Create a default profile](create-default-profile.md)**  
Create a connection profile that the ServiceNow CLI uses by default. You must create a default profile to set up the CLI's initial connection with an instance.
-   **[Create a named profile](create-named-profile.md)**  
Create a named connection profile to use with specific commands. This allows you to specify a different instance or connection protocol for a specific command.
-   **[View profiles](list-all-profiles.md)**  
View all connection profiles set in the configuration file, or view information about a specific profile.
-   **[Remove a profile](delete-profile.md)**  
Remove a named connection profile that you no longer need from the configuration file.
-   **[Refresh your connection](refresh-profile.md)**  
Update the available commands from the instance for the given profile. Refresh your connection after modifying any of the commands on the corresponding instance in order to keep the CLI up-to-date.

**Parent Topic:**[ServiceNow CLI](../concept/servicenow-cli.md)

