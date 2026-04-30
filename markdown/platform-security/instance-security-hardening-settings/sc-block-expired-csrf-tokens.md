---
title: Block Expired Anti-CSRF Tokens \[Updated in Security Center 1.5\]
description: Block expired CSRF tokens to prevent cross-site request forgery attacks.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Block Expired Anti-CSRF Tokens \[Updated in Security Center 1.5\]

Block expired CSRF tokens to prevent cross-site request forgery attacks.

## Overview

Cross-site request forgeries are a type of malicious exploit whereby unauthorized commands are performed on behalf of an authenticated user.

## Configuration details

|Attribute|Description|
|---------|-----------|
|Overview|Controls the usage of an expired secure token to identify and validate incoming requests. Set to **false** to prevent a previously expired token to validate an incoming request.|
|Configuration name|**glide.security.csrf\_previous.allow**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Data type|boolean|
|Recommended value|**false**|
|Default value|**true**|
|Category|[Access control](sc-access-control.md)|
|Security risk|**Severity score**: 6.5|
|**Severity rating per CVSS score**: Medium|
|**Security risk details**: Enforces a strong anti-CSRF mechanism to protect authenticated functionality, and effective anti-automation or anti-CSRF protects unauthenticated functionality.|
|Dependencies and prerequisites|None|
|References|[Enable Anti-CSRF token \[New in Security Center 1.3, updated in 1.5, and removed in 2.0\]](sc-anti-csrf-token.md), [cross-site request forgery](https://en.wikipedia.org/wiki/Cross-site_request_forgery).|

**Parent Topic:**[Access control](sc-access-control.md)

