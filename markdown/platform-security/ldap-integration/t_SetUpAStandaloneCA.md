---
title: Set up a stand-alone certificate authority for active directory
description: The first step to configure Microsoft Active Directory for SSL access is to set up a stand-alone Certificate Authority \(CA\).
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configure Microsoft Active Directory for secure LDAPS communication, LDAP integration, Authentication, Access Management]
---

# Set up a stand-alone certificate authority for active directory

The first step to configure Microsoft Active Directory for SSL access is to set up a stand-alone Certificate Authority \(CA\).

## Before you begin

Role required: admin

## About this task

Do not worry about addition resource utilization because both of the required services \(IIS &amp; CA\) can be disabled after issuing the certificate\(s\).

## Procedure

1.  Install Internet Information Server \(IIS\).

2.  Install Certificate Authority Services in stand-alone mode.

3.  Verify the Certificate Services web application is installed and active.


## What to do next

Using the IIS Manager console, expand the local computer and select Web Sites. The state of **Default Web Site** should be Running. You should also see a CertSrv application listed under the **Default Web Site**. If the site is not running or the application is missing, you must resolve the issue before you proceed.

