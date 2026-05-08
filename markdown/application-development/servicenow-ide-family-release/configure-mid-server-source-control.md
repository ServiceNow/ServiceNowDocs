---
title: Configure a MID Server to use source control with the ServiceNow IDE
description: Configure a MID Server to use source control with the ServiceNow IDE if your Git provider is behind a firewall.
locale: en-US
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate source control, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Configure a MID Server to use source control with the ServiceNow IDE

Configure a MID Server to use source control with the ServiceNow IDE if your Git provider is behind a firewall.

## Before you begin

Install a MID Server with a REST capability. For more information, see Installing the MID Server and Configure MID Server capabilities.

Role required: admin

## Procedure

1.  Change the application scope of the instance to ServiceNow IDE.

    1.  In the Unified Navigation, select the globe icon \(![Globe icon](../../applications/image/icon-scope.png)\).

    2.  Select **Application scope**.

    3.  Select **ServiceNow IDE**.

2.  Navigate to **All** &gt; **MID Server** &gt; **Applications**.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|A name for the MID Server Application.|
    |Default MID Server|The MID Server configured with a REST capability.|
    |Application|The ServiceNow IDE.|
    |Included in application ALL|An option to include this MID Server Application in the definition of ALL for a MID Server.|

5.  Select **Submit**.


## What to do next

If you haven't already, configure basic or OAuth 2.0 authentication to connect to a Git domain or repository. For more information, see [Connect to a Git provider using basic authentication with the ServiceNow IDE](connect-git-provider-basic-auth.md) or [Connect to a Git provider using OAuth 2.0 with the ServiceNow IDE](../concept/connect-git-provider-oauth-2.md#).

**Note:** The MID Server user must have the sn\_glider.ide\_git\_user role or admin role to perform Git operations in the ServiceNow IDE. For more information, see Create the MID Server user and grant the role and [ServiceNow IDE MID Server User \[sn\_glider.ide\_git\_user\]](../reference/servicenow-ide-roles.md#).

**Parent Topic:**[Integrating source control with the ServiceNow IDE](../concept/integrating-source-control-servicenow-ide.md)

**Related topics**  


[Connect to a Git provider using basic authentication with the ServiceNow IDE](connect-git-provider-basic-auth.md)

[Connect to a Git provider using OAuth 2.0 with the ServiceNow IDE](../concept/connect-git-provider-oauth-2.md#)

[Initialize a Git repository with the ServiceNow IDE](initialize-git-repository-servicenow-ide.md)

[Using source control in the ServiceNow IDE](../concept/using-source-control-servicenow-ide.md)

