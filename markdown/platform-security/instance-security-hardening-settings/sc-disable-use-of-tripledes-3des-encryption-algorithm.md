---
title: Disable use of TripleDES/3DES encryption algorithm
description: Avoid the security risks of outdated encryption methods by disabling the use of the TripleDES/3DES encryption algorithm.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Stored cryptography, Hardening settings, Platform Security]
---

# Disable use of TripleDES/3DES encryption algorithm

Avoid the security risks of outdated encryption methods by disabling the use of the TripleDES/3DES encryption algorithm.

Disable the use of legacy, deprecated Triple Data Encryption Standard \(3DES or Triple-DES\) on your instance, which may lead to loss and leakage of sensitive information.

The National Institute of Standards and Technology \(NIST\) has advised against using Triple DES \(3DES\) to encrypt data. For more details, refer to NIST 800-131A Rev 2.  3DES is now banned for encryption in federal systems. Going forward, TDES can only be used for historical purposes, such as decrypting old messages, key unwrapping, and MAC verification.

The **glide.security.3des.encryption.allow** system property controls whether 3DES encryption is enabled on your instance, however there are several steps which may need to be taken to verify that your instance is ready for deprecation. Review [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=915ce1dd474f2650f64de825126d43c1) for further information on the deprecation process before setting this property.

## More information

|Attribute|Description|
|---------|-----------|
|Technical configuration name|glide.security.3des.encryption.allow|
|Plugin applicability|None|
|Security risk|Usage of outdated and weak encryption like 3DES may lead to loss and leakage of sensitive information.|
|Common Vulnerability Scoring System \(CVSS\) score|4.2|
|Common Vulnerability Scoring System \(CVSS\) rating|Medium|
|Functional impact|Setting this property to **false** helps prevent your instance from use of outdated and weak encryption. This affects how Password2 data is stored. Review [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=294339844799e654f64de825126d43d1) for further information on functional impact of 3DES deprecation.|
|Dependencies and prerequisites|Perform the tasks outlined in [KB1704481](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=294339844799e654f64de825126d43d1) before changing the value of this property.|
|Data type|Boolean|
|Base system value|false|
|Fallback value|false|
|Recommended value|false|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Stored cryptography](sc-stored-cryptography.md)

