---
title: Binding alerts to a specific host CI \(default binding\)
description: Binding alerts to Configuration Items \(CIs\) using the Node field or the CI Identifier field ensures accurate event association. By comparing an event record’s Node or CI Identifier value, alerts are linked to the right system. This improves response, root cause analysis, and impact assessment by providing clear visibility into affected assets.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-05-08"
reading_time_minutes: 3
breadcrumb: [Binding alerts to CIs, Event rules, Processing Events, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Binding alerts to a specific host CI \(default binding\)

Binding alerts to Configuration Items \(CIs\) using the **Node** field or the **CI Identifier** field ensures accurate event association. By comparing an event record’s **Node** or **CI Identifier** value, alerts are linked to the right system. This improves response, root cause analysis, and impact assessment by providing clear visibility into affected assets.

## How default binding works

The system can perform default binding using the **Node** field or the **CI Identifier** field from the event record.

When an event enters the system, a key field like **Node** is available in the event record. However, there is no **Node** field in the CI. Instead, the node value from the event is compared with various attributes in the host CI, such as Name, Fully Qualified Domain Name \(FQDN\), IP, or MAC address. If a match is found, the alert is linked to the corresponding CI. This is the default method for binding alerts to CIs.

The property **sa.active\_operation\_status** is used by the default binding mechanism, specifically when binding via IP/MAC using the node field in the event. When an event attempts to bind to a host through the node field \(using IP/MAC\), the system ignores hosts whose operational status is not included in this property and the operational status of the host must also not be null. By default, the property value is "1", which corresponds to Operational. You can extend the list to include additional statuses, and any status in the list is not ignored during binding.

Example: If **sa.active\_operational\_status** = "1,2", then both Operational and Non-operational hosts are considered valid for binding. The status attribute is defined by the following values:

-   1 – Operational
-   2 – Non-operational
-   3 – Repair in Progress
-   4 – DR Standby
-   6 – Retired

**Note:** In this binding process, the CI must be a host. Host CIs include Computers, Operating Systems \(OS\), Switches, Routers, or any CI type/class that extends the \[cmdb\_ci\_hardware\] table, meaning the CI type or class must be a hardware component.

If no match is found using node, the system looks at the **CI Identifier** field on the event record. The **CI Identifier** is a JSON structure containing column names and values for comparison \(e.g., Name, Fully qualified domain name, IP, or MAC Address\). The JSON is: \{"column\_name":"&lt;column\_value&gt;"\}. For example, if we want to bind to a CI identified by **serial\_number** whose value is **Dell Latitude 7420 Laptop**, the JSON is: `{"serial_number":"Dell Latitude 7420 Laptop"}`. If a match is found, the alert is linked to the corresponding CI.

## Difference between binding with Node vs. CI Identifier

In default binding, the system considers all fields in the **Additional Information** field and attempts to match their values with the CI table. The **CI Identifier** field allows specifying particular fields for matching, even if they are not present in **Additional Information**. This process uses a predefined JSON structure and applies only when the CI is a host.

**Note:** Even if the **Node** or the **CI Identifier** successfully binds the alert with the CI, event rules further determine how the binding occurs using the **Override default binding** check box available in Event rules. This ensures that alerts are bound correctly based on business logic, not just direct matches. This ensures that alerts are bound correctly based on business logic, not just direct matches.

## Example: Resolving a CI Using Node and Event Rules

Imagine a server \(Server-123\) in your network generates an event. The event record contains a **Node** field with the value "Server-123.example.com".

1.  Matching with CI Attributes:
    1.  The system checks the Node value against the CMDB.
    2.  It compares "Server-123.example.com" with the FQDN, IP, MAC address, or Name of existing host CIs.
    3.  If a match is found \(e.g., FQDN in the CMDB is also "Server-123.example.com"\), the alert is linked to that CI.
2.  Applying Event Rules: Even if the Node resolves to Server-123, additional event rules might determine if the alert should be linked differently. For example, an event rule may specify that alerts from Server-123 should be linked to a parent CI \(like a cluster\) instead of the individual server.

