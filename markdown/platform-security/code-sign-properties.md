---
title: Properties installed with Code Signing
description: Code Signing adds the following properties.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Code Signing reference, Code Signing, Platform Security]
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

com.snc.csf.servicenow\_root\_of\_trust.disabled

</td><td>

true\|false

</td><td>

Whether the Root of Trust feature is active. The default value is `false`, meaning that ServiceNow build certificates are trusted.**Important:** This property can only be changed using a signed scheduled job from a user with the admin, security admin and KMF manager roles. For details on changing your Root of Trust, see [Change your Root of Trust configuration](../concept/change-rot-overview.md).

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

</td></tr></tbody>
</table>**Parent Topic:**[Code Signing reference](code-signing-reference.md)

