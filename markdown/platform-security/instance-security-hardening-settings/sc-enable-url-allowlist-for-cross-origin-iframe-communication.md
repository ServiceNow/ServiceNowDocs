---
title: Enable URL allowlist for cross-origin iframe communication
description: Use the glide.ui.concourse.onmessage\_enforce\_same\_origin property to enable cross-origin communication between iframes.
locale: en-US
release: zurich
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enable URL allowlist for cross-origin iframe communication

Use the **glide.ui.concourse.onmessage\_enforce\_same\_origin** property to enable cross-origin communication between `iframes`.

`Openframe` can only process messages from trusted domains that are specified in the **glide.ui.concourse.onmessage\_enforce\_same\_origin\_whitelist** property. To learn more, see [Enable URL allowlist for cross-origin iframe communication](sc-enable-url-allowlist-for-cross-origin-iframe-communication.md).

## More information

|Attribute|Description|
|---------|-----------|
|Property name|**glide.ui.concourse.onmessage\_enforce\_same\_origin**|
|Configuration type|System Properties \(/sys\_properties\_list.do\)|
|Data type|Boolean|
|Category|[Access control](sc-access-control.md)|
|Purpose|To enable inclusion listing of trusted domains, so they can communicate between iframes for openframe.|
|Recommended value|true|
|Default value|true|
|Security risk rating|4.2|
|Functional impact|If you do not inclusion list intended domains, the ability to embed other pages within ServiceNow AI Platform instances may be limited.|
|Security risk|\(High\) If a web page contains event handlers that do not perform proper origin validation, a web page, or script from any origin, can communicate with it. It can also initiate any functionality performed by the event handler.|
|References|[OpenFrame overview](https://www.servicenow.com/docs/access?context=c_OpenFrameOverview&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)|

To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

