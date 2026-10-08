---
title: Environment and capability controls
description: Environment and capability controls limit what ServiceNow Cowork can access while an action runs, keeping the agent within the boundaries you set.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/environment-capability-controls.html
release: brazil
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 1
keywords: [sandbox rules, network rules, connector scopes, capabilities, file type rules]
breadcrumb: [Reference, ServiceNow Cowork, Extending AI with external systems and providers, Enable AI Experiences]
---

# Environment and capability controls

Environment and capability controls limit what ServiceNow Cowork can access while an action runs, keeping the agent within the boundaries you set.

Environment and capability controls govern what an action can access when it begins executing. Tool gates and approval policies determine whether an action can run, while environment and capability controls determine what a running action can access and do.

-   **Sandbox rules**

    Cowork runs actions inside an isolated virtual environment. Sandbox rules set the file system boundary and network access for the execution environment. You can add restrictions to the default protections for credential paths and system directories but can't remove them. You can also add filesystem deny rules that block the agent from writing to specific paths. For an example, see .

-   **Network rules**

    By default, Cowork blocks all outbound traffic except to the hosts, domains, and ports in the network allow list. The Default Policy includes a predefined list of trusted domains.

-   **Connector scopes**

    A connection credential for a service from a third-party may grant broad access. Connector scopes restrict what Cowork can do on that service, independent of the credential. Scopes apply to capabilities on a resource. For example, you can restrict write access to mail without affecting calendar access. For the Microsoft 365 connector, the OAuth scopes that you turn on determine which operations are available. Users can narrow their own permissions but can't widen them beyond what you turn on.

-   **Capabilities**

    Capabilities are feature switches and numeric limits. You can turn features and connectors on or off for specific users or user groups, including connectors that are turned off by default. Capability overrides change an effective value without altering the default.

-   **File type rules**

    File type rules set read, write, or deny access for each file extension. Rules apply in priority order, and ties resolve toward the more restrictive rule.


**Parent Topic:**[ServiceNow Cowork reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/servicenow-cowork-reference.md)

