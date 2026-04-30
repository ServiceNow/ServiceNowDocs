---
title: MID Server domain separation
description: Use the MID Server user role to configure MID Servers to access separate domains. The credentials in the config.xml file of a MID Server determine which domains it can access. Specific MID Server policy records can be restricted for use only by MID Server from the same domain.Set up domain separation through the MID server user role and the MID Server configuration file.You can create a MID Server in the global domain that can explore targets in other domains.
locale: en-US
release: zurich
product: MID Server
classification: mid-server
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Configuring MID Servers, Configuring MID Server, MID Server, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# MID Server domain separation

Use the MID Server user role to configure MID Servers to access separate domains. The credentials in the `config.xml` file of a MID Server determine which domains it can access. Specific MID Server policy records can be restricted for use only by MID Server from the same domain.

<table id="table_qxn_nt4_nhb"><tbody><tr><td>

![Setup indicator for configuration phase](../image/ProgressBarConfig.png)

</td></tr></tbody>
</table>The records that can be read, updated, or created by a MID Server are determined by the credentials configured for that MID Server in the `config.xml` file. These are the user credentials that a MID Server uses to access the instance and specify which domain's records that MID Server can access.

You can create versions of these specific MID Server policy records that only a MID Server from the same domain can use. This process separation is supported for records in tables that extend MID Server Synchronized Files \[ecc\_agent\_sync\_file\]:

-   MID Server MIB File \[ecc\_agent\_mib\]
-   MID Server JAR File \[ecc\_agent\_jar\]
-   MID Server Script File \[ecc\_agent\_script\_files\]

**Note:** Attachments on MIB or JAR file records might not appear as they did in a non-domain separated environment. The attachments do not appear because the **Attachments** \[sys\_attachment\] table is data separated. When data is separated between domains, a record in a child domain cannot access records in a parent domain.

**Parent Topic:**[Configuring MID Servers](c_MIDServerConfiguration.md)

## Set up domain separation for MID servers

Set up domain separation through the MID server user role and the MID Server configuration file.

### Before you begin

Role required: agent\_admin or admin

### Procedure

1.  [Configure a MID Server user](../task/t_SetupMIDServerRole.md#) within a specified domain with the proper **mid\_server** role.

2.  Specify this user within the MID Server **config.xml** file.

    When you set the [MID Server user credentials](mid-server-install-prereqs.md#) in the `config.xml` file, make sure they are in the proper domain.


### What to do next

If you must change the MID Server domain:

1.  Stop the MID Server and delete the ecc\_agent record.
2.  Update the MID Server `config.xml` with the new user in the new domain and restart the MID Server service.

If you need to create versions of specific MID Server files that only MID Servers in your domain can use:

1.  Open or create a record in one of these MID Server modules:
    -   **SNMP MIBs**
    -   **JAR Files**
    -   **Script Files**
2.  Update an existing domain policy or submit a new record.

    **Note:** Attachments on MIB or JAR file records might not appear as they did in a non-domain separated environment. The attachments do not appear because the **Attachments** \[sys\_attachment\] table is data separated. When data is separated between domains, a record in a child domain cannot access records in a parent domain.


## Configure a multi-domain MID Server

You can create a MID Server in the global domain that can explore targets in other domains.

### Before you begin

Before configuring a multi-domain MID Server:

-   Activate the Domain Support - Domain Extensions Installer \[com.glide.domain.msp\_extensions.installer\] plugin.
-   Ensure that your instance is [domain separated](https://www.servicenow.com/docs/access?context=c_DomainSeparation&version=zurich&pubname=zurich-platform-security&ft:locale=en-US).

Role required: admin

### Procedure

1.  Type **sys\_properties.list** in the navigation filter and press **Enter**.

2.  Locate the **glide.ecc.enable\_multidomain\_mid** property.

3.  Set the value of the property to **true**.

    **Note:** Enabling this property has no effect on existing MID Servers. MID Servers in a domain prior to setting this property, remain in that domain.

4.  Create a MID Server in the global domain.

    A MID Server created in the global domain after this property is set to **true** can explore any domain for which it has the credentials. However, this MID Server is restricted to trying only the credentials for the target domains requested by ECC Queue inputs.

    **Warning:** If you reset the **glide.ecc.enable\_multidomain\_mid** property to **false** after creating a multi-domain MID Server in the global domain, that MID Server writes all the data it receives to the global domain and not to the correct domains.


