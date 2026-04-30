---
title: LDAP transform maps
description: The transform map moves data from the import set table to the target table \(User or Group\).
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
breadcrumb: [Import and map data, LDAP integration, Authentication, Access Management]
---

# LDAP transform maps

The transform map moves data from the import set table to the target table \(User or Group\).

The LDAP integration uses standard import sets and transform maps. You can also create custom LDAP transform maps.

**Important:** Whether you select or create custom LDAP transform maps, there should be one active transform map for a set of source and target tables. Enabling multiple transform maps for the same source and target tables can produce duplicate entries in the target table unless you coalesce against the matching fields.

## Default LDAP transform maps

By default, the system provides two transform maps for LDAP data.

|Transform Map|Source Table|Target Table|Description|
|-------------|------------|------------|-----------|
|LDAP User Import|\[ldap\_import\]|\[sys\_user\]|Default transform map for creating user records from LDAP credentials as part of LDAP on-demand login. Contains mappings for an Active Directory LDAP server.|
|LDAP Group Import|\[ldap\_group\_import\]|\[sys\_user\_group\]|Default transform map for creating group records from LDAP OUs. Contains mappings for an Active Directory LDAP server.|

**Note:** By default, the system does not have a transform map for LDAP department records.

## Requirements for custom LDAP transform maps

If you choose to create a custom transform map, the transform map must meet the following mapping requirements.

<table id="table_RequirementsForCustomLDAPTransformMaps"><thead><tr><th>

Source Table

</th><th>

Source Field

</th><th>

Target Table

</th><th>

Target Field

</th><th>

Coalesce

</th><th>

Description

</th></tr></thead><tbody><tr><td>

`ldap_import`

</td><td>

`u_source`

</td><td>

`sys_user`

</td><td>

source

</td><td>

false

</td><td>

The **u\_source** field identifies the LDAP DN of the imported user or group. The system uses this field to determine that a user requires LDAP authentication, to find a user's manager, and to put users into groups.

</td></tr><tr><td>

`ldap_import`

</td><td>

Select one of the following fields:-   `u_samaccountname`
-   `u_dn`
-   `u_cn`

</td><td>

`sys_user`

</td><td>

`user_name`

</td><td>

true

</td><td>

If LDAP integrates to Active Directory, select **u\_samaccountname** as the source field. If other LDAP directories are used, select **u\_dn** or **u\_cn** as the source field.

</td></tr></tbody>
</table>## Differences between LDAP transform maps and legacy import maps

When specifying LDAP mapping relationships using transform maps, there is a major difference in how reference fields are set for manager and department.

When using a transform map, it is necessary to use a transform script to create references. This is because the value associated with an LDAP attribute like "manager" is the distinguished name \(DN\) of the manager.

Without some extra logic in place, the result is the creation of a user record with a manager name that is the distinguished name of that user in LDAP. The integration includes a transform script to facilitate the creation of these references. The default transform map "LDAP User Import" includes transform scripts for these references.

-   **Existing mapping relationships**

    When updating legacy import maps to transform maps, you can retain the LDAP mapping relationships that existed prior to the addition of the System LDAP application. The LDAP server has a **Map** field that is a reference to the legacy import map.

    **Note:** By default this field is hidden, so you have to configure the form to display it.

    If you want to transition to using a transform map, clear the reference to the legacy import map.

-   **LDAP import map settings**

    Verify and use attributes to limit the fields the integration imports from the LDAP source. Additionally, it is important to map the user\_name field to the LDAP attribute that contains the user's login ID. For Active Directory this is usually the sAMAccountName attribute. If you would like to import and coalesce on a binary attribute \(such as objectSID or objectGUID\), you have to create a custom transform script.

    **Note:** Any value mapped to the user\_name field must be unique.

    If you do not specify a transform map \(such as LDAP User Import\), the integration uses the following default mappings:

    |User field or variable|LDAP attribute|
    |----------------------|--------------|
    |user\_name|sAMAccountName|
    |email|mail|
    |phone|telephoneNumber|
    |home\_phone|homePhone|
    |mobile\_phone|mobile|
    |first\_name|givenName|
    |last\_name|sn|
    |title|title|
    |department|department|
    |manager|manager|
    |middle\_name|initials|
    |u\_memberof|groups|
    |u\_member|members|
    |u\_manager|manager|


## LDAP data transformation

If an LDAP attribute contains simple data, the transform map links an imported LDAP attribute to an appropriate field in the target table \(User or Group\). For example, sample data in the sAMAccountName attribute maps to the **User ID** field in the User table.

If the imported LDAP data maps to a reference field, the instance searches for an existing matching record. If no matching record exists, the instance creates a new record for the reference field unless the field mapping specifies otherwise.

For example, suppose the LDAP attribute l maps to the **Location** reference field in the User table. Whenever the import brings in an attribute value that does not match an existing location record value, the transform map creates a new location record. The new location record has the same value as the imported attribute, and the imported user record now has a link to the new location record.

However, there are times when LDAP attribute returns a distinguished name \(DN\), which is essentially a reference to another record within the LDAP directory. For example, the manager attribute typically contains the distinguished name for the manager of the current LDAP directory entry. An imported DN typically uses a long text string such as: cn=Beth Anglin,ou=Users,dc=my-domain,dc=com.

**Warning:** Make sure your target fields are long enough to contain a DN. Many text fields use the default length of 40, which may not be long enough for some DN values. The ServiceNow system truncates any value that exceeds the field length.

Administrators do not typically want the system to create new users from the DN value because the new user has no association with an existing user. Instead, administrators want the import to locate the manager's existing user record and associate it with the newly imported user. The `LDAPUtils` script include contains the `setManager` and `processManagers` functions that can parse a DN and search for an existing user. For best results, use these functions to create a custom transform map.

For example, the `LDAP User Import` transform map script calls the `setManager` function:

```

// 
// The manager coming in from LDAP is the DN value for the manager.   
// The line of code below will locate the manager that matches the 
// DN value and set it into the target record.  If you are not  
// interested in getting the manager from LDAP then remove or 
// comment out the line below
ldapUtils. setManager (source , target ) ;
```

In some cases, the integration imports a user's record before importing the associated manager's user record. To handle such cases, you may want to call the `processManagers` function after the transform completes. For example, the **LDAP User Import** transform map uses an `onComplete` transform script to call the `processManagers` function.

```
// It is possible that the manager for a user did not exist in the database when // the user was processed and therefore we could not locate and set the manager field. // The processManagers call below will find all those records for which a manager could  // not be found and attempt to locate the manager again. This happens at the end of the  // import and therefore all users should have been created and we should be able to  // locate the manager at this point 
ldapUtils. processManagers ( ) ;
```

Remove or comment out the `setManager` and `processManagers` function calls if your LDAP integration does not use the manager attribute.

