---
title: Find inactive LDAP accounts by using the userAccountControl field
description: Identify when an Active Directory \(AD\) user is deleted \(or made inactive\).
locale: en-US
release: australia
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Inactive LDAP user accounts, LDAP record synchronization, LDAP integration, Authentication, Access Management]
---

# Find inactive LDAP accounts by using the userAccountControl field

Identify when an Active Directory \(AD\) user is deleted \(or made inactive\).

## Before you begin

Role required: admin

## About this task

One method is to track the active status of AD users and create a business rule to update corresponding accounts when an AD account is inactive.

## Procedure

1.  Create a new string field on the User \[sys\_user\] table to track the value of the AD **userAccountControl** field.

    For example: `u_ad_user_account`.

2.  Create an LDAP transform script to set the field value.

    ```
    target.u_ad_user_account = source.userAccountControl
    ```

3.  Update the LDAP filter to show disabled AD accounts.

    Here is an example of a filter.

    ```
    (&(objectClass=person)(sn=*)(!(objectClass=computer))(!(userAccountControl:1.2.840.113556.1.4.803:=2)))
    ```

    Here is an example of a replacement filter you can use.

    ```
    (&(objectClass=person)(sn=*)(!(objectClass=computer)))
    ```

4.  Create an onChange business rule to set the active field to false whenever the u\_ad\_user\_account field has the value 514.

    '514' indicates an inactive account.


