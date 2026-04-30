---
title: Modify the OpenLDAP schema
description: Modify the OpenLDAP schema. These steps detail a schema modification to OpenLDAP 2.3 provided by one of our customers that helped them integrate with their instance.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [OpenLDAP minor schema modification, LDAP integration, Authentication, Access Management]
---

# Modify the OpenLDAP schema

Modify the OpenLDAP schema. These steps detail a schema modification to OpenLDAP 2.3 provided by one of our customers that helped them integrate with their instance.

## Before you begin

Role required: admin

## About this task

**Warning:** The customization described here was developed for use in specific instances, and is not supported by Now Support. This method is provided as-is and should be tested thoroughly before implementation. Post all questions and comments regarding this customization to our community [forum](http://community.service-now.com/).

To modify the OpenLDAP schema for integration with the instance:

## Procedure

1.  Create a custom attribute.

    ```
    attribute ( 1.3.6.1.4.1.3403000.2.1.8
    
         NAME 'servnowid'
      ORDERING caseIgnoreOrderingMatch
      EQUALITY caseIgnoreMatch
      SYNTAX '1.3.6.1.4.1.1466.115.121.1.15' )
    ```

2.  Include the attribute in the selected objectclass OID.

    ```
    objectclass ( 1.3.6.1.4.1.3403000.2.2.1
         NAME 'BcfUserIdentifiers' SUP top AUXILIARY
      MAY ( uniqid $ unixid $ servnowid ) )
    ```

    In OpenLDAP 2.3, you can dynamically change the server configurations, but you can only extend the schema. You cannot modify or delete the existing schema. Instead of creating another objectclass for this attribute in the dynamic configuration, use the static configuration file, slapd.conf.

3.  In slapd.conf, include indexing for the new attribute in the bdb section of your main database backend.

    ```
    database bdb (configs here) .... 
    
    index servnowid pres 
    
    (other indexes here) ..... 
    ```

4.  As root, run slapindex to index this attribute to make it available in search filters.

    Make sure that the OpenLDAP daemon is not running or is in read-only mode before starting slapindex.


