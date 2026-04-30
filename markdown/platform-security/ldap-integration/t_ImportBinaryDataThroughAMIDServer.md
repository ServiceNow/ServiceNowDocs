---
title: Import binary data through a MID Server
description: As an administrator, you can import binary large object \(BLOB\) data with an LDAP integration through the MID Server.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [LDAP integration via MID Server, LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# Import binary data through a MID Server

As an administrator, you can import binary large object \(BLOB\) data with an LDAP integration through the MID Server.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Add the name of the LDAP column you want to import binary data from to the system property `glide.ldap.binary_attributes`.

2.  Add a MID Server property with the Name `glide.ldap.binary_attributes` and the same value you set for the system property.


