---
title: Set up a MID Server to use IPKI authentication
description: Set up a new MID Server to authenticate to your instance with instance PKI \(IPKI\), where the instance issues the certificate that the MID Server uses. Use this procedure for a new MID Server.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/servicenow-platform/mid-server/mid-set-up-ipki-authentication.html
release: australia
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-10-29"
reading_time_minutes: 3
keywords: [iPKI, MID Server setup]
breadcrumb: [MID Server IPKI authentication, Securing and encrypting MID Server data, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Set up a MID Server to use IPKI authentication

Set up a new MID Server to authenticate to your instance with instance PKI \(IPKI\), where the instance issues the certificate that the MID Server uses. Use this procedure for a new MID Server.

## Before you begin

A local Windows service account with the Log on as a service right must exist on the host before you run the installer.

Role required: admin or agent\_admin

## About this task

In this task, you select IPKI as the authentication type in the MID Server onboarding step, configure the MID Server, and run the generated install command on the MID Server host. When the installation finishes, the MID Server authenticates to your instance with IPKI. Use this procedure for a new MID Server.

## Procedure

1.  On your instance, navigate to **Workspaces** &gt; **ITOM Infra Services Workspace**.

2.  Select the **MID Servers** icon in the navigation panel.

3.  On the **MID Onboarding** tab, select **Set up MID Server**.

4.  On the **Tell us about your environment** step, provide the requested environment details:

    1.  In the **Authentication type** list, select **ServiceNow Certificate \(private key JWT\)**.

    2.  Select the operating system you're installing the MID Server on.

    3.  In the **I want to install using a** list, select **Command line installer**.

        To set up the MID Server manually, select **Manual configuration via Zip file**. On the **MID onboarding** tab, the installation plan with detailed instructions appears for you to complete.

    4.  Select **Next: Configuration**.

    \[Omitted image "mid-server-onboarding-step1.png"\] Alt text: MID Server onboarding step showing ServiceNow certificate \(private key JWT\) authentication type selected.

5.  On the **Configure the MID Server** step, provide the requested configuration details:

    1.  In the **MID Server name** field, enter the MID Server name.

        **Warning:** Avoid spaces and special characters in the MID Server name. On Windows, the name becomes part of the Windows service name, and a space or special character can make that name invalid.

    2.  Expand **Advanced configuration settings** to configure any of the following optional settings:

        -   Turn on **Manually set MID Server user** to select the MID Server user from the **MID Server user** list.
        -   Turn on **Proxy configuration** if the host needs a proxy to reach the instance, then provide the **Proxy host** \(IP address\) and **Proxy port**.
        -   Turn on **Manually set service name** to set a custom **Service name**. By default, the Windows service name is `snc_mid_` followed by the MID Server name you gave.
    3.  Select **Next: Installation plan**.

        \[Omitted image "mid-server-onboarding-step2.png"\] Alt text: MID Server onboarding step showing the Configure the MID Server for iPKI configuration details.

    The installation plan appears with the install command generated from the details provided.

6.  On the installation plan, copy and run the install command from step 3 of the plan in the target installation folder.

    **Note:** Run the install command in PowerShell as an administrator.

    On success, `config.xml` is populated automatically with the registration key, user, and **mid.ipki.enabled** set to `true`.

    To reregister an existing MID Server whose certificate has expired or been revoked, see [Reregister MID Servers to restore IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-reregister-ipki-authentication.md).

    To generate a registration key as part of an automated or scripted deployment instead of using the wizard, see the registration-key API in [MID Server iPKI reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-ipki-reference.md).

7.  Enter the service account name and password when the MID Server installer prompts you.

8.  Verify the pre-install check summary and proceed with the installation.


## Result

After successful installation, the **Ensure new MID Server is working** step in the installation plan shows **Validated**. The MID Server authenticates to the instance using IPKI.

\[Omitted image "mid-server-onboarding-step3.png"\] Alt text: MID Server onboarding step showing the validated status after successful installation.

## What to do next

After you set up a MID Server to use IPKI authentication, you must add its capabilities, applications, and IP ranges.

-   [Configure MID Server capabilities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/t_ConfigureCapabilities.md)
-   [Configure an IP address range for the MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/t_ConfigureMIDIPRange.md)

**Parent Topic:**[MID Server IPKI authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/servicenow-platform/mid-server/mid-server-ipki-authentication.md)

