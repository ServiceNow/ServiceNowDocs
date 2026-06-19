---
title: Secure data transfer using Service Bridge
description: Data transfer between the Impact Delivery Instance and Impact Store Application is facilitated via Service Bridge.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/impact/service-bridge-overview.html
release: zurich
product: Impact
classification: impact
topic_type: concept
last_updated: "2025-11-20"
reading_time_minutes: 1
breadcrumb: [Impact reference, Impact]
---

# Secure data transfer using Service Bridge

Data transfer between the Impact Delivery Instance and Impact Store Application is facilitated via Service Bridge.

Service Bridge is a core technology that enables secure integration and real-time data synchronization, maintaining consistency across both instances. The framework primarily handles outbound and inbound payloads using the sendPayload\(\) method for data transmission. sendPayload is a Service Bridge function that enables JSON data transfer to the transport queue. It is used internally and configured by the ServiceNow team to package and send data between the Impact Delivery Instance \(IDI\) and Impact Store Application. Tables are mapped between the two instances, and custom logic is applied for specific data synchronization needs.

For information on configuring the data transfer between the Impact Store Application and the Impact Delivery Instance see [Configure the Impact Store Application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/configuring-impact-platform.md).

For more information on Service Bridge, see .

For more information on Impact table mapping, see [Table and field level mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/table-field-level-mapping.md) and [Dependent applications installed with the Impact Store App](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/data-sync-idi-store.md).

**Parent Topic:**[Impact reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/impact/impact-reference.md)

