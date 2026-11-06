---
title: Environment and capability controls
description: Environment and capability controls limit what ServiceNow Arc can access while an action runs, keeping the agent within the boundaries you set.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/environment-capability-controls.html
release: australia
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 2
keywords: [sandbox rules, network rules, connector scopes, capabilities, file type rules]
breadcrumb: [Reference, ServiceNow Arc, Extend, AI Workflow Factory Prime, Agentic app development, Building applications]
---

# Environment and capability controls

Environment and capability controls limit what ServiceNow Arc can access while an action runs, keeping the agent within the boundaries you set.

Environment and capability controls govern what an action can access when it begins executing. Tool gates and approval policies determine whether an action can run, while environment and capability controls determine what a running action can access and do.

-   **Sandbox rules**

    Arc runs actions inside an isolated virtual environment. Sandbox rules set the file system boundary and network access for the execution environment. You can add restrictions to the default protections for credential paths and system directories but can't remove them. You can also add filesystem deny rules that block the agent from writing to specific paths. For an example, see [Prevent changes to sandbox files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/prevent-changes-sandbox.md).

    On Windows, Arc applies sandbox and network rules when it creates the sandbox. When a policy changes, Arc rebuilds the sandbox after running tasks finish. Rules that limit which programs can run are checked before a command starts, not inside the sandbox, and network rules set to monitor aren't enforced.

-   **Network rules**

    By default, Arc blocks all outbound traffic except to the hosts, domains, and ports in the network allow list. The Default Policy includes a predefined list of trusted domains.

-   **Connector scopes**

    A connection credential for a service from a third-party may grant broad access. Connector scopes restrict what Arc can do on that service, independent of the credential. Scopes apply to capabilities on a resource. For example, you can restrict write access to mail without affecting calendar access. For the Microsoft 365 connector, the OAuth scopes that you turn on determine which operations are available.

    For each Microsoft 365 capability, you can allow it, require user approval, or deny it. Your setting is the most a user can choose. If you allow a capability, users can choose **Allow**, **Ask me first**, or **Deny**. If you require approval, users can choose **Ask me first** or **Deny**. If you deny it, the capability is off. A capability you allow starts as **Allow** for users, and one that requires approval starts as **Ask me first**. To require approval, select **Approval gate** on the connector scope in the policy.

-   **Capabilities**

    Capabilities are feature switches and numeric limits. You can turn features and connectors on or off for specific users or user groups, including connectors that are turned off by default. Capability overrides change an effective value without altering the default.

-   **File type rules**

    File type rules set read, write, or deny access for each file extension. Rules apply in priority order, and ties resolve toward the more restrictive rule.


**Parent Topic:**[ServiceNow Arc reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/servicenow-cowork-reference.md)

