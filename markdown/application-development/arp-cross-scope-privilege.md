---
title: Cross scope privilege
description: Cross-scope privilege records define rules for access to application resources outside your application's scope. Application Runtime Policy generates cross scope privilege records automatically when your application attempts to access resources beyond its own scope.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/arp-cross-scope-privilege.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Explore, Application Runtime Policy \(ARP\), Developing your application, Building applications]
---

# Cross scope privilege

Cross-scope privilege records define rules for access to application resources outside your application's scope. Application Runtime Policy generates cross scope privilege records automatically when your application attempts to access resources beyond its own scope.

When an application attempts to access resources that belong to a different application scope, Application Runtime Policy \(ARP\) generates a new policy within the Cross Scope Privilege table. ARP's cross scope access enhances any existing cross scope privileges, so all related functionalities \(for example, Restricted Caller Access\) still operate without interference. To navigate to a specific policy record from the Cross Scope Privilege table, hover over a policy and select the preview icon\[Omitted image "info-icon.png"\] Alt text: that appears.

The Cross Scope Privilege table displays the following information:

-   **Source Scope**

    The application requesting runtime access to another application's resources.

-   **Target Scope**

    The application whose resources are being requested.

-   **Target Name**

    The name of the table, script include, or script object being requested.

-   **Operation**

    The operation the script performs on the target. The target type determines the available operations. Tables support the read, write, create, and delete operations. Script includes and script objects only support the execute API operation.

-   **Status**

    Determines whether the application can access resources from different application scopes as defined in the cross scope privilege record. While an application is still in development, you can change the state as needed.

    -   **Allowed** is the default policy state when ARP is in tracking mode. It enables access to resources in different application scopes as defined in the network policy.
    -   **Requested** is the default policy state when ARP is in enforcing mode. It prevents access to resources in different application scopes as defined in the cross scope privilege record and indicates that you haven't approved or denied the privilege.
    -   **Denied** state prevents access to resources in different application scopes as defined in the cross scope privilege record.
-   **Application**

    The name of the application that attempted to access resources outside its own scope.


