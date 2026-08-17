---
title: Configure a MID Server to use source control
description: Configure a MID Server to use source control with ServiceNow Studio if your Git provider is behind a firewall.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/fluent-sc-configure-mid-server-to-use-sc.html
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: task
last_updated: "2026-07-24"
reading_time_minutes: 1
keywords: [MID Server, ServiceNow Studio, pro-code development]
breadcrumb: [Fluent source control in ServiceNow Studio, Source control integration, Use, ServiceNow Studio, Developing your application, Building applications]
---

# Configure a MID Server to use source control

Configure a MID Server to use source control with ServiceNow Studio if your Git provider is behind a firewall.

## Before you begin

Install a MID Server with a REST capability. For more information, see [Installing the MID Server with manual or guided setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/mid-server-installation.md) and [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_ConfigureCapabilities.md).

Role required: admin

## Procedure

1.  Change the application scope of the instance to ServiceNow IDE.

    1.  In the Unified Navigation, select the globe icon \[Omitted image "icon-scope.png"\] Alt text:.

    2.  Select **Application scope**.

    3.  Select **ServiceNow IDE**.

2.  Navigate to **All** &gt; **MID Server** &gt; **Applications**.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the MID Server Application.|
    |Default MID Server|MID Server configured with a REST capability.|
    |Application|The ServiceNow IDE.|
    |Included in application ALL|Option to include this MID Server Application in the definition of ALL for a MID Server.|

5.  Select **Submit**.


## What to do next

If you haven't already, configure basic or OAuth 2.0 authentication to connect to a Git domain or repository. For more information, see [Connect to a Git provider using basic authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-connect-to-git-provider-basic-auth.md) or [Connect to a Git provider using OAuth 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-sc-connect-to-git-provider-oauth-2-0.md).

**Note:** The MID Server user must have the sn\_glider.ide\_git\_user role or admin role to perform Git operations in ServiceNow Studio. For more information, see [Create the MID Server user and grant the role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_SetupMIDServerRole.md) and [ServiceNow IDE MID Server User \[sn\_glider.ide\_git\_user\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/servicenow-ide-roles.md).

**Parent Topic:**[Fluent source control in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-studio-classic/fluent-source-control-sn-studio.md)

