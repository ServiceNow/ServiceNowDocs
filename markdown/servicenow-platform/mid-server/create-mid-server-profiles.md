---
title: Create MID Server profiles
description: Create a MID Server profile to configure MID Server settings, such as JVM memory, from your ServiceNow instance. MID Server profiles are available starting with the Zurich release and apply to all MID Server types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/mid-server/create-mid-server-profiles.html
release: zurich
product: MID Server
classification: mid-server
topic_type: task
last_updated: "2026-07-27"
reading_time_minutes: 1
keywords: [create MID Server profile, MID Server profiles, MID Server configuration]
breadcrumb: [MID Server profiles, Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Create MID Server profiles

Create a MID Server profile to configure MID Server settings, such as JVM memory, from your ServiceNow instance. MID Server profiles are available starting with the Zurich release and apply to all MID Server types.

## Before you begin

Role required: agent\_admin

## Procedure

1.  Navigate to **All** &gt; **MID Server** &gt; **Profiles and Deployments** &gt; **MID Server Profiles**.

    Alternatively, in the navigation filter, enter `mid_server_profile.list`.

2.  Select **New**.

3.  In the **Name** field, enter a name for the profile.\[Omitted image "create-new-midserver-profile.png"\] Alt text: MID Server Profile new record form with Name and Description fields.

4.  In the **Description** field, enter a description for the profile.

5.  Select **Submit**.

6.  Select the profile record you created.

7.  Select the relevant tabs and set the parameters to define the profile. \[Omitted image "mid-server-profile-record.png"\] Alt text: MID Server profile record showing configuration tabs.

    For example, in the **MID Profile Wrapper Configs** tab, select **New**, and then complete the fields.

    |Field|Description|
    |-----|-----------|
    |**Parameter name**|The parameter name. For example, `wrapper.java.maxmemory`.|
    |**Value**|The parameter value. For example, enter `4096` to set JVM maximum memory to 4096 MB.|

    **Tip:** To verify the JVM memory change was applied, check the `wrapper.log` file on the MID Server host and verify the `-Xmx` value matches your configured parameter.

    For more information on the tables available for configuration, see [MID Server profile configuration data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/mid-server-profile-configuration-data.md).

8.  Select **Submit**.

    **Tip:**

    You can also create profiles using the following alternative methods:

    -   On a MID Server profile record, in the Related Links section, select **Duplicate** to copy an existing profile record and customize it.
    -   On a MID Server record, in the Related Links section, select **Create MID Profile** to create a MID Server profile from the selected MID Server.

## What to do next

After creating the profile and setting its parameters, configure the MID Servers to use it. See [Configure MID Servers using profiles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/mid-server/configure-mid-server-profile.md).

