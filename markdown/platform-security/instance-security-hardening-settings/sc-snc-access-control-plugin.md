---
title: Enable SNC access control plugin \[Updated in Security Center 1.3\]
description: Activate the SNC Access Control \(com.snc.snc\_access\_control\) plugin to control access to your instances by Customer Service and Support personnel.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable SNC access control plugin \[Updated in Security Center 1.3\]

Activate the SNC Access Control \(com.snc.snc\_access\_control\) plugin to control access to your instances by Customer Service and Support personnel.

Prevent ServiceNow Customer Service and Support personnel from accessing the instances without your express permission by enabling the SNC Access Control \(com.snc.snc\_access\_control\) plugin. Although all access to your instance is audited, you may prefer to control this access. This access method is fully auditable and tracked.

**Note:** Other authorized ServiceNow Operations personnel, in their capacity to support and manage the product, are required to perform administrative actions on the underlying infrastructure. Enabling this plugin may affect support service levels and the Availability SLA. Availability SLA is then measured from the time that Support staff personnel are granted access to your instance.

Enable the SNC Access Control \(com.snc.snc\_access\_control\) plugin to restrict access to your instance without your express permission. For more details on this feature, see [ServiceNow access control](../../security/concept/c_SNCAccessControl.md). For activation information, see [Activate ServiceNow access control](../../security/task/t_ActivateSNCAccessControl.md)

## More information

|Attribute|Description|
|---------|-----------|
|Plugin Name|**com.snc.snc\_access\_control**|
|Configuration type|System Definition &gt; Plugins|
|Category|[Access control](sc-access-control.md)|
|Purpose|Prohibits Customer Service and Support employees from accessing the instance|
|Recommended value|Active|
|Default value|None. This is a plugin, not a Glide property, so there is no default value. The plugin is not installed by default.|
|Role required|The customer administrator can't activate this plugin. It must be explicitly requested because it requires elevated privileges to activate the plugin.|
|Security risk rating|3.3|
|Functional impact|If this plugin is inactive, all Customer Service and Support employees can access the customer's instance. Enabling the plugin enables the customer to restrict access to authorized Customer Service and Support employees only.|
|Security risk|\(High\) Unnecessary exposure of instance access to wider group of people.|
|References|[ServiceNow access control](../../security/concept/c_SNCAccessControl.md)|

## Steps to configure

1.  To request the plugin, follow the steps in [Activate ServiceNow access control](../../security/task/t_ActivateSNCAccessControl.md). Customers must request the SNC Access Control plugin \(com.snc.snc\_access\_control\) from HI.
2.  To enable SNC access control, follow the steps in [Configure ServiceNow access control](../../security/task/t_ConfigureAccessControl.md). Configure an access control record to specify one or more Customer Service and Support employees that have permission to log in your instance.

**Parent Topic:**[Access control](sc-access-control.md)

