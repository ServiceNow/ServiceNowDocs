---
title: LDAP scripting
description: Create custom transform maps, scripts, and business rules to specify requirements when importing data.Use the following script to automatically deactivate users when the associated AD user is disabled.You can use a script to assign a value to any field for which there is a field mapping.If you cannot completely filter the LDAP user list using LDAP filter properties, you can exclude users with a map script.
locale: en-US
release: australia
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Import and map data, LDAP integration, Authentication, Access Management]
---

# LDAP scripting

Create custom transform maps, scripts, and business rules to specify requirements when importing data.

Custom transform maps should include `onStart` and `onAfter` transform scripts.

The `onStart` script should call the `LDAPUtils` script include and start logging. For example, the **LDAP User Import** transform map has an `onStart` script that uses this code:

```
gs.include ( "LDAPUtils" ) ; var ldapUtils  = new LDAPUtils ( ) ;
ldapUtils. setLog (log ) ;
```

The `onAfter` script should call the `addMembers` function. For example:

```
ldapUtils.addMembers (source , target ) ;
```

## Set disabled Active Directory users to inactive

Use the following script to automatically deactivate users when the associated AD user is disabled.

### Before you begin

Role required: admin

### About this task

You can identify disabled Active Directory users by checking the value of the `userAccountControl` attribute. This rule executes whenever the `userAccountControl` value changes and deactivates user accounts if the **User Account Control** signifies a disabled AD account.

Use the following script to automatically deactivate users when the associated AD user is disabled.

### Procedure

1.  Configure the User form and create a new integer field called **User Account Control**.

2.  Add mapping for userAccountControl \(external\) to the new field.

3.  Create a new business rule with the following properties:

    |Business rule field|Value|
    |-------------------|-----|
    |Name|Disable AD Users|
    |Table|User \[sys\_user\]|
    |When|Before|
    |Condition|current.u\_user\_account\_control.changes\(\)|

    The Script field should contain the following:

    ```
    var disabledFlag = 2;
    //perform a bitwise comparison on userAccountControl to see if the 2 bit flag is enabled
    if (current.u_user_account_control & disabledFlag) {
      gs.log('Disabling user: ' + current.user_name + 'userAccountControl=' + current.u_user_account_control);
      current.active='false';
      current.locked_out='true';
    }
    ```


## Assign LDAP field values

You can use a script to assign a value to any field for which there is a field mapping.

For example, to assign a value to the sys\_user.company field, create a field map for the company field and add a transform script of:

```
company = "Don's Sporting Goods";
```

## Exclude particular LDAP users

If you cannot completely filter the LDAP user list using LDAP filter properties, you can exclude users with a map script.

After you have run the logic to identify a user that should not be imported, set the user\_name field to an empty string and this user will not be imported.

```
user_name='';
```

One way to identify users to filter out is to look for a string in the `distinguishedName` attribute. For example, this script excludes accounts that are not in a Users OU. You might use this script if you have too many Users OU to include in the target OU LDAP Option.

```
//vdn is a variable mapped to distinguishedName
gs.include("LDAPUtils");
var vdn = source.getElement(this.distinguishedName);
if (vdn.indexOf('OU=Users')<0) {
  user_name='';
  gs.log('LDAP Import Skipping User: ' + vdn);
}
```

A more complex method of filtering is to use regular expressions.

```
//vcn is a variable mapped to cn
//vdn is a variable mapped to distinguishedName
//c is the regular expression string
gs.include("LDAPUtils");
var vdn = source.getElement(this.distinguishedName);
var vcn = source.getElement(this.cn);
var c = /^[a-z][a-z][a-z][0-9][0-9][0-9]$/;
var nvcn = vcn.toLowerCase();
//test to see if the cn is in the form of 3 letters followed by 3 numbers, only import these
if (c.test(nvcn)) {
	user_name = nvcn;
} else {
	gs.log("LDAP import rejected username: " + vcn + " for DN: " + vdn);
	user_name = "";
}
```

