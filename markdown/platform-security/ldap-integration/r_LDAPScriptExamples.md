---
title: LDAP script examples
description: The following script examples assume you use an Active Directory \(AD\) for your LDAP server.
locale: en-US
release: australia
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [LDAP record synchronization, LDAP integration, Authentication, Access Management]
---

# LDAP script examples

The following script examples assume you use an Active Directory \(AD\) for your LDAP server.

## userAccountControl attribute values script

This example tests the source for the userAccountControl attribute values associated with a disabled user \(514 or 546\).

```
//Deactivate LDAP-disabled users during transform based on 'userAccountControl' attribute
if(source.u_useraccountcontrol == '514' || source.u_useraccountcontrol == '546'){
   target.active=false;
   target.locked_out=true;
}
```

Here is an example using a bitwise check:

```

if(source.u_useraccountcontrol & 2){
   active = false;
}

```

## userAccountControl attribute script

This example examines the userAccountControl attribute but does not test for specific values. It also contains the option of reactivating LDAP user accounts.

```
/*
* Deactivate LDAP-disabled users during transform based on 'userAccountControl' attribute
* Convert the userAccountControl attribute back to a hex value
*/
var ctrl = parseInt(source.u_useraccountcontrol, 10);
ctrl = ctrl.toString(16);
 
/*
* The only digit we care about is the final one
* A final hex digit value of '2' in 'ctrl' means disabled
*/
if(ctrl.substr(-1) == "2"){
 
   //Deactivate and lock the user account
   target.active = false;
   target.locked_out = true;
 
   //Ignore any insert of a disabled record
   if(action == 'insert'){
      ignore = true;
   }
}
/* Optional: Uncomment else block to reactivate and unlock the user account
else {
   target.active = true;
   target.locked_out = ctrl.substr(-2, 1) == "1";
}
*/
```

## onBefore transform map script

Here is an example of a onBefore transform map script. The script identifies disabled records and records being inserted. If an insert of a disabled user is occurring, then the operation transform ignores the record.

```
//Ignore any insert of a disabled record as defined by the 'userAccountControl' attribute
var uc = source.u_useraccountcontrol;
if((uc == '514' || uc == '546') && action == 'insert'){
   ignore = true;
}
```

## DN member script

This script example introduces flexibility by not relying on the 546 and 514 userAccountControl values, but instead checking whether the user is a member of a particular Distinguished Name \(DN\). You can use this script either in the **Script** field of the ‘Table Transform Map’ record or in an onBefore transform map script.

```
//Deactivate LDAP-disabled users during transform based on OU membership in 'dn'
if(source.u_dn.indexOf('OU=Disabled Accounts') > -1){
   target.active = false;
   target.locked_out = true;
}
```

