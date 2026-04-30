---
title: Set up ADAMSync
description: ADAMSync is included with Windows Server 2003 R2. Download and install ADAMSync if you are using a different OS.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use ADAMSync to populate ADAM, Active Directory Application Mode \(ADAM\), LDAP integration, Authentication, Access Management]
---

# Set up ADAMSync

ADAMSync is included with Windows Server 2003 R2. Download and install ADAMSync if you are using a different OS.

## Extending the schema

The ADAM schema needs to be extended to support ADAMSync.

1.  Run the following command from c:\\windows\\adam to import the ADAMSync schema extensions. You may have to change the server:port and add credentials if the current user doesn't have access. See the AdamSyncMetadata.ldf file for details.

    ```
    ldifde -i -f MS-AdamSyncMetadata.LDF -s localhost:50000 -j . -c "cn=Configuration,dc=X" #configurationNamingContext
    ```

2.  Do the same with MS-AdamSchemaW2k3.ldf to support Windows 2003 attributes.

    ```
    ldifde -i -u -f MS-AdamSchemaW2K3.LDF -s localhost:50000 -j . -c "cn=Configuration,dc=X" #configurationNamingContext
    ```


## Recommended schema changes

Here are some additional schema changes we recommend.

1.  Open a new MMC console and add the ADAM Schema Snap-in.
2.  Connect to the ADAM instance.
3.  Expand the Classes folder and locate the userProxy class, open **Properties**.
4.  Verify the following optional attributes on the Attributes tab, add any that do not already exist.
    -   company
    -   department
    -   givenNane
    -   mail
    -   physicalDeliveryOfficeName
    -   sAMAccountName
    -   sn
    -   telephoneNumber
    -   title
    -   userAccountControl
    -   userPrincipalName
5.  Restart the ADAM Service to enable the new settings.

