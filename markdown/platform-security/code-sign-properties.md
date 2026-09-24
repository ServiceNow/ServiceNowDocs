---
title: Properties installed with Code Signing
description: Code Signing adds the following properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/code-sign-properties.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [Administer and Troubleshoot, Code Signing, Platform Security]
---

# Properties installed with Code Signing

Code Signing adds the following properties.

<table id="table_fck_z3z_mzb"><thead><tr><th>

Property

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.codesigning.expanded.tracking.enabled

</td><td>

true\|false

</td><td>

When true, the validation length for the meta stack is increased for ecc\_queue topics listed in the **com.glide.codesigning.expanded\_tracking.topic.list** property.**Important:** Elevated Security is needed to modify this property.

</td></tr><tr><td>

com.glide.codesigning.expanded.tracking.length

</td><td>

Integer

</td><td>

Levels of Code Signing validation to occur when Code Signing is enabled. The default value is 3.**Important:** Elevated Security is needed to modify this property.

</td></tr><tr><td>

com.glide.codesigning.expanded\_tracking.topic.list

</td><td>

String

</td><td>

Comma-separated list of topics to be subject to increased meta-stack tracking.**Important:** Elevated Security is needed to modify this property.

</td></tr><tr><td>

com.glide.codesigning.tables.excluded\_from\_audit

</td><td>

String

</td><td>

Comma-separated list of tables that are excluded from Code Signing change auditing. Create, update, and delete operations on these tables don't generate an audit record. By default, this property excludes the internal tables that Code Signing uses for certificate storage, cryptographic module and policy configuration, and signing job tracking. For more information, see [Code Signing change audit data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/cs-vault-audit-data.md).

</td></tr><tr><td>

com.glide.codesigning.tracking.agent.validation.exclusion.list

</td><td>

String

</td><td>

Comma-separated list of ecc\_queue agents for which Code Signing should be skipped

</td></tr><tr><td>

com.glide.codesigning.tracking.debug

</td><td>

true\|false

</td><td>

When true, debug logging for the Code Signing tracker is enabled.

</td></tr><tr><td>

com.glide.codesigning.tracking.enabled

</td><td>

true\|false

</td><td>

When true, enables Code Signing caller tracking.**Important:** Elevated Security is needed to modify this property.

</td></tr><tr><td>

com.glide.codesigning.tracking.logging.enabled

</td><td>

true\|false

</td><td>

When true, enables logging for Code Signing tracking.

</td></tr><tr><td>

com.glide.codesigning.tracking.unsupported\_script\_tracking.enabled

</td><td>

true\|false

</td><td>

When true, ecc\_queue records inserted via unsupported scripts \(if detected\) aren’t notarized.**Important:** Elevated Security is needed to modify this property.

</td></tr><tr><td>

com.glide.codesigning.tracking.validation.fail\_fast

</td><td>

true\|false

</td><td>

When true, Code Signing verification fails at the first script validation failure instead of verifying all scripts.**Important:** Elevated Security is needed to modify this property.

</td></tr><tr><td>

com.glide.event\_handler.code\_signing.tracking

</td><td>

String

</td><td>

Defines the Event Handler that helps ensure that customers newly enabling Code Signing are configured to be as secure as possible.**Important:** Elevated Security is needed to modify this property.

</td></tr><tr><td>

com.glide.web\_service\_outbound.impl.codesigning.tracking

</td><td>

true\|false

</td><td>

When true, enables SOAPMessageV2 Code Signing tracking**Important:** Elevated Security is needed to modify this property.

</td></tr><tr><td>

com.snc.csf.maximum\_update\_size

</td><td>

Integer

</td><td>

The maximum number of records allowed in a Code Signing update set. This value should be limited to a value between 6000 to 10000. If this value is exceeded, multiple update sets are generated and are linked to the same parent update set to enable batch processing. This limitation prevents UI issues described in [KB0557104](https://buildtools1.service-now.com/kb_view.do?sysparm_article=KB0557104).

</td></tr><tr><td>

com.snc.csf.servicenow\_root\_of\_trust.disabled

</td><td>

true\|false

</td><td>

Whether the Root of Trust feature is active. The default value is `false`, meaning that ServiceNow build certificates are trusted.**Important:** This property can only be changed using a signed scheduled job from a user with the admin, security admin and KMF manager roles. For details on changing your Root of Trust, see [Change your Root of Trust configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/change-rot-overview.md).

</td></tr><tr><td>

com.snc.kmf.signature.validation.optin

</td><td>

true\|false

</td><td>

When true, enables Code Signing on your instance.**Important:** This property can only be changed via a request to Customer Service and Support.

</td></tr><tr><td>

glide.jdbcprobeloader.tracking

</td><td>

true\|false

</td><td>

Toggles Code Signing on or off for JDBC data sources.**Important:** Elevated Security is needed to modify this property.

</td></tr><tr><td>

glide.rest.codesigning.tracking

</td><td>

true\|false

</td><td>

When true, enables RESTMessageV2 Code Signing tracking.**Important:** Elevated Security is needed to modify this property.

</td></tr><tr><td>

sn\_cse.com.snc.csf.vault\_audit\_enabled

</td><td>

true\|false

</td><td>

When true, the platform records create, update, and delete operations on records protected by Code Signing in the **sn\_cse\_vault\_codesigning\_audit\_data** table. The default value is `true`. For more information, see [Code Signing change audit data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/cs-vault-audit-data.md).**Important:** Only a user with the codesigning\_admin role can modify this property.

</td></tr><tr><td>

sn\_cse.com.snc.csf.vault\_audit\_data\_max\_size

</td><td>

Integer

</td><td>

Maximum number of records that the **sn\_cse\_vault\_codesigning\_audit\_data** table retains. The default value is 9000. When the record count exceeds this value, the Vault Code Signing Audit Data Cleaner scheduled job deletes the oldest audit records until the count matches this value.**Important:** Only a user with the codesigning\_admin role can modify this property.

</td></tr><tr><td>

sn\_cse.com.snc.csf.vault\_audit\_data\_retention\_days

</td><td>

Integer

</td><td>

Number of days that the **sn\_cse\_vault\_codesigning\_audit\_data** table retains an audit record. The default value is 90. Values below 30 are treated as 30, and values above 360 are treated as 360.**Important:** Only a user with the codesigning\_admin role can modify this property.

</td></tr><tr><td>

sn\_cse.com.snc.csf.generate\_signature\_commit

</td><td>

true\|false

</td><td>

When true, a trusted instance generates signatures for eligible records during a source control commit from ServiceNow Studio. The default value is `false`. For more information, see [Signature generation during source control commit](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown).**Important:** Only a user with the codesigning\_admin role can modify this property.

</td></tr></tbody>
</table>**Parent Topic:**[Code Signing reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/code-signing-reference.md)

