---
title: Hermes Messaging Service system properties
description: These system properties control the behavior of the Hermes Messaging Service.
locale: en-US
release: australia
product: Multi-Instance Framework - Hermes
classification: multi-instance-framework-hermes
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Hermes Messaging Service, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Hermes Messaging Service system properties

These system properties control the behavior of the Hermes Messaging Service.

To set Hermes Messaging Service system properties, navigate to the System Properties \[sys\_properties\] table and add the property.

<table id="table_tmy_syv_4xb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Encoding format for message payload in the Hermes Messaging Service topic inspector

 `glide.hermes.topic.inspector.payload.format`

</td><td>

By default, messages in the **Payload** column are displayed as strings in UTF8. You can display binary data using base-64 encoding by adding this system property and setting the value to binary.-   string: display message payload in UTF8
-   binary: display message payload in base64

</td></tr><tr><td>

Encoding format for message keys in the Hermes Messaging Service topic inspector

 `glide.hermes.topic.inspector.key.format`

</td><td>

By default, identifiers in the **Keys** column are displayed as strings in UTF8. You can display binary data using base-64 encoding by adding this system property and setting the value to binary.-   string: display keys in UTF8
-   binary: display keys in base64

</td></tr></tbody>
</table>**Parent Topic:**[Hermes Messaging Service reference](../concept/hermes-messaging-service-reference.md)

**Related topics**  


[Hermes Messaging Service components](../concept/hermes-messaging-service-components.md)

[Hermes Messaging Service security model](../concept/hermes-messaging-service-security-model.md)

[Hermes Messaging Service roles](hermes-messaging-service-roles.md#)

[Hermes Messaging Service domain separation](hermes-messaging-service-domain-separation.md)

