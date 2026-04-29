---
title: Restrict access
description: Service Catalog enables an administrator to grant or deny access to a service catalog item or category by company, department, group, user, or location.By default, individual catalog items and categories do not have access restrictions.Service Catalog enables you to control access to a service catalog item or category with a custom script.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legacy service catalog access controls, Service Catalog security, Configuring Service Catalog, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Restrict access

Service Catalog enables an administrator to grant or deny access to a service catalog item or category by company, department, group, user, or location.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Maintain Items** or **Service Catalog** &gt; **Maintain Categories**.

2.  Open the relevant catalog item or category.

3.  [Configure the form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&section=t_ConfigureAForm&ft:locale=en-US) to add the appropriate **Available** or **Not available** lists.

    ![access control](../image/AccessControl.png "Access Control")

4.  Add the companies, departments, groups, users, or locations to the appropriate list.

5.  Click **Update**.


**Parent Topic:**[Legacy service catalog access controls](../concept/c_LegcySrvcCatAccessCntrol.md)

## Restrict access by role

By default, individual catalog items and categories do not have access restrictions.

### Before you begin

Role required: admin

### About this task

Administrators can grant or deny access to a service catalog item or category based on role.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Maintain Items** or **Service Catalog** &gt; **Maintain Categories**.

2.  Open the relevant catalog item or category.

3.  Add the required roles to the **Roles** field.

    You can, if needed, [Configure the form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US) or change to **Default View** to see the **Roles** field.

    ![roles granted](../image/RolesGranted.png "Roles Granted")


## Restrict access by a script

Service Catalog enables you to control access to a service catalog item or category with a custom script.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Maintain Items** or **Service Catalog** &gt; **Maintain Categories**.

2.  Open the relevant catalog item or category.

3.  [Configure the form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&ft:locale=en-US) to add the **Entitlement Script** field.

    ![entitlement script](../image/EntitlementScript.png "Entitlement Script")

4.  In the **Entitlement Script** field, enter the access control script.

    Sample Scripts:

    The following example script grants access to a catalog item named French Blackberry to users with a language of Fr \(French\):

    ```
    gs.log ( 'Running Entitlement script for French Blackberry' ) ;
     
     if (gs. getUser ( ). getLanguage ( ) == 'fr' ) 
        answer = true ; else 
        answer = false ;
     
    answer ;
    ```

    The following example script could be used to distinguish between two categories of users \(one with full access and one with restricted access\) on the catalog of services:

    ```
    var userid  = gs. getUserID ( ) ; var now_GR  = new GlideRecord ( 'sys_user' ) ; 
    now_GR. get ( 'sys_id' , userid ) ; 
     
     if (now_GR. source )
        answer = true ; else
        answer = false ; 
     
    answer ;
    ```

    Overriding Entitlement Scripts by Role

    1.  Navigate to **Service Catalog** &gt; **Properties**.
    2.  Enter the roles for which to override the entitlement script \(grant access\) in the property List of roles \(comma-separated\) that can override normal entitlement checking inside the catalog. An itil role of "itil" means that the itil role can order any catalog item, even one protected by entitlement restrictions.

