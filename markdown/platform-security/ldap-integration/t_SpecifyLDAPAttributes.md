---
title: Specify the LDAP attributes
description: Specify the attributes included in LDAP server queries by using the LDAP server Attributes field. This can enhance performance as well as security.
locale: en-US
release: zurich
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# Specify the LDAP attributes

Specify the attributes included in LDAP server queries by using the LDAP server **Attributes** field. This can enhance performance as well as security.

## Before you begin

Role required: admin

## About this task

By default, the system loads all of the attributes for each object that it has permission to read from your LDAP server. Using the **Attributes** field, you can specify and thereby limit the attributes the LDAP query returns. Using this approach for large LDAP imports can greatly improve the speed of those imports.

## Procedure

1.  Explicitly define attributes where possible.

    If there is information that you do not want exposed to the instance, exclude the attribute. If you do not specify LDAP server attributes, user transactions may freeze for extended periods of time when new attributes are added to an LDAP server object because the system will be busy loading data from the new attributes.

    **Note:** To use the manager lookup scripts described in Select or Create a Transform Map for LDAP Data, specify **manager** and **dn** \(distinguished name\) in the **Attributes** field. Neither attribute is required to be a part of a transform map.

    ![LDAP attributes.](../image/LdapAttributes.png)


