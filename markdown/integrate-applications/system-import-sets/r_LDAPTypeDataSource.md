---
title: LDAP type data source
description: An LDAP data source is automatically created when you configure your instance to integrate with LDAP.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data sources, Import sets, Imports, Workflow Data Fabric]
---

# LDAP type data source

An LDAP data source is automatically created when you configure your instance to integrate with LDAP.

![LDAP data source example](../image/data-source-ldap.png)

## Processing a large LDAP request without paging

When an LDAP server does not support paging, a large request is automatically broken into multiple smaller requests.

This process is known as "nibbling" the LDAP request. The large request is broken into multiple smaller requests based on the value of the **Query field** in the LDAP OU definition. This field should specify a unique value such as email address or user ID.

For example, the following LDAP query might return more than 1000 records.

```
(&(objectclass=user)(sn=*))
```

In this example, the LDAP server **Query field** is **preferredIdentity**. The instance then splits the large request into multiple smaller requests, grouping records based on the **preferredIdentity** value.

```
(&((&((preferredIdentity>=0)(preferredIdentity<=1))))((&(objectclass=user)(sn=*))))
(&((&((preferredIdentity>=1)(preferredIdentity<=2))))((&(objectclass=user)(sn=*))))
(&((&((preferredIdentity>=2)(preferredIdentity<=3))))((&(objectclass=user)(sn=*))))
. . .
(&((&((preferredIdentity>=9)(preferredIdentity<=a))))((&(objectclass=user)(sn=*))))
(&((&((preferredIdentity>=a)(preferredIdentity<=b))))((&(objectclass=user)(sn=*))))
(&((&((preferredIdentity>=b)(preferredIdentity<=c))))((&(objectclass=user)(sn=*))))
```

**Related topics**  


[LDAP integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/ldap-integration/c_LDAPIntegration.md)

[Specify LDAP attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/ldap-integration/t_SpecifyLDAPAttributes.md)

[Define LDAP organizational units](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/ldap-integration/t_DefineLDAPOrganizationalUnits.md)

