---
title: Agent Client Collector release notes
description: The ServiceNow Agent Client Collector application enables you to monitor the service availability, performance, and infrastructure of your system. See the following sections for release notes by version.This release enables discovering software installed by package managers and provides enhanced error tracking with the Error Framework application. Additionally, agents have enhanced efficiency when working with virtual VDI machines.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/agent-client-collector-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [IT Operations Management release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Agent Client Collector release notes

The ServiceNow® Agent Client Collector application enables you to monitor the service availability, performance, and infrastructure of your system. See the following sections for release notes by version.

## About Agent Client Collector

-   Monitor the performance and health of your infrastructure components.
-   Enable proactive management and troubleshooting of Configuration Items \(CIs\).
-   Identify characteristics of components running on your servers, as an alternative to horizontal, IP-based Discovery.

See [Agent Client Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/acc-landing-page.md) for more information.

## Activation and other requirements

**Note:** Agent Client Collector is available in the ServiceNow Store. For details, see the following activation information.

-   **Activation information**

    Agent Client Collector is available with activation of the Agent Client Collector Framework plugin \(sn\_agent\) and the Agent Client Collector Monitoring plugin \(sn\_itmon\) in an instance on which Event Management is installed.


## Accessibility and localization

-   **Localization information**

    The current available languages for Agent Client Collector are US English, UK English, French, German, Italian, Japanese, and Spanish. The default language is US English.


**Parent Topic:**[IT Operations Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/it-operations-management-rn-landing.md)

## Version 7.0.1

This release enables discovering software installed by package managers and provides enhanced error tracking with the Error Framework application. Additionally, agents have enhanced efficiency when working with virtual VDI machines.

### What's new

-   **[Discover portable software installed by package managers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/accvc-package-discovery.md)**

    Discover software installed on endpoints via package managers that isn't discoverable by traditional checks and policies.

-   **[Create a custom filter rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/create-custom-filter-rule.md)**

    Create a custom software filter rule to exclude irrelevant entries from Discovery in your Software Asset Management \(SAM\) inventory.

-   **[Configure a license key discovery rule and write a parser script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/configure-license-key-rule.md)**

    Verify software legitimacy by creating license keys on your Windows, Linux and macOS devices.

-   **[Categorize software](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/acc-software-categorization.md)**

    Use software categorization to group discovered software packages into business-relevant categories. Software categorization helps you avoid manually tagging software and provides administrative teams with an efficient inventory of software records.

-   **[Track software on Windows applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/using-enhanced-discovery-and-sam-together.md)**

    Use improved software tracking on Windows applications. Software tracking informs you of the last time the application was used.

-   **[Require a maintenance token for Windows uninstalls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/require-maintenance-token-uninstall.md)**

    Require using a maintenance token when uninstalling an agent from a Windows device. A maintenance token provides a layer of protection so that unauthorized personnel can't perform the uninstall.

-   **[Enable a non-persistent virtual desktop infrastructure agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/enable-npvdi-agent.md)**

    Configure an agent to enable it to work in a Virtual Desktop Infrastructure \(VDI\) environment. VDI agents gather data more quickly than traditional agents not enabled for a VDI.

-   **[Categorize discovered browser extensions and software packages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-operations-management/acc-categorize-discovered-software.md)**

    Discover browser extensions and software packages by category. Categorization removes the need to tag software records manually and provides an accurate software inventory.


### What's deprecated or removed

-   **UserAssist deprecation during SAM last-used metric collection**

    The Windows `UserAssist` registry key is no longer used to determine the **last-used** timestamp for installed software. The **last-used** value is now derived from running-process snapshots collected by the existing SAM metering poll on the endpoint, with a Windows registry **Run** key used for auto-start applications.


