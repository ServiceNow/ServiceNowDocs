---
title: Supported and unsupported fields in Identity Access and Audit
description: A list of fields that support auditing and those that do not.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Identity and Access Audit, Identity]
---

# Supported and unsupported fields in Identity Access and Audit

A list of fields that support auditing and those that do not.

Audit Fields Validation prevents some fields from being selected in the field\_list in the Security Field Audit Config \(sys\_sec\_field\_audit\_config\) table.

<table id="table_zcw_t4b_nzb"><thead><tr><th>

Table

</th><th>

Fields supported or not supported

</th></tr></thead><tbody><tr><td>

**All tables**

</td><td>

Fields that aren’t supported:

 -   Created On \(sys\_created\_on\)
-   Created By \(sys\_created\_by\)
-   Updated By \(sys\_updated\_by\)
-   Updated On \(sys\_updated\_on\)

</td></tr><tr><td>

**User has role \(sys\_user\_has\_role\)**

</td><td>

Fields that are supported:-   User
-   Role
-   Inherited
-   Count

</td></tr><tr><td>

**User \(sys\_user\)**

</td><td>

Fields that aren't supported:-   Last Login \(last\_login\)
-   Last Login Time \(last\_login\_time\)
-   Last Login Device \(last\_login\_device\)
-   Enable Multi-factor Authentication \(enable\_multifactor\_authn\)
-   Default Perspective \(default\_perspective\)
-   Calendar Integration \(calendar\_integration\)
-   Federated ID \(federated\_id\)
-   Password Needs Reset \(password\_needs\_reset\)
-   Failed Attempts \(failed\_attempts\)
-   Last Password \(last\_password\)
-   LDAP Server \(ldap\_server\)
-   Locked Out \(locked\_out\)
-   Notification \(notification\)
-   Roles \(roles\)
-   Domain \(sys\_domain\)
-   Domain Path \(sys\_domain\_path\)
-   Time Format \(time\_format\)
-   Hashed User ID \(hashed\_user\_id\)
-   Class Name \(sys\_class\_name\)
-   Mod Count \(sys\_mod\_count\)

</td></tr></tbody>
</table>