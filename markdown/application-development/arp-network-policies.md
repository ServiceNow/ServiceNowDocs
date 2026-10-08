---
title: Network policies
description: Network policies allow list the external hosts and endpoints that an application is permitted to access. Application Runtime Policy \(ARP\) generates network policies automatically when your application attempts to connect to external networks during development.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/arp-network-policies.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Explore, Application Runtime Policy \(ARP\), Developing your application, Building applications]
---

# Network policies

Network policies allow list the external hosts and endpoints that an application is permitted to access. Application Runtime Policy \(ARP\) generates network policies automatically when your application attempts to connect to external networks during development.

Some application functionality might require access to an external network to use a third-party API or content delivery URL. When an application's client-side or server-side code attempts to connect to an external network, Application Runtime Policy \(ARP\) tracks the access and generates a policy in the Network Policies table \[sys\_arp\_network\_policy\]. To navigate to a specific policy record from the network policies table, hover over a policy and select the preview icon\[Omitted image "info-icon.png"\] Alt text: that appears.

\[Omitted image "arp-open-policy-rec.gif"\] Alt text: Hover over a record on the table to reveal the preview icon. From the record preview, select Open Record to open the record's form.

The Network Policy table displays the following information:

-   **Active**

    A true\|false value that shows whether each network policy is enabled.

-   **Host**

    Displays the external host that the application attempted to access when the policy was generated.

-   **Path**

    Resource paths or endpoints within the external network that the application attempted to access when the policy was generated. This might include API endpoints, image paths, or script locations. For Inbound Cross Scope Requests policy types, either a path or resource can be included \(not both\).

-   **Policy Type**

    Specifies the type of external network access the policy governs. Policy type describes both the direction of the request and whether it originates from client-side or server-side code.

    -   **Client Cross-origin Request** is a client-side request to an external host, such as a fetch or XHR call made from a UI page script.
    -   **Client Cross-origin Scripts** is a client-side request to load an external script resource.
    -   **Inbound Cross Scope Request** is a fetch or XHR request originating from the application as it runs in the browser, and attempting to access cross scope REST APIs, processors, or ServiceNow AI Platform APIs.
    -   **Inbound Global Request** is a global API request with a fetch call that doesn't follow the ARP governance model \(for example, websocket connections\).
    -   **Server Outbound Request** is a server-side outbound call to an external host, such as a call made from a script include.
-   **Resource**

    Identifies the specific platform processor and sub-processor involved in an external request, in `processor.subprocessor[.context]` format. For Inbound Cross Scope Request policy types, either a path or a resource can be included \(not both\).

-   **Scheme**

    Specifies the network protocol used when the application accesses the external host, if applicable.

-   **Short Description**

    A description of the policy. When using ARP, "Auto-created from violation" is the default, but can be changed.

-   **Status**

    Determines whether the application can access external networks as defined in the network policy. While an application is still in development, you can change the state as needed.

    -   **Allowed** is the default policy state when ARP is in tracking mode. It enables external network access as defined in the network policy.
    -   **Requested** is the default policy state when ARP is in enforcing mode. It prevents external network access as defined in the network policy and indicates that you haven't approved or denied the policy.
    -   **Denied** state prevents external network access as defined in the network policy.

