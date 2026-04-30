---
title: Access Controls Auditor checks
description: Learn about the checks available in the default Access Controls Auditor Suites, what criteria they evaluate, and how they can be used to improve the security of your instance.
locale: en-US
release: yokohama
product: Security Center
classification: security-center
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Scan suites, Security scanner, Security configuration console, Security Center, Platform Security]
---

# Access Controls Auditor checks

Learn about the checks available in the default Access Controls Auditor Suites, what criteria they evaluate, and how they can be used to improve the security of your instance.

Access Control List rules \(ACLs\) restrict access to data by requiring users to pass a set of requirements before they can interact with it. Access Controls Auditor checks evaluate your instance according to the eight criteria listed in the following table. Use the findings on these checks to improve the security of your instance.

|Check Name|Check Criteria|Description|
|----------|--------------|-----------|
|All Processors of type - SCRIPT must be protected with CSRF Token|Checks for Processors with the **SCRIPT** type that aren’t protected with a CSRF token.|All Processors with the **SCRIPT** type should be protected with a Cross-site Request Forgery \(CSRF\) token. These processors should have the CSRF option checked, which prohibits the processor from running unless the instance uses a CSRF token.|
|Can Contribute / Cannot Contribute user criteria to be defined on each knowledge|Checks for knowledge base records that don’t have **Can Contribute** or **Cannot Contribute** user criteria defined.|Each knowledge base should have either **Can Contribute** or **Cannot Contribute** user criteria defined. Otherwise, any user can contribute content to a knowledge base with no Contribute criteria defined.|
|Empty ACLs|Checks for Access Control List \(ACL\) records that have no security attribute, no role, or the **public** role.|Leaving ACLs empty or using the **public** role may provide open access to any content protected by this ACL.|
|Access Controls on Client callable Script Includes|Checks for client-callable script includes that aren’t secured by ACLs.|All client callable script includes should be secured with an ACL using required roles.|
|Access controls on UI Pages|Checks for UI Pages that aren’t secured by ACLs|Without an ACL securing access to a UI Page, that UI Page is accessible to all logged-in internal users. Without any restrictions logged-in users can potentially make unauthorized changes.|
|Access controls on Tables|Checks for tables without ACLs|Tables should be secured with ACLs. Access to data stored in tables should be limited only to users that need it.|
|User Account shouldn’t have both Internal and External roles|Checks for user records with both **Internal** and **External** roles assigned|Internal user roles are intended for users within your company. External user roles are intended for external personnel, such as customers and partners.|
|Publicly accessible knowledge base and articles|Checks for publicly accessible knowledge bases and knowledge base articles|Publicly accessible knowledge bases and articles are visible to all users in the instance. Increase security by limiting knowledge bases and articles to the specific audience that needs them.|

**Parent Topic:**[Scan suites](../concept/sec-center-suites.md)

