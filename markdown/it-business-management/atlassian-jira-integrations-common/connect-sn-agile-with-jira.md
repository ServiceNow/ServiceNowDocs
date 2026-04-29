---
title: Connecting Agile Development 2.0 to Jira
description: Establish a connection between Agile Development 2.0 and Jira using a Jira connection alias and a Jira instance.Create a Basic Auth credential and an HTTP\(s\) connection with a Jira connection alias to establish a connection with Jira.Create a Jira instance record using the connection alias that you created to enable the setup of Jira integration with Agile Development 2.0.Connect Jira to Agile Development 2.0 to enable the integration.
locale: en-US
release: australia
product: Atlassian Jira Integrations Common
classification: atlassian-jira-integrations-common
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up the integration between Jira and Agile Development 2.0, Atlassian Jira Integration for Agile Development, Strategic Portfolio Management]
---

# Connecting Agile Development 2.0 to Jira

Establish a connection between Agile Development 2.0 and Jira using a Jira connection alias and a Jira instance.

When you connect Agile Development 2.0 to Jira, a webhook is registered in Jira which receives the following event updates between Jira and Agile Development 2.0.

-   Creating or updating projects.
-   Creating, updating, or deleting information of epic, story, sprint, and any custom table maps and their fields.

**Parent Topic:**[Setting up the integration between Jira and Agile Development 2.0](../task/setting-up-the-integration-between-jira-and-agile-development.md)

## Create a Jira connection alias for integration with Agile Development 2.0

Create a Basic Auth credential and an HTTP\(s\) connection with a Jira connection alias to establish a connection with Jira.

### Before you begin

Roles required:

-   admin to create a connection and credential alias
-   sn\_jira\_int.admin or sn\_jira\_int.user to create basic authorization credentials and HTTP\(s\) connection

### Procedure

1.  [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US)

    -   You can use the connection alias \(sn\_jira\_int.Jira\) that is available by default.
    -   You must create a connection alias for every Jira instance that you use.
    -   For Jira server \(on-prem\) users, ensure that the **server\_type** and **server\_version** connection attributes are present.
2.  Create [Basic authorization credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

    Ensure that the user for whom the basic authorization credentials are created has access to all Jira projects.

3.  [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=australia&pubname=australia-platform-security&ft:locale=en-US).


## Create a Jira Instance for integration with Agile Development 2.0

Create a Jira instance record using the connection alias that you created to enable the setup of Jira integration with Agile Development 2.0.

### Before you begin

Role required: sn\_jira\_int.admin or sn\_jira\_int.user

### Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Jira Instances**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the Jira instance. Enter a name of your choice.|
    |Connection Alias|Jira connection alias that you already created. Use the lookup \(![Lookup icon](../../project-workspace/image/lookup_icon.png)\) option to select your connection alias.|
    |Version|Jira version. Use the lookup \(![Lookup icon](../../project-workspace/image/lookup_icon.png)\) option to select your Jira API version.|

4.  Click **Submit**.


## Connect Agile Development 2.0 to Jira

Connect Jira to Agile Development 2.0 to enable the integration.

### Before you begin

Role required: sn\_jira\_int.user

### Procedure

1.  Navigate to **All** &gt; **Agile Jira Integration** &gt; **Jira Instances**.

2.  Open your Jira instance record.

3.  Click **Connect**.


### Result

-   If the connection is successful, the **State** field on the Jira Instance record shows Connected. A webhook is now registered in Jira to receive update events.
-   If the connection could not be established, the **State** field on the Jira Instance record shows Connection Failed. You can view the reason for the failure in the error message.

### What to do next

[Discover and import Jira projects and boards](../task/discover-projects.md)

.

